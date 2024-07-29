# Angular Compilation (JIT vs AOT)

- JIT (Just-In-Time Compilation)
- AOT (Ahead-of-Time Compilation)

## JIT Compilation
    - Compiled in the browser.
    - Each file compiled separately.
    - No need to build after changing your code and before reloading the browser page.
    - Suitable for local development.

## AOT Compilation
    - Compiled by the machine itself, via the command line (Faster).
    - All code compiled together, inlining HTML/CSS in the scripts.
    - No need to deploy the compiler (Half of Angular size).
    - More secure, original source not disclosed.
    - Suitable for production builds.

[Deep Dive](https://stackoverflow.com/questions/45703443/what-is-the-difference-between-angular-aot-and-jit-compiler)