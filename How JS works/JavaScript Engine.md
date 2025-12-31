
# JavaScript Engine
A JavaScript engine is simply a computer program that executes JavaScript code. It's responsible for translating human-readable JavaScript code into machine-readable instructions that the computer's hardware can execute.

## How JS engine works

- Any JS engine always contains a call stack and a heap.
- The call stack is where our code gets executed with the help of the execution context.
- And the heap is an unstructured memory pool that stores all the objects in the memory that our application needs.

<img width="600" alt="image" src="https://github.com/user-attachments/assets/2a3ff95e-c64f-4ef4-aeb2-8fdc74424d71" />

The question is how the code gets compiled to machine code so that it can execute afterwards.

### Compilation vs Interpretation

<img width="1034" height="161" alt="image" src="https://github.com/user-attachments/assets/8a441ae9-cb4f-43af-899e-3829c750262c" />
<img width="1032" height="205" alt="image" src="https://github.com/user-attachments/assets/9a37e2cf-2ab6-49e9-b89a-f2af21cbfc12" />

- JS used to be a purely interpreted language. But since interpretation is slow, a mix of compilation and interpretation is used which is called JIT (Just-in-time) compilation.
- In JIT, "selective compilation" is done in runtime, on a demand basis. Only that code is compiled which will benefit from compilation. The remaining code is simply interpreted.
- It works by identifying frequently used code sections ("hotspots") and compiling them to optimized machine code for direct CPU execution, speeding up repeated tasks after an initial "warm-up" period. 
