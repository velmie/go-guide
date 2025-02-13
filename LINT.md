# Lint coverage

| Section     | Subsection                                         | Coverage           |
|-------------|----------------------------------------------------|--------------------|
| Guidelines  | Pointers to Interfaces                             | :heavy_check_mark: |
|             | Verify Interface Compliance                        | -                  |
|             | Receivers and Interfaces                           | -                  |
|             | Zero-value Mutexes are Valid                       | -                  |
|             | Copy Slices and Maps at Boundaries                 |                    |
|             | - Receiving Slices and Maps                        | -                  |
|             | - Returning Slices and Maps                        | -                  |
|             | - Always return a slice if a function modifies one | -                  |
|             | Defer to Clean Up                                  | -                  |
|             | Channel Size is One or None                        | -                  |
|             | Start Enums at One                                 | -                  |
|             | String() for enums                                 | -                  |
|             | Use `"time"` to handle time                        | -                  |
|             | Errors                                             |                    |
|             | - Error Types                                      | :heavy_check_mark: |
|             | - Error Wrapping                                   | -                  |
|             | - Error Naming                                     | :heavy_check_mark: |
|             | - Handle Errors Once                               | -                  |
|             | Handle Type Assertion Failures                     | :heavy_check_mark: |
|             | Don't Panic                                        | -                  |
|             | Use go.uber.org/atomic                             | -                  |
|             | Avoid Mutable Globals                              | -                  |
|             | Avoid Embedding Types in Public Structs            | -                  |
|             | Avoid Using Built-In Names                         | :heavy_check_mark: |
|             | Avoid `init()`                                     | :heavy_check_mark: |
|             | Exit in Main                                       | -                  |
|             | - Exit Once                                        | -                  |
|             | Use field tags in marshaled structs                | :heavy_check_mark: |
|             | Don't fire-and-forget goroutines                   | -                  |
|             | - Wait for goroutines to exit                      | -                  |
| Performance | Prefer strconv over fmt                            | :heavy_check_mark: |
|             | Avoid repeated string-to-byte conversions          | :heavy_check_mark: |
|             | Prefer Specifying Container Capacity               | :heavy_check_mark: |
| Style       | Avoid overly long lines                            | :heavy_check_mark: |
|             | Be Consistent                                      | -                  |
|             | Group Similar Declarations                         | -                  |
|             | Import Group Ordering                              | :heavy_check_mark: |
|             | Package Names                                      | :heavy_check_mark: |
|             | Function Names                                     | -                  |
|             | Import Aliasing                                    | -                  |
|             | Function Grouping and Ordering                     | -                  |
|             | Reduce Nesting                                     | :heavy_check_mark: |
|             | Unnecessary Else                                   | :heavy_check_mark: |
|             | Top-level Variable Declarations                    | -                  |
|             | Prefix Unexported Globals with `_`                 | -                  |
|             | Embedding in Structs                               | -                  |
|             | Local Variable Declarations                        | -                  |
|             | nil is a valid slice                               | -                  |
|             | Reduce Scope of Variables                          | -                  |
|             | Avoid Naked Parameters                             | -                  |
|             | Use Raw String Literals to Avoid Escaping          | -                  |
|             | Initializing Structs                               |                    |
|             | - Use Field Names to Initialize Structs            | -                  |
|             | - Omit Zero Value Fields in Structs                | -                  |
|             | - Use `var` for Zero Value Structs                 | -                  |
|             | - Initializing Struct References                   | -                  |
|             | Initializing Maps                                  | -                  |
|             | Format Strings outside Printf                      | -                  |
|             | Naming Printf-style Functions                      | -                  |
