
To get started, you might want to explore the project directory structure and the default configuration file. Working with this project in your development environment will not affect any production deployment or identity tokens.

To learn more before you start working with dfx_react_typescript, see the following documentation available online:

- [Quick Start](https://sdk.dfinity.org/developers-guide/quickstart.html)
- [Developer's Guide](https://sdk.dfinity.org/developers-guide)
- [Language Reference](https://sdk.dfinity.org/language-guide)

## Important Note

Before you run `dfx build`, you must update the `@dfinity/agent` property in the package.json

to get the locataion of your `@dfinity/agent`, run `echo $HOME/.cache/dfinity/versions/<your-dfx-version>/js-user-library`. that should print something like this:

`"/Users/myname/.cache/dfinity/versions/0.5.7/js-user-library"`

Replace <js-user-library> in the `package.json` with the string found above.

```json
{
...
  "devDependencies": {
    "@dfinity/agent": <js-user-library>,
    ...
  }
}

```

```bash
cd dfx_react_typescript/

dfx start

# open a new terminal

dfx build
dfx install canister dfx_react_typescript

# use above output ID here:
# open http://localhost:8000/?canisterId=<your-canister-id>
```