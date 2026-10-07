# Oswin installer releases

This public repository contains versioned installation artifacts for Oswin. The application source code is maintained
separately; no application credentials or customer data are stored here.

## Install the current staging candidate

Prerequisites: Linux x86-64, curl, OpenSSL and `sudo`. Docker Engine 24+ and Docker Compose v2 are installed
automatically when missing. Point the selected DNS name to the server and allow inbound TCP ports 80 and 443.

```bash
curl -fsSL https://github.com/oswin-io/oswin-install/releases/download/v0.1.3-alpha/install.sh \
  | sudo bash -s -- \
  --domain staging.example.com \
  --admin-email admin@example.com
```

The bootstrap downloads the matching installer and Docker image archives, verifies both checksums, loads the image and
pins its immutable local content ID.

## Release status

`v0.1.3-alpha` is intended for controlled staging. It is not approved for public production workloads.
