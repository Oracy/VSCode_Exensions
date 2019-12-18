# How to Export and Import VSCode extensions (Unix Terminal)

1. Export Extensions creating shell file.

    ```bash
    code --list-extensions | sed -e 's/^/code --install-extension /' > code_extensions.sh
    head code_extensions.sh
    ```

    **Expected result**

    ```bash
    code --install-extension aaron-bond.better-comments
    code --install-extension ahmadawais.shades-of-purple
    code --install-extension amandeepmittal.expressjs
    code --install-extension bierner.emojisense
    code --install-extension chenxsan.vscode-standardjs
    code --install-extension christian-kohler.npm-intellisense
    code --install-extension christian-kohler.path-intellisense
    code --install-extension CoenraadS.bracket-pair-colorizer
    code --install-extension DavidAnson.vscode-markdownlint
    code --install-extension dbaeumer.vscode-eslint
    ```

2. Import Extensions from shell file

    ```bash
    ./code_extensions.sh
    ```
