# socketio/socket.io

- Stars: ~62k
- Evaluated: 2026-11-23 (midday run)
- Result: picked

## Contribution rules
Monorepo (engine.io, socket.io, clients, adapters under packages/). PR template: kind of change checkboxes + Current behavior / New behavior / Other information. Commit titles `fix(sio): ...`, `fix(eio-client): ...`. Outside PRs merged regularly (darrachequesne).

## AI / agent policy
None found.

## CLA / DCO
None.

## Tests / CI
`npm ci --ignore-scripts` (eiows needs make), compile the workspace deps (`npm run compile` in engine.io-parser, engine.io, socket.io-adapter, socket.io-component-emitter, socket.io-parser, engine.io-client, socket.io-client), then in packages/socket.io: `npm run format:check && npm run compile && npx mocha --import=tsx --timeout 10000 test/index.ts` (219 passing on main 0e247793).

## Decision
PICKED #5642 (duplicate CONNECT packets for one client+namespace create two Sockets and fire `connection` twice; `Client.ondecoded` guards on `nsps`, which is only set after the async `_add`). Reproduced with a raw ws client (2 connections), prototype pending-namespace set in Client fixed it (221 passing with 2 new tests; the duplicate test fails without the fix). Claim: https://github.com/socketio/socket.io/issues/5642#issuecomment-7094366646 . Brief: /workspace/batch-2026-11-23-midday/socket.io-5642.md. Nearby open PRs: #5600, #5588 (namespace middleware), #5623 (client side duplicate CONNECT).
