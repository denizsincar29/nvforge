# NVForge
a package manager and build system for Non-Visual Game Toolkit

## features
- create new projects (nvforge new <project-name>)
- build projects (nvforge build [--release])
- run projects (nvforge run)
- install packages (nvforge add <git_url>
- remove packages (nvforge remove <package-name>) ...

The package manager is based on git, so you can use any git repository as a package source.
The package structure looks like this:
```
package-name
  - package.json
  - src
    - main.nvgt
  - include
    - package-name.nvgt
  - target
    - debug
      - package-name.exe (or app or whatever platform specific)
    - release
      - package-name.exe or whatever

```

package.json:
```json
{
  "name": "package-name",
  "version": "0.1.0",
  "description": "A package for NVGT",
  "dependencies": [
    "https://github.com/username/package-name",
    ...
  ]
```

