# vscode-chrome-debug-config
VSCode Chrome Debug configuration with Webpack 2

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
      },
      "skipFiles": [
        "node_modules"
      ]
    },
    {
      "name": "Chrome Debug Server Cart",
      "type": "chrome",
      "request": "launch",
      "sourceMaps": true,
      "port": 9222,
      "url": "https://wycart.dev/",
      "webRoot": "${workspaceRoot}/app",
      "diagnosticLogging": true,
      "sourceMapPathOverrides": {
        "webpack:///./*":   "${webRoot}/*"
      }
    }
  ]
}
```
into **webpack.config.js** add `devtool: "inline-source-map"`.

### Enjoy your debugging!
