Mod to extract a Traefik certificate to use it with [ZNC](https://github.com/linuxserver/docker-znc).

Env vars:

- `CERT_DIR`: directory where Traefik stores its certificates JSON.
- `CERT_RESOLVER`: cert resolver as found inside the JSON.
- `MAIN_DOMAIN`: main domain from the JSON certificate that shall be extracted.
- `OUTPUT_DIR`: directory where the cert and key pair will be stored.

The output files under `OUTPUT_DIR` will be `cert.pem` and `key.pem`

Note that ZNC [reloads certs on every client connection](https://github.com/znc/znc/issues/1215).
