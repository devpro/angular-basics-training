# Debugging

## Visual Studio Code (VS Code)

* Install from [code.visualstudio.com](https://code.visualstudio.com/)
* Make sure Firefox is installed
* Open VS Code and install the folloging extensions
  * [Debugger for Firefox](https://marketplace.visualstudio.com/items?itemName=firefox-devtools.vscode-firefox-debug)

_To know more about VS Code, have a look at [everyday-cheatsheets](https://github.com/devpro/everyday-cheatsheets/blob/main/docs/microsoft/vscode.md)_

### Debug with Visual Studio Code

* Create a file `.vscode/launch.json` at the root of the Angular project
* Put the following file content

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Launch localhost",
      "type": "firefox",
      "request": "launch",
      "reAttach": true,
      "url": "http://localhost:4200",
      "webRoot": "${workspaceFolder}"
    }
  ]
}
```

* In VS Code, from the Debug view, click on the Start Debugging icon or hit F5
* Add/remove breakpoints and enjoy debugging your code!
