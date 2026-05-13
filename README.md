# MTCode RemoteGPU

Run Python projects on remote GPU servers directly from VS Code — upload files, execute scripts, and download results, all from a sidebar panel in your editor.

> **Get started at [mtcodeai.com](https://mtcodeai.com/platform/gpu-server.html)** — download the MTCode GPU Server program to share your GPU resources without exposing your whole computer. Unlike conventional SSH login that gives access to the entire system, MTCode GPU Server runs each authorized user's Python scripts in a sandbox: file system access is restricted to designated directories and dangerous system operations are blocked, protecting your machine from malicious or accidental harm.

## Features

- **Remote GPU Access** — connect to GPU servers shared through the [MTCode DirectLink Platform](https://mtcodeai.com/platform/index.html)
- **Project Upload & Sync** — smart upload with file change detection; only new or modified files are transferred
- **Online Execution** — run scripts and stream output in real time to the VS Code OUTPUT console
- **Offline Execution** — submit jobs that run independently on the server; disconnect and retrieve results later
- **Project Output & Downloads** — browse and download output files; multi-select with Shift/Ctrl + click
- **Dataset Management** — upload your own datasets or reference shared server datasets using `${env:dataset-1}` variables
- **Python Interpreter Selection** — choose from system Python, Conda, or virtual environments on the server
- **Package Management** — install, remove, and list Python packages on the server without SSH
- **Security** — credentials encrypted via VS Code Secrets API; all data transmitted over an encrypted connection; server-side sandboxing for script execution

## Getting Started

1. **Install** — install MTCode RemoteGPU from the VS Code Marketplace
2. **Log in** — click the Login button and enter your credentials. Access is by invitation: the administrator who registered the GPU server sends you an invitation email — follow the link to create your account before signing in.
3. **Select a GPU server** — the "GPU servers" dropdown lists available servers; selecting one auto-connects and shows server info
4. **Upload & run** — load a project folder, configure a task, upload files, and click "Start Execution"
5. **Learn more** — see documentation at [mtcodeai.com/platform/remote-gpu.html](https://mtcodeai.com/platform/remote-gpu.html)

## The GPU Control Panel

The sidebar is divided into a **server area** and a **project area**:

### Server Area
- **GPU servers** — refresh and select from available servers (account, computer, GPU model)
- **Server info** — view detailed specs including CPU, RAM, GPU, and VRAM
- **GPU / Disk utilization** — monitor GPU usage and your disk quota

### Project Area (3 Tabs)
- **Project Content** — file tree with sync status, upload controls, and task configuration
- **Project Output** — browse and download output files from the server
- **User Directory** — manage all your files on the server

## Task Configuration

- Select an active task or create a new one
- Choose an entry-point Python script and set command-line arguments
- Reference server datasets with `${env:dataset-1}`, `${env:dataset-2}`, `${env:dataset-3}`
- Select a Python interpreter and save configuration to `.vscode/launch.json`

## Execution Modes

| Mode | Description |
|------|-------------|
| **Online** | Real-time output in the OUTPUT console. Stops if you disconnect. |
| **Offline** | Runs on the server independently. Output saved to `*_output.log`. |

## License

See LICENSE.txt
