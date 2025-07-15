<h1 align="center">
  <br>
  <a href="http://github.com/elbrodelche"><img src="/assets/vscode-tips.png" alt="Smooth Visual Studio Tips" width="250"></a>
  <br>
Smooth Visual Studio Tips
  <br>
</h1>
<div align="center">
  :rocket:
</div>
<div align="center">
  Best modules, config and <code>shortcuts</code>
</div>

<br />

<div align="center">
  <sub>Shred by
  <a href="">
  Juan Carlos Migliavacca
  </a>
</div>

## Table of Contents

- [Shortcuts](#shortcuts)
- [Configs](#configs)
- [Tips](#tips)
- [Useful Extensions](#useful-extensions)

## Shortcuts

### Standard Shortcuts

| Key Combination        | Action                                                  |
| ---------------------- | ------------------------------------------------------- |
| CMD B                  | Open/Close the sidebar                                  |
| CMD P                  | Open/Close the file switcher                            |
| CMD SHIFT P            | Open/Close the command palette                          |
| CMD + `                | Open/Close the terminal                                 |
| CMD + J                | Open/Close the panel                                    |
| OPT + DOWN + ,         | Move Line                                               |
| OPT + SHIFT + DOWN + , | Duplicate Line                                          |
| OPT + CMD + K + ,      | Duplicate Line                                          |
| CMD + -                | Navigate back                                           |
| CMD + SHIFT + -        | Navigate forward                                        |
| CMD + /                | Comment line                                            |
| CMD + SHIFT + L        | Add multiple cursors on every selected match            |
| CMD + D                | Add multiple cursors at a time (for skip, use CMD + K ) |
| OPT + ENTER            | Add multiple cursors when using find box                |
| CMD + P + P            | Switch file                                             |
| CMD + 0                | Switch to sidebar                                       |
| CMD + 1                | Switch editor                                           |
| CMD .                  | Expand bulb options                                     |
| CMD SHIFT B            | Build process                                           |

## Configs

### Disable Minimap

1. Open Command Palette ( CMD + SHIFT + P on macOS, CTRL + SHIFT + P on Windows/Linux).
2. Type Preferences: Open Settings (UI) and select it.
3. Search for "Minimap" in the search bar.
4. Uncheck the checkbox for "Editor: Minimap" to disable the minimap.

### Toggle Primary Sidebar Position

1. Open Command Palette.
2. Type View: Toggle Side Bar Position and select it to toggle the sidebar position between left and right.

### Disable Open Editors Visible

1. Go to Settings UI as before.
2. Search for "Open Editors".
3. Uncheck the checkbox for "Explorer: Open Editors Visible" to hide the Open Editors pane in the sidebar.

### Add OPT + CMD + , to Open Normal UI (Settings UI uses AI)

To create a custom keyboard shortcut for opening the Settings UI:

1. Open Command Palette.
2. Type Preferences: Open Keyboard Shortcuts (JSON) and select it.
3. Add the following JSON object to your keybindings file:
   ```json
   {
     "key": "opt+cmd+,",
     "command": "workbench.action.openSettings",
     "when": "settingsEditor:useSplitJSON !== true"
   }
   ```
4. Save the file.

## Tips

### Search

When using the file switcher:

```
@ symbol browser
@: group symbols
#: search across files for symbol
```

You can use the VS CODE type check withot configure TS
` "js/ts.implicitProjectConfig.checkJs": true`

Logpoints
Console log statements from the editor

exclude files from the editor

```json
files.exclude
```

### Region folding

This will collapse all the code between these tags

```
// # region Description
// # endregion
```

### Launch config

Use launch config for debugging

Debugger auto-attach
`node --inspect index.js`

## Useful Extensions

### How to Manage Extensions

**View All Extensions:**

- Press `CMD + SHIFT + X` to open Extensions view
- Use Command Palette: `CMD + SHIFT + P` → "Extensions: Show Installed Extensions"

**List via Terminal:**

```bash
# List all installed extensions
code --list-extensions

# List with versions
code --list-extensions --show-versions
```

### 🎨 **Themes & UI Enhancement**

| Extension           | ID                           | Description                                  |
| ------------------- | ---------------------------- | -------------------------------------------- |
| Material Icon Theme | `pkief.material-icon-theme`  | Beautiful file and folder icons              |
| Peacock             | `johnpapa.vscode-peacock`    | Color your workspace for easy identification |
| Power Mode          | `hoovercj.vscode-power-mode` | Add visual effects while typing              |
| Indent Rainbow      | `oderwat.indent-rainbow`     | Colorize indentation levels                  |
| VS Code Pets        | `tonybaloney.vscode-pets`    | Add cute pets to your editor                 |

### 🤖 **AI & IntelliSense**

| Extension                      | ID                                                    | Description                  |
| ------------------------------ | ----------------------------------------------------- | ---------------------------- |
| GitHub Copilot                 | `github.copilot`                                      | AI-powered code completion   |
| GitHub Copilot Chat            | `github.copilot-chat`                                 | AI chat assistant for coding |
| IntelliCode                    | `visualstudioexptteam.vscodeintellicode`              | AI-assisted development      |
| IntelliCode API Usage Examples | `visualstudioexptteam.intellicode-api-usage-examples` | API usage examples           |
| Windows AI Studio              | `ms-windows-ai-studio.windows-ai-studio`              | AI development tools         |

### 🔧 **Code Quality & Formatting**

| Extension                | ID                               | Description                         |
| ------------------------ | -------------------------------- | ----------------------------------- |
| ESLint                   | `dbaeumer.vscode-eslint`         | JavaScript/TypeScript linting       |
| Prettier                 | `esbenp.prettier-vscode`         | Code formatter                      |
| EditorConfig             | `editorconfig.editorconfig`      | Maintain consistent coding styles   |
| Markdown Lint            | `davidanson.vscode-markdownlint` | Markdown linting and style checking |
| Pretty TypeScript Errors | `yoavbls.pretty-ts-errors`       | Better TypeScript error messages    |

### 🌐 **Web Development**

| Extension                 | ID                               | Description                              |
| ------------------------- | -------------------------------- | ---------------------------------------- |
| Tailwind CSS IntelliSense | `bradlc.vscode-tailwindcss`      | Tailwind CSS autocomplete                |
| Auto Rename Tag           | `formulahendry.auto-rename-tag`  | Automatically rename paired HTML tags    |
| Live Server               | `ritwickdey.liveserver`          | Launch local development server          |
| REST Client               | `humao.rest-client`              | Send HTTP requests directly from VS Code |
| Toggle Quotes             | `britesnow.vscode-toggle-quotes` | Switch between quote styles              |

### 📦 **Package Management**

| Extension            | ID                                   | Description                       |
| -------------------- | ------------------------------------ | --------------------------------- |
| npm Intellisense     | `christian-kohler.npm-intellisense`  | Autocomplete npm modules          |
| Version Lens         | `pflannery.vscode-versionlens`       | Show package version information  |
| Import Cost          | `wix.vscode-import-cost`             | Display size of imported packages |
| npm Dependency Links | `herrmannplatz.npm-dependency-links` | Navigate to npm package pages     |
| npm Dependency       | `howardzuo.vscode-npm-dependency`    | Manage npm dependencies           |

### 🐳 **DevOps & Cloud**

| Extension           | ID                                     | Description               |
| ------------------- | -------------------------------------- | ------------------------- |
| Docker              | `docker.docker`                        | Docker support            |
| Remote - Containers | `ms-vscode-remote.remote-containers`   | Develop inside containers |
| AWS Toolkit         | `amazonwebservices.aws-toolkit-vscode` | AWS development tools     |

### 📊 **Data & Files**

| Extension    | ID                        | Description                      |
| ------------ | ------------------------- | -------------------------------- |
| Rainbow CSV  | `mechatroner.rainbow-csv` | Highlight CSV columns            |
| SQL Notebook | `cmoog.sqlnotebook`       | SQL query notebooks              |
| YAML         | `redhat.vscode-yaml`      | YAML language support            |
| File Size    | `mkxml.vscode-filesize`   | Display file sizes in status bar |
| PDF          | `tomoki1207.pdf`          | View PDF files                   |

### 🔄 **Git & Version Control**

| Extension   | ID                           | Description                           |
| ----------- | ---------------------------- | ------------------------------------- |
| GitLens     | `eamodio.gitlens`            | Supercharge Git capabilities          |
| Git History | `donjayamanne.githistory`    | View git log and file history         |
| Git Graph   | `mhutchie.git-graph`         | View repository git graph             |
| Live Share  | `ms-vsliveshare.vsliveshare` | Real-time collaborative development   |
| gitignore   | `codezombiech.gitignore`     | Language support for .gitignore files |

### 🛠️ **Productivity & Utilities**

| Extension         | ID                                   | Description                      |
| ----------------- | ------------------------------------ | -------------------------------- |
| Bookmarks         | `alefragnani.bookmarks`              | Mark lines and jump between them |
| TODO Tree         | `gruntfuggly.todo-tree`              | Show TODO comments in tree view  |
| TODO Highlight    | `wayou.vscode-todo-highlight`        | Highlight TODO comments          |
| Turbo Console Log | `chakrounanas.turbo-console-log`     | Automate console.log statements  |
| Path Intellisense | `christian-kohler.path-intellisense` | Autocomplete filenames           |
| ScratchPads       | `buenon.scratchpads`                 | Quick note-taking                |
| Multi Command     | `ryuta46.multi-command`              | Execute multiple commands        |

### 🔍 **Code Analysis & Comparison**

| Extension      | ID                                    | Description                   |
| -------------- | ------------------------------------- | ----------------------------- |
| Partial Diff   | `ryu1kn.partial-diff`                 | Compare text selections       |
| Diff & Merge   | `moshfeu.diff-merge`                  | Advanced diff and merge tools |
| Annotator      | `ryu1kn.annotator`                    | Add annotations to code       |
| Gutter Preview | `kisstkondoros.vscode-gutter-preview` | Preview images in gutter      |
| Paste Image    | `mushan.vscode-paste-image`           | Paste images from clipboard   |

### 🎯 **Development Tools**

| Extension      | ID                        | Description                    |
| -------------- | ------------------------- | ------------------------------ |
| Quokka.js      | `wallabyjs.quokka-vscode` | Live JavaScript scratchpad     |
| Regex Snippets | `monish.regexsnippets`    | Regular expression snippets    |
| Reveal         | `smulyono.reveal`         | Reveal file in OS file manager |
| Footsteps      | `wattenberger.footsteps`  | Show where you've been in code |
| Share Snippet  | `aleg94.share-snippet`    | Share code snippets            |

### 📄 **Document Generation**

| Extension    | ID                   | Description             |
| ------------ | -------------------- | ----------------------- |
| Markdown PDF | `yzane.markdown-pdf` | Convert Markdown to PDF |

### Installation Tips

**Install Multiple Extensions:**

```bash
# Install all essential extensions at once
code --install-extension pkief.material-icon-theme \
     --install-extension github.copilot \
     --install-extension esbenp.prettier-vscode \
     --install-extension dbaeumer.vscode-eslint \
     --install-extension eamodio.gitlens
```

**Export Your Extensions:**

```bash
# Create a list of your installed extensions
code --list-extensions > my-extensions.txt
```

**Install from List:**

```bash
# Install extensions from a file
cat my-extensions.txt | xargs -L 1 code --install-extension
```
