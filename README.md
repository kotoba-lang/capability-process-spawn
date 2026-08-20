# capability-process-spawn

Atomic authority package for `process/spawn` (compiler wire id **20**, ADR-t83).

- imports: `#{process-spawn}`
- effects: `#{system-write :process-exec}`
- default policy: `:approval-required`
- semantic definition CID: `bafyreihqyss6vswxjwjrfeafcuuzphbtzzlyxzbssk3tmut5r3w5ldqlrb`
- hash contract CID: `bafkreiflhj3fslsbh7okdas2fzlhmogai64x6p3lkla6gtr7berbp7ftvi`
- provider status: `contract-only`

Pairs with the foundational stdlib [`kotoba-lang/process`](https://github.com/kotoba-lang/process)
(`kotoba.lang.process` / `kotoba.lang.process-host`). Importing this package does
**not** grant runtime authority: Tamaki must request it and Kototama must admit
the sealed envelope. Hosts must still inject absolute `:binaries` — no PATH.

Sibling: [`capability-process-list`](https://github.com/kotoba-lang/capability-process-list)
covers listing only, not spawn.

```sh
clojure -M:test
```
