# VXL Official Package Repository 📦

> The official collection of powerful scripts and libraries for the Voxel Language ecosystem.

[![Vxl](https://img.shields.io/badge/Vxl-tool-brightgreen?style=for-the-badge)](https://github.com/Intelektika-team/vxl)
[![Voxel Lang](https://img.shields.io/badge/Voxel-Lang-orange?style=for-the-badge)](https://github.com/Intelektika-team/Voxel)
[![Version](https://img.shields.io/badge/Version-0.7.2-blue?style=for-the-badge)](#)
[![Join](https://img.shields.io/badge/Join-us-red?style=for-the-badge)](https://intelektika-team.github.io/)
[![Team](https://img.shields.io/badge/Our-team-yellow?style=for-the-badge)](https://github.com/Intelektika-team)

This repository is the central hub for extending your Voxel projects. Here you'll find a growing collection of scripts and libraries designed to seamlessly integrate with the `vxl` package manager, adding new capabilities and simplifying your development process.

## ✨ What's Inside?

This repo contains **exclusively** `.py` scripts designed to be used as dependencies in Voxel projects. These can include:
- **Libraries:** Additional functions and utilities for math, strings, data structures, etc.
- **Modules:** Pre-built solutions for common tasks (e.g., working with files, networks).
- **Tools:** Scripts that enhance the VXL CLI itself.

## 🚀 Quick Start

1.  **Ensure you have a Voxel project.** If you don't have one, create it:
    ```bash
    vxl -n my_awesome_project
    cd my_awesome_project
    ```

2.  **Install a package from this repo.** For example, to install a script called `http_utils`:
    ```bash
    vxl -i http_utils
    ```
    This command will download `http_utils.py` from this repository and place it in your project's `_voxel_/_dependencies_/` folder.

3.  **Use it in your Voxel code!** Import it inside a `pyl` command or a Python-line block:
    ```voxel
    @include= tape
    @include= stdio
    @import=hhtp_utils, http;

    :voxel-fetch_data-{
        pyl= data //- http.get("https://api.example.com/data") /:
        pyl= print(data) /:
    };

    use= fetch_data
    ```

## 🔧 Advanced Usage: Installing from Any GitHub Repo

The `vxl` tool is not limited to this repo. You can install scripts from any public GitHub repository!

```bash
# Syntax: vxl -if <github_user/repo_name> <script_name>
vxl -if someuser/cool-vxl-scripts awesome_module
```
This command will download `awesome_module.py` from `https://github.com/someuser/scripts/cool-vxl-scripts`.

## 🤝 How to Contribute Your Package

We welcome contributions! To add your awesome script to the official repository:

1.  **Fork** this repository.
2.  **Add your `.py` script** to the root of the `scripts/` directory.
3.  **Test it thoroughly.**
4.  **Submit a Pull Request** with a description of what your script does and how to use it.

Please ensure your code is well-commented and follows general Python best practices.
