# VSCode Chrome Debug configuration with Webpack 2

Use for this extension: [VSCode Chrome Debug Extension](https://github.com/Microsoft/vscode-chrome-debug)

Add into `.vscode/launch.json` this code.
```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "chrome",
      "request": "launch",
      "name": "Debug Chrome",
      "url": "http://localhost:8080",
      "webRoot": "${workspaceFolder}",
      "sourceMaps": true,
      "sourceMapPathOverrides": {
        "webpack:///*": "${webRoot}/src/*"
      }
    }
  ]
}
```
After into **webpack.config.js** add `devtool: "inline-source-map" or "source-map"`.

### Enjoy your debugging!
