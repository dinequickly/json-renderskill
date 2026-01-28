# UI Rendering Patterns (AI SDK)

## Tool output shape
- Keep outputs JSON-serializable.
- Prefer stable keys for lists (`id`, `slug`) so React list rendering is predictable.
- For shared UI components, add a `kind` field or normalize to a common shape.

Example normalized output:
```ts
{ kind: 'weather', temperature: 72, unit: 'F', description: 'sunny' }
```

## Message-part helpers
Use a small helper to keep rendering logic consistent.

```tsx
function renderPart(part: any, renderers: Record<string, (output: any) => JSX.Element>) {
  if (part.state !== 'output-available') return null;
  if (part.type === 'text') return <div>{part.text}</div>;
  if (part.type && renderers[part.type]) return renderers[part.type](part.output);
  return null;
}
```

## Tool name conventions
Most clients emit tool parts as `tool-<toolName>`. If your framework uses a different prefix, adapt the registry keys to match what you receive.

## Streaming UI notes
- Create the UI stream once per request.
- Only call `done(...)` when the final component is ready.
- If your SDK version supports incremental updates, you can `update(...)` with intermediate UI states and then `done(...)`.

## Debugging tips
- Log the raw message parts to confirm `part.type` and `part.state` values.
- If UI does not render, confirm the tool output matches component props and is serializable.
