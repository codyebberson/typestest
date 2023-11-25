# typestest

Variables:

1. Whether to include top-level `"types"`
2. Whether to include `"types"` in `"exports"`
3. Whether to use specialty file extensions `.d.cts` and `.d.mts` vs normal `.d.ts`

Outputs:

1. Does it pass https://arethetypeswrong.github.io/
2. Does it work with https://www.typescriptlang.org/play

| id  | top-level `"types"` | `"types"` in `"exports"` | specialty file extensions | TS project | TS playground | are the types wrong |
| --- | ------------------- | ------------------------ | ------------------------- | ---------- | ------------- | ------------------- |
| 1   | no                  | no                       | no                        | ❌         | ❌            | ❌ No types         |
| 2   | no                  | no                       | yes                       | 🟢         | ❌            | 🟢                  |
| 3   | no                  | yes                      | no                        | ❌         | ❌            | ❌ No types         |
| 4   | no                  | yes                      | yes                       | 🟢         | ❌            | 🟢                  |
| 5   | yes                 | no                       | no                        | 🟢         | 🟢            | ❌ No types         |
| 6   | yes                 | no                       | yes                       | 🟢         | ❌            | 🟢                  |
| 7   | yes                 | yes                      | no                        | 🟢         | 🟢            | 🟢                  |
| 8   | yes                 | yes                      | yes                       | 🟢         | ❌            | 🟢                  |
