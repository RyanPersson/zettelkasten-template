# zet-setup

MAY be possible to save all these configs and make them portable:


### To set up `Paste Image from local pc`
Install extension `sakamoto66.vscode-paste-image`

In zet root workspace, go to workspace settings:
1. press `Ctrl+,`
2. Go to `Workspace>Extensions>Paste Image Configuration
3. Set `Paste Image Path:` from `./` to `./media/`

This tells `vscode-paste-image` to save images in ./media/ relative to the file they're pasted in.


[[vscode-global-setup]]

## Place to store my settings for my vscode workplace and howto-installs

See 

[[environment-setup]]

[[desktop]]

[[vscode-global-setup]]

<br>

Also worth using: [reccomended  workspace settings](https://github.com/kortina/vscode-markdown-notes/blob/master/RECOMMENDED-SETTINGS.md) from vscode markdown notes extension.

<br>


Vscode can hide stuff from search by keeping it in .gitignore 
I believe ag does the same thing

<br>
Currently using Paste-Markdown extension to paste images into desktop/ui side
markdown using Ctrl+shift+v
---

Trying out Markdown-Links to see graphs:

YOU LOVE IT, use command:
```
Show Graph
```
in command shift pallete (Ctrl+Shift+P)
---


need to [[make-vscode-portable]]

---
# Set code wrapping in Markdown Preview Enhanced Extension:

From [this issue on gh](https://github.com/shd101wyy/markdown-preview-enhanced/issues/1224)

1. `Ctrl+Shift+P` to open command palette.
2. go to `Markdown Preview Enhanced: Customize CSS`
3. Add: 
```
.markdown-preview.markdown-preview {
       pre, code {
            white-space: pre-wrap;
       }
}
```
to `styles.less`.


## Forward Links


