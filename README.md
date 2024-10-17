# The TypeScript Compiler and its configuration

## Watch Mode

```sh
    tsc app.ts -watch
    
    # Shorter version
    tsc app.ts -w
```

# Compiling the entire project (multiple files)

```sh
    # Run once to Generate the tsconfig.json
    tsc --init
```

```sh
    # Compile all typescript files
    tsc
```

```sh
    # Watch for changes and recompiles the typescript files
    tsc -watch
    
    # Shorter version
    tsc -w
```

# Including & Excluding Files

We can set in the [tsconfig.json](tsconfig.json#L110) file a `exclude` key to set a list of files or paths to exclude from compilation. If `exclude` is not specified `node_modules` folder is excluded by default, but if you are using the `exclude` key you need to specify the `node_modules` folder.

`**/*.dev.ts` selects all files in all paths wih .dev.ts termination.

Alternatively, we could set a `include` key that sets a list of files or paths to compile.

Also, we have the `files` key that contains a list of files that will be included in the compilation.

## Debugging

Enable `sourceMap` option in the [tsconfig.json](tsconfig.json#L61), set the break points in the code and `Start Debugging` on VSCode - the first time will generate a `.vscode` configuration file where you need to put the port that the server is running.

## References

* tsconfig Docs:
  <https://www.typescriptlang.org/docs/handbook/tsconfig-json.html>

* Compiler Config Docs:
  <https://www.typescriptlang.org/docs/handbook/compiler-options.html>

* VS Code TS Debugging:
  <https://code.visualstudio.com/docs/typescript/typescript-debugging>
