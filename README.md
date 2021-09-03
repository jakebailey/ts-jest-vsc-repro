Reproducer for broken `ts-jest` source mapping in VS Code 1.60; works in 1.59 and below.

1. Open `index.ts` and set a breakpoint on the log line.
2. Open `doSomething.test.ts` and run the debug task. The breakpoint will not be hit.
3. Set a breakpoint in `doSomething.test.ts`; the breakpoint will be caught in the unmapped transformed file, on the wrong line.
