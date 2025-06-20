# VPN access via Netbird

## Setup

1. Ensure you have Docker and Git
2. clone this repo: `git clone https://github.com/runchise/vpn.git && cd vpn`
3. run `bin/install` and wait until Docker build finished
4. set `NB_SETUP_KEY` in `.env` file.

## Usage

Run `docker compose up -d` to start the services, and  `docker compose stop` to stop them.

### Port Forwarding

For port forwarding via ssh, e.g.
to access remote server, e.g. `http://dev-server.netbird.cloud`:

1. `bin/port-forward dev-server.netbird.cloud 8080:80`
2. in other terminal, test the connectivity: `curl http://localhost:8080`

### SOCKS Proxy (recommended)

Alternatively use SOCKS5 proxy (`localhost:1080`) so that you can
access remote servers using their proper URLs.

Useful links:

* [Enter proxy server settings on Mac](https://support.apple.com/en-eg/guide/mac-help/mchlp25912/15.0/mac/15.0)
* [Connection settings in Firefox](https://support.mozilla.org/en-US/kb/connection-settings-firefox)
* [Configuring a SOCKS proxy server in Chrome](https://www.chromium.org/developers/design-documents/network-stack/socks-proxy/)
* [How to Use cURL With Proxy?](https://oxylabs.io/blog/curl-with-proxy)