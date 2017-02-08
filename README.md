# VSCode Chrome Debug configuration with Webpack 2

Use for this extension: [VSCode Chrome Debug Extension](https://github.com/Microsoft/vscode-chrome-debug)

Add into `.vscode/launch.json` this code.
```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Chrome Debug Local",
      "type": "chrome",
      "request": "launch",
      "sourceMaps": true,
      "port": 9222,
      "url": "http://localhost:3000/",
      "webRoot": "${workspaceRoot}",
      "verboseDiagnosticLogging": true,
      "sourceMapPathOverrides": {
        "webpack:///*": "${webRoot}/app/*"
      }
    }
  ]
}
```
After into **webpack.config.js** add `devtool: "inline-source-map"`.

### Enjoy your debugging!
