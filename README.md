# obsidian-plugin-skill

An [agent skill](https://agentskills.io/specification) for building Obsidian plugins using TypeScript and the Obsidian API.

## What is this?

This skill provides AI coding agents with comprehensive knowledge of Obsidian plugin development — project structure, build configuration, API patterns, UI components, security rules, and release workflows.

## Usage

Copy the `obsidian-plugin/` directory into your project's `.github/skills/` directory (or wherever your agent discovers skills):

```bash
# Clone into your project
git clone https://github.com/raykao/obsidian-plugin-skill.git /tmp/obsidian-plugin-skill
cp -r /tmp/obsidian-plugin-skill/obsidian-plugin/ .github/skills/obsidian-plugin/
```

Or add as a git submodule:

```bash
git submodule add https://github.com/raykao/obsidian-plugin-skill.git .github/skills/obsidian-plugin-skill
```

## Skill Contents

```
obsidian-plugin/
├── SKILL.md                      # Core instructions (agentskills.io format)
└── references/
    └── API-REFERENCE.md           # Condensed Obsidian TypeScript API surface
```

### SKILL.md covers:
- Project structure & build system (esbuild, TypeScript, CJS output)
- `manifest.json`, `package.json`, `tsconfig.json` templates
- Plugin lifecycle (`onload` / `onunload`)
- UI components: Views, Commands, Settings, Modals, Ribbon, Status Bar, Context Menus
- Vault API (file CRUD, frontmatter, metadata)
- Events and resource management
- Editor extensions (CodeMirror 6)
- HTML/CSS rules (security, theming, Obsidian CSS variables)
- Release and distribution checklist

### API-REFERENCE.md covers:
- Core classes: `Plugin`, `App`, `Vault`, `Workspace`, `Editor`
- View types: `ItemView`, `MarkdownView`, `Modal`, `SuggestModal`, `FuzzySuggestModal`
- UI: `Setting`, `Menu`, `MenuItem`
- File types: `TFile`, `TFolder`, `TAbstractFile`
- Utility functions: `normalizePath`, `addIcon`, `setIcon`, `requestUrl`, `MarkdownRenderer`
- CSS variables reference

## License

MIT
