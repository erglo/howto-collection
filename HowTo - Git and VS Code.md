# HowTo - Git and VS Code

REF.: [How to use VS Code as your Git editor, difftool, and mergetool](https://www.roboleary.net/vscode/2020/09/15/vscode-git.html) by _Rob O'Leary_  
REF.: [Visual Studio Code](https://code.visualstudio.com/) Homepage  
REF.: [nano &ndash; Text editor](https://www.nano-editor.org/) Homepage  
REF.: [Git - git-mergetool Documentation](https://git-scm.com/docs/git-mergetool)  
REF.: [Git - git-difftool Documentation](https://git-scm.com/docs/git-difftool)  

----

## Make VS Code your Default Editor

```bash
git config --global core.editor 'code --wait'
# or
git config --global core.editor 'code --wait --new-window'
# skip '--global' to use for current project only
```

_or_

- Type `git config --global -e` to open in editor, and add following lines:

  ```ini
  [core]
    editor = code --wait  # --new-window
  ```

## Reset to Default Editor

```bash
git config --global --unset core.editor
# default is Nano
```

## Make VS Code your Default Diff Tool

```bash
git config --global diff.tool vscode
git config --global difftool.vscode.cmd 'code --wait --diff $LOCAL $REMOTE'
```

_or_

- Type `git config --global -e` to open in editor, and add following lines:

  ```ini
  [diff]
    tool = vscode
  [difftool "vscode"]
    cmd = code --wait --diff $LOCAL $REMOTE
  ```

## Making VS Code your Default Merge Tool

```bash
git config --global merge.tool vscode
git config --global mergetool.vscode.cmd 'code --wait $MERGED'
git config --global mergetool.vscode.trustExitCode true
```

_or_

- Type `git config --global -e` to open in editor, and add following lines:

  ```ini
  [merge]
    tool = vscode
  [mergetool "vscode"]
    cmd = code --wait $MERGED
    trustExitCode = true
  ```
