# lib-ws-frame

WebSocket frame contract — RFC 6455 opcodes and encode/decode types.

Part of the `handl-lang` org split (ADR-0128). History is a `git subtree
split` of the platform monorepo's `ws_frame/` (via `web`).

## Layout

```text
src/        the .hnl sources
pkg.hnl     dependencies, when any: `{ deps: { <name>: "branch:<ref>" } }`
```

## Gate

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

## License

MIT.
