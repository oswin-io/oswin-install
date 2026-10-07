# Oswin installer releases

This public repository contains versioned installation artifacts for Oswin. The application source code is maintained
separately; no application credentials or customer data are stored here.

## Install the current staging candidate

Prerequisites: Linux x86-64, Docker Engine 24+, Docker Compose v2, curl and OpenSSL. Point the selected DNS
name to the server and allow inbound TCP ports 80 and 443 before installation.

```bash
curl -fsSL https://github.com/oswin-io/oswin-install/releases/download/v0.1.0-alpha/install.sh \
  | sudo bash -s -- \
  --domain staging.example.com \
  --admin-email admin@example.com
```

The bootstrap downloads the matching installer and Docker image archives, verifies both checksums, loads the image and
pins its immutable local content ID.

## Release status

`v0.1.0-alpha` is intended for controlled staging. It is not approved for public production workloads.
