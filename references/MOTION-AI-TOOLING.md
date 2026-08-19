# Motion AI Tooling for Aurex

Motion AI Kit belongs to the Claude Code development environment, not to every client website. It supplies current Motion documentation, implementation guidance, example search, CSS spring generation, transition editing, and, where the account permits, MotionScore performance analysis. Aurex still owns the creative decision.

## Recommended Claude Code setup

Follow Motion's current official installer rather than copying a static MCP configuration:

```bash
npx motion-ai@latest
```

Choose the global scope and Claude Code when prompted so the tooling is available across Aurex client repositories. Activate the installed Motion MCP servers in Claude Code if the installer asks for that final step.

Re-run the same command at the same scope to upgrade. Current Motion documentation says the installer rewrites its skill and MCP configuration in place and uses Motion's hosted MCP servers. The older local MCP configuration containing an `npx` command and `TOKEN` is retired and should be removed if present.

Official sources:

- [Motion AI Kit](https://motion.dev/docs/ai-kit)
- [Install Motion AI Kit](https://motion.dev/docs/ai-kit-install)
- [Motion for React](https://motion.dev/docs/react)
- [Motion accessibility](https://motion.dev/docs/react-accessibility)

Access to premium examples, Motion UI source, the transition editor, and MotionScore may depend on Motion+ access. Do not make Aurex project completion depend on an unavailable premium feature.

## Responsibility boundary

Aurex defines:

- why something moves and what deserves emphasis
- motion personality and intensity
- hierarchy, continuity, choreography, and restraint
- brand and creative-concept fit
- conversion impact
- mobile behavior and reduced-motion intent
- which of the site's 1-3 signature moments use motion

Motion AI Kit provides current API syntax, official implementation patterns, performance guidance, reduced-motion practices, and optional inspection/editing tools. It does not choose the creative direction or justify an effect merely because an example exists.

## Client runtime boundary

Do not copy the AI Kit, its MCP configuration, or its agent skill into client sites by default. A client repository receives only the runtime dependencies required by its approved concept.

For a React client that actually uses Motion, follow the current official install and imports:

```bash
npm install motion
```

```ts
import { motion } from "motion/react"
```

Use the client's existing package manager rather than assuming npm. Motion currently requires React 18.2 or newer. Do not install Motion when CSS fully expresses the approved interaction.
