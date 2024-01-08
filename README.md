# cpachecker-vscode-plugin-poc

This is a VS Code extension communicating with a MagpieServer as described in [Tutorial 2](https://www.github.com/MagpieBridge/MagpieBridge/wiki/Tutorial-2.Display-any-results-in-IDEs-with-MagpieBridge).

## How to run

1. `cd` to the project folder
2. Use the latest stable node version: `nvm use --lts`
3. Use VS Code Extension Manager `vsce` to pack the extension into `.vsix` file:
   ```
   npm install -g vsce
   vsce package
   ```
   _Note: using vsce in this way is deprecated, but should suffice for now_
4. Install the extension:
   ```
   code --install-extension cpachecker-vscode-plugin-poc-0.0.1.vsix
   ```
5. Open [_DemoProject_](https://github.com/MagpieBridge/DemoProject)
