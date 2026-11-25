# lib-ws-frame

WebSocket frame **contract** — RFC 6455 opcodes and encode/decode
types. Pure `.hnl`.

## Layout

| path | role |
| --- | --- |
| `src/index.hnl` | the contract — opcodes + codec types |
| `pkg.hnl` | package manifest — `modules: ["ws_frame"]` |
| `scripts/hnl-gate.sh`, `workflows/gate.yaml` | the gate / bupha entry |

## Contract

- Port side of the frame codec: opcodes + encode/decode types;
  implementations are `lib-ws-frame-handl` (pure handl) and the C/host
  backends used by `lib-serve-epoll`/`lib-ws-c`.

## Verification

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

## License

MIT.

<!-- myco:agent-awareness -->

## Agent awareness

- Session start / any work discussion: run `myco status --prompt`
  before proposing next steps — know the board first.
- User describes new work → offer to capture it (`myco todo add`,
  `issue new`, `proposal new`). Don't wait to be asked.
- Picking up a task: `myco resume <ID>` is the briefing.
- Wrapping up: `myco handoff <ID>` anything resumable; keep statuses
  honest (claimed → in-progress → blocked/done).

<!-- /myco:agent-awareness -->
