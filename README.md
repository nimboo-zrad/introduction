# NPM(node package manager): 
is a package manager for the JavaScript programming language. It's the default package manager for Node.js and is used to install, update, and manage dependencies of JavaScript packages. think of it as a library where you can find pre-written code modules (packages) that developers can easily incorporate into their projects.

> Remember You don’t need to write all the code from scratch & using others’ code and existing modules is a smart way to build your projects.

**Before installing any packages, we should cover these key concepts:**
  **1. What is package.json:**  The package.json file is a core component of Node.js projects. It's a JSON file that acts as a manifest, storing metadata about the project and its dependencies. This file is crucial for managing and distributing Node.js packages, as well as for streamlining development workflows.  

  **2. What is package-lock.json:**  is automatically generated for any operations where npm modifies either the node_modules tree, or package. json . It describes the exact tree that was generated, such that subsequent installs are able to generate identical trees, regardless of intermediate dependency updates.

## Installation ways! 
There are several ways to install packages, but the most practical methods are local, global, and developer dependency installations.

| Installation Type               | Command Example                          | Saves to `package.json` |
|----------------------------------|-----------------------------------------|-------------------------|
| Local                            | `npm install lodash`                    | `dependencies`          |
| Global                           | `npm install -g nodemon`                | No                      |
| Dev Dependency                   | `npm install -D jest`                   | `devDependencies`       |
| Optional Dependency              | `npm install -O fsevents`               | `optionalDependencies`  |
| Exact Version                    | `npm install -E react@18.2.0`           | Exact version           |
| From `package.json`              | `npm install`                           | N/A                     |
| From GitHub                      | `npm install git+https://...`           | Yes (if `--save` used)  |
| Dry Run                          | `npm install --dry-run`                 | No                      |
| Forced Reinstall                 | `npm install --force`                   | Depends on flags        |
| Without Modifying `package.json` | `npm install --no-save axios`           | No                      |

> Install global packages (npm install -g) for tools you use across projects. For project-specific tools, use dev dependencies (npm install -D). Note: global packages don't appear in package.json, while dev dependencies are listed separately under "devDependencies".
> 
> If you want to install a specific package from github:  `npm install git+https://github.com/username/repository.git`  and if you want to install from a compressed tarball:  `npm install https://example.com/path/to/package.tgz`
>
> If you have a package.json file already and want to install the listed packages just run `npm install`

## Other package managers:
  1. Yarn:  
    Developed by: Facebook (now community-led)  
    Advantages:  
    - Faster than npm (uses a caching system)  
    - Deterministic dependency resolution with yarn.lock  
    - Workspaces for monorepos  
    - Plug'n'Play (zero-install) mode  

  2. PNPM:  
    Standout Feature: Disk-space efficiency (hard links to avoid duplicate packages)  
    Advantages:  
    - Faster installs than npm/Yarn  
    - Strict dependency isolation (prevents "phantom dependencies")  
    - Compatible with npm/Yarn workflows  

  3. Bun:  
    It includes Package manager, runtime, bundler, and test runner  
    The most significant advantage is its exceptional speed, because it's sritten in Zig!  