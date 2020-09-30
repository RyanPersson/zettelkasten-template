# vscode-global-setup


[[vscode]] general tips

Need in global settings.json:
```
"vim.overrideCopy": false,
```

Need for markdown zet:
```json
    "[markdown]": {
        "editor.quickSuggestions": true
    },
```


Copy of global settings: figure out what's nescessary
```json
{
    "window.zoomLevel": 1,
    "terminal.integrated.inheritEnv": false,
    "editor.suggestSelection": "first",
    "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
    "python.jediEnabled": false,
    "[html]": {
        "editor.defaultFormatter": "HookyQR.beautify"
    },
    "latex-workshop.view.pdf.viewer": "browser",
    "vim.overrideCopy": false,
    "[javascript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "editor.minimap.enabled": false,
    "window.menuBarVisibility": "default",
    "javascript.updateImportsOnFileMove.enabled": "always",
    "diffEditor.ignoreTrimWhitespace": false,
    "workbench.editor.enablePreview": false,
    "[markdown]": {
        "editor.quickSuggestions": true
    },
    "MarkdownPaste.path": "./media/",
    "python.condaPath": "C:/Users/perss/miniconda3/",
    "python.languageServer": "Microsoft",
    "python.dataScience.alwaysTrustNotebooks": true
}
```


#todo POSSIBLY run vscode in docker container. See [this example docker image](https://github.com/caesarnine/data-science-docker-vscode-template) containing conda, jupyter & vscode. 

Good way to encapsulate extensions possibly?