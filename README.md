# cpachecker-vscode-plugin-poc

This is a VS Code extension communicating with a MagpieServer as described in [part two of the official MagpieBridge tutorials](https://www.github.com/MagpieBridge/MagpieBridge/wiki/Tutorial-2.Display-any-results-in-IDEs-with-MagpieBridge).

The language server is included as an executable jar file. On activation, the extension executes this jar and hands the path to a mock result file (`preparedResults.json`) which indicates a problem with a parameter in the tutorial's [DemoProject](https://github.com/MagpieBridge/DemoProject). A new _ServerAnalysis_ that knows the path to the mock result is added to the language server.

## How to run

1. Install dependencies:

   ```
   npm install
   ```

2. `cd` to the project folder
3. Make sure to use the latest stable node version: `nvm use --lts`
4. Use VS Code Extension Manager `vsce` to pack the extension into `.vsix` file:
   ```
   npm install -g vsce
   vsce package
   ```
   _Note: using vsce in this way is deprecated, but should suffice for now_
5. Install the extension:
   ```
   code --install-extension cpachecker-vscode-plugin-poc-0.0.1.vsix
   ```
6. Open [_DemoProject_](https://github.com/MagpieBridge/DemoProject)
