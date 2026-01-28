# json-renderskill

```
   _       _          ____                 _           _ _
  (_) __ _| |__      |  _ \ ___ _ __   __ _| | ___  ___| | |
  | |/ _` | '_ \ ____| |_) / _ \ '_ \ / _` | |/ _ \/ __| | |
  | | (_| | | | |____|  _ <  __/ | | | (_| | |  __/\__ \_|_|
 _/ |\__,_|_| |_|    |_| \_\___|_| |_|\__,_|_|\___||___(_|_)
|__/
```

Render UI from AI SDK tool calls. This repo ships a shareable Codex skill named `ai-sdk` that helps you:

- Return JSON from tool calls and map outputs to React components
- Render tool outputs on the client or stream UI from the server with RSC
- Keep multi-tool interfaces organized with registries and normalized shapes

## Install

From GitHub:
```
npx skills add https://github.com/dinequickly/json-renderskill.git --skill ai-sdk
```

From local files:
```
npx skills add ./dist/ai-sdk.skill
```

## Use

Prompt ideas:
- "Implement AI SDK tool calling that returns JSON and renders a WeatherCard."
- "Show how to stream UI with @ai-sdk/rsc in Next.js App Router."
- "Refactor a big switch statement into a tool renderer registry."

## What's inside

```
skills/
  ai-sdk/
    SKILL.md
    references/
      ui-rendering.md
```

## Package

Build a distributable `.skill`:
```
python3 ~/.codex/skills/.system/skill-creator/scripts/package_skill.py skills/ai-sdk dist
```

## License

MIT
