# MiLuAssistantWeb

MiLuAssistantWeb is a web-based personal AI assistant adapted from the CoPaw / QwenPaw project line. This repository keeps the original multi-channel assistant, skills, model provider, workspace, memory, and security concepts, while rebranding and adapting the application into the MiLu web edition.

## Positioning

- **Upstream basis**: CoPaw / QwenPaw by AgentScope.
- **Project role**: Web edition of the MiLu assistant project.
- **Follow-up package**: [MiLuAssistantDesktop](https://github.com/White-147/MiLuAssistantDesktop), the Windows desktop installer version based on this web edition.
- **Main scenario**: Local or self-hosted AI assistant with configurable models, skills, channels, files, memory, and scheduled tasks.

## Main Changes

- Renamed the Python package, CLI entry, runtime namespace, working directory, and environment variables from the original assistant project to `milu`.
- Replaced web console branding assets with MiLu-related icons and product naming.
- Added MiLu-specific local provider configuration and workspace defaults.
- Cleaned runtime data, user workspaces, and private custom configuration before publishing.
- Prepared this web edition as the base project for the later Windows desktop installer.

## Tech Stack

- **Backend**: Python, FastAPI / Uvicorn, AgentScope, AgentScope Runtime.
- **Frontend**: React, TypeScript, Vite, Ant Design.
- **AI capabilities**: model provider configuration, skills, memory, multi-agent collaboration, MCP tools, browser/file/Office/PDF-related skills.
- **Deployment**: local Python runtime, web console, optional Docker-based deployment inherited from the upstream project.

## Local Development

```powershell
cd D:\code\MiLuAssistantWeb
pip install -e .
milu init --defaults
milu app
```

Then open:

```text
http://127.0.0.1:8088/
```

## Relationship With MiLuAssistantDesktop

This repository provides the web application and Python backend. The desktop installer repository packages this project into an Electron / NSIS Windows application, starts the Python backend locally, loads the web UI in a native window, and isolates user data under the Windows local app data directory.

## License

This project keeps the Apache License 2.0 inherited from the upstream CoPaw / QwenPaw project line. See [LICENSE](LICENSE).
