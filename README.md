# json-renderskill

```
   _       _          ____                 _           _ _
  (_) __ _| |__      |  _ \ ___ _ __   __ _| | ___  ___| | |
  | |/ _` | '_ \ ____| |_) / _ \ '_ \ / _` | |/ _ \/ __| | |
  | | (_| | | | |____|  _ <  __/ | | | (_| | |  __/\__ \_|_|
 _/ |\__,_|_| |_|    |_| \_\___|_| |_|\__,_|_|\___||___(_|_)
|__/
```

Agentic Skill to use the Vercel AI SDK for json-render . This repo ships a shareable  skill named `ai-sdk` that helps you:

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
I used it interally in a few apps:
Suggeestions are dynamically generated to create custom learning environments more condusive to convey certain feedback:
<img width="1726" height="989" alt="Screenshot 2026-01-28 at 3 21 34 AM" src="https://github.com/user-attachments/assets/f961fff2-6658-46e7-974f-8d3185ee4637" />
Or here to give the user ways to configure their interview based on their desired conversation:
<img width="882" height="586" alt="Screenshot 2026-01-28 at 3 23 59 AM" src="https://github.com/user-attachments/assets/<img width="752" height="955" alt="Screenshot 2026-01-28 at 3 25 02 AM" src="https://github.com/user-attachments/assets/45143d76-4303-4ed4-b280-c2882321f09e" />
e1279b1b-c6c8-45e9-afef-8a29081ae09b" />

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
