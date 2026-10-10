# AGENTS.md

Guidance for AI coding agents working in this repository.

## What this is

`@three-ws/retarget` v0.1.2. Retarget animations onto any humanoid GLB. Canonicalizes bone names from Mixamo, Avaturn, VRM/VRoid, Daz/Genesis, MakeHuman, Unreal, and Blender rigs onto one canonical skeleton, retargets clips with rest-pose and hip-axis correction, and drives them with a crossfading runtime, so no rig ever freezes in a T-pose.

A JavaScript library. Import it from ESM.

## Use it

```bash
npm install @three-ws/retarget
```

Full usage, tool list and configuration are in [README.md](README.md). Machine-readable summaries: [llms.txt](llms.txt) and [llms-full.txt](llms-full.txt).

## Develop

```bash
npm install
npm test
```

Scripts:
- `npm run build`: `node build.mjs`
- `npm run pretest`: `npm run build`
- `npm run test`: `node --test test/*.test.mjs`
- `npm run prepublishOnly`: `npm run build && npm test`

## Conventions

- ES modules, Node >=18.
- Read-only by default. Anything that signs, spends or sends must be an explicit, separately named tool or option, and must never be inferred from untrusted text (token names, memos, listings).
- Never commit credentials. Configuration comes from environment variables documented in the README.
- Keep changes small and covered by a test next to the code they change.

## Source of truth

This repository is a generated mirror of `packages` in https://github.com/nirholas/three.ws. Open issues here; send substantial changes as a pull request here or upstream.
