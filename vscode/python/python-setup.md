# VSCode Reference Guide for Python Projects

## .vscode/settings.json

```json
// https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance
// https://code.visualstudio.com/docs/python/linting
// https://code.visualstudio.com/docs/python/editing
{
  "python.pythonPath": "/path/to/python/",
  "python.analysis.extraPaths": [
    ""
  ],
  "python.linting.enabled": true,
  "python.linting.lintOnSave": true,
  "python.linting.pylintEnabled": true,
  "python.linting.pylintArgs": [""],
  "python.linting.maxNumberOfProblems": 200,
  "python.linting.ignorePatterns": [
    ".vscode/*.py",
    "**/site-packages/**/*.py"
  ],
  "python.formatting.provider": "autopep8",
  "python.formatting.autopep8Args": [
    "--max-line-length",
    "79",
    "--experimental",
    "--indent-size=4"
  ],
  "python.autoComplete.extraPaths": [
    "./sync/",
    "./",
  ],
  "python.sortImports.args": [
    "--atomic"
  ],
  "terminal.integrated.scrollback": 100000,
  "editor.insertSpaces": true,
  "editor.tabSize": 4,
  "editor.formatOnSave": true,
}
```

## .vscode/launch.json

```json
// https://code.visualstudio.com/docs/python/debugging
// https://code.visualstudio.com/docs/editor/debugging
{
  "configurations": [
    {
      "name": "Usersync Script",
      "type": "python",
      "request": "launch",
      "program": "${file}",
      "args": ["arg1", "arg2", "arg3"],
      "pythonArgs": ["arg1", "arg2", "arg3"],
      // VScode take env vars from a .env file as well
      "env": {
        "ENV_VAR_01": "VALUE_01",
        "ENV_VAR_01": "VALUE_02",
        "ENV_VAR_03": "VALUE_03",        
      },
      "cwd": "${fileDirname}",
      "console": "integratedTerminal",
    }
  ]
}
```

## .pylintrc

The following configuration file is a reference. Before disabling any pylint message control it should be thought carefully why are you disabling it.

```plain
[MESSAGES CONTROL]

disable=
    logging-fstring-interpolation,
    E1101, # no-member
    C0301, # line-too-long
    C0103, # invalid-names
    C0114, # missing-module-docstring
    C0115, # missing-class-docstring
    C0116, # missing-function-docstring
```
