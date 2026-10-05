# Ansys HFSS

> Runs Ansys HFSS through this assistant instead of you opening the Ansys application by hand — it simulates high-frequency electronics such as antennas and radio-frequency (RF) circuits. Needs Ansys HFSS installed and licensed on this computer; the first time you use it, point it at your Ansys install folder.

The bundle zip (**51.9 MB**) is stored in this repository at **`f6372850-0d92-4fcd-b42c-3c0d70c9a885.zip`**.

This repository is part of the **Forjinn-Desk** MCP bundle collection. An MCP bundle is a self-contained server that a host application launches and communicates with over the MCP (Model Context Protocol) protocol.

## Repo metadata

| Field | Value |
| --- | --- |
| Registry ID | `f6372850-0d92-4fcd-b42c-3c0d70c9a885` |
| Status in registry | active |
| Bundle size | 51.9 MB |
| Distribution | committed to this repo |

## Environment variables

| Variable | Value / note |
| --- | --- |
| `ANSYS_ROOT` | `C:\ANSYS\v252\ansys_inc` |

## MCP launch configuration

The host replaces `__INSTALL_DIR__` (install dir) and `__PYTHON__` (bundled Python) at runtime.

```json
{
  "command": "__PYTHON__",
  "args": [
    "server.py"
  ],
  "cwd": "__INSTALL_DIR__",
  "env": {
    "ANSYS_ROOT": "",
    "ANSYS_WORKDIR": "__INSTALL_DIR__",
    "AEDT_NO_GUI": "1"
  }
}
```


## Install / usage

1. Get the bundle:
   - download `f6372850-0d92-4fcd-b42c-3c0d70c9a885.zip` from this repo (Code → Download ZIP, or `git clone`).
2. Extract to your target installation directory (config paths expect contents at the install-dir root).
3. Set the environment variables listed above.
4. Launch using the MCP config JSON (or let a host client manage it automatically).

> Bundles may include vendored runtimes (bundled Python, Node, or native executables). Builds are Windows x64.
