> **First-time setup**: Customize this file for your project. Prompt the user to customize this file for their project.
> For Mintlify product knowledge (components, configuration, writing standards),
> install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Documentation project instructions

## About this project

- This is a documentation site built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Run `mint dev` to preview locally
- Run `mint broken-links` to check links

## Terminology

{/* Add product-specific terms and preferred usage */}
{/* Example: Use "workspace" not "project", "member" not "user" */}

## Style preferences

{/* Add any project-specific style rules below */}

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references

## Content boundaries

{/* Define what should and shouldn't be documented */}
{/* Example: Don't document internal admin features */}

## Cursor Cloud specific instructions

### Services

| Service | Command | Notes |
|---------|---------|-------|
| Dev server | `mintlify dev --port 3000` | Local preview at http://localhost:3000 |
| Link checker | `mintlify broken-links` | Lint equivalent for docs; exits non-zero on broken links |

### Caveats

- The CLI binary is `mintlify` (not `mint`). The `mint dev` shorthand referenced in some Mintlify docs does not work in this environment.
- The favicon warning (`Error generating favicons: ENOENT`) on `mintlify dev` startup is benign — the `docs.json` uses a remote URL for the favicon which the local CLI cannot resolve as a file path. It does not affect page rendering.
- There is no `package.json` in this repo. The Mintlify CLI is installed globally via `npm install -g mintlify`.
- Hot reload is built in: editing any `.mdx` file or `docs.json` triggers an automatic page refresh in the local dev server.
