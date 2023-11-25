# typestest

### Variables

1. Whether to include top-level `"types"`
2. Whether to include `"types"` in `"exports"`
3. Whether to use specialty file extensions `.d.cts` and `.d.mts` vs normal `.d.ts`

### Outputs

1. Does it work as a dependency in a TypeScript project
2. Does it work with https://www.typescriptlang.org/play
3. Does it pass https://arethetypeswrong.github.io/

### Test code

```ts
import { sum1 } from "typestest1";
import { sum2 } from "typestest2";
import { sum3 } from "typestest3";
import { sum4 } from "typestest4";
import { sum5 } from "typestest5";
import { sum6 } from "typestest6";
import { sum7 } from "typestest7";
import { sum8 } from "typestest8";

console.log("sum1(1, 2) =", sum1(1, 2));
console.log("sum2(1, 2) =", sum2(1, 2));
console.log("sum3(1, 2) =", sum3(1, 2));
console.log("sum4(1, 2) =", sum4(1, 2));
console.log("sum5(1, 2) =", sum5(1, 2));
console.log("sum6(1, 2) =", sum6(1, 2));
console.log("sum7(1, 2) =", sum7(1, 2));
console.log("sum8(1, 2) =", sum8(1, 2));
```

### Results

| id  | top-level `"types"` | `"types"` in `"exports"` | specialty file extensions | TS project | TS playground | are the types wrong |
| --- | ------------------- | ------------------------ | ------------------------- | ---------- | ------------- | ------------------- |
| 1   | no                  | no                       | no                        | ❌         | ❌            | ❌                  |
| 2   | no                  | no                       | yes                       | 🟢         | ❌            | 🟢                  |
| 3   | no                  | yes                      | no                        | ❌         | ❌            | ❌                  |
| 4   | no                  | yes                      | yes                       | 🟢         | ❌            | 🟢                  |
| 5   | yes                 | no                       | no                        | 🟢         | 🟢            | ❌                  |
| 6   | yes                 | no                       | yes                       | 🟢         | ❌            | 🟢                  |
| 7   | yes                 | yes                      | no                        | 🟢         | 🟢            | 🟢                  |
| 8   | yes                 | yes                      | yes                       | 🟢         | ❌            | 🟢                  |

### Conclusion

The best option is:

1. Include top-level `"types"`
2. Include `"types"` in `"exports"`
3. Do not use specialty file extensions `.d.cts` and `.d.mts`
