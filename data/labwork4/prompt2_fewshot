
You are an AI agent representing an end-to-end TypeScript dependency analysis system. 
You receive input X and must output y by executing the full pipeline (AST parsing → semantic resolution → dependency extraction → DSM → summary).

Below are known examples (X,y) pairs from previous analyses:

### Example 1
X:
Small project with files:
A.ts → imports B.ts
B.ts → imports C.ts
C.ts → imports A.ts
y:
Circular dependency detected: A ↔ B ↔ C
DSM shows strong cyclic coupling among all modules
Graph density: High
Recommendation: break cycle by extracting shared logic from module B

### Example 2
X:
Project using both runtime and type-only imports
y:
Dependencies: 70% runtime imports, 30% type-only imports
No circular dependencies detected
Recommendation: create separate folders for type-only modules to improve modular clarity

### Example 3
X:
Nested folder structure: module/ui/Button.ts imports module/core/Theme.ts and module/core/constants.ts
y:
No cycles detected
DSM shows one-way dependency direction: core → ui
Architecture score: Stable
Recommendation: fine-grained modularization not required at this time

---

### NEW REQUEST — Solve for a new X
Apply the same reasoning used in the above examples to the following input and generate y.

### X (Input):
Project: "TaskManagerTS"
Files:
-----------------------------
/main.ts
import { createTask } from "./services/task";
console.log(createTask("Study"));
-----------------------------
/services/task.ts
import { uid } from "../utils/id";
export function createTask(name: string) {
  return { id: uid(), name };
}
-----------------------------
/utils/id.ts
export const uid = () => Math.random().toString(36).substring(2);
-----------------------------

### Output y Format Required:
1) Dependency Graph (JSON or text)
2) DSM
3) Structural insights (runtime vs type-only imports)
4) Architecture quality summary
5) Suggested improvements (if any)

Begin.
