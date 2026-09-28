# MinIO Deployment

## Overview
This document records how I deployed a MinIO S3-compatible object storage server using Docker in a KillerCoda Ubuntu Playground.

## Docker Command Used
```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
cgr.dev/chainguard/minio server /data --console-address ":9001"
```

**Note on the image:** The lab handout uses `minio/minio`, but pulling it failed with "pull access denied," and `quay.io/minio/minio` failed with "unauthorized." Both appear to have been removed or restricted in September 2026. I used `cgr.dev/chainguard/minio` instead, with the same ports, credentials, and flags.

## Web Console Port
The web console is accessed on port **9001**. Port 9000 is the S3 API port.

## Bucket Created
`client-photos`

## What the -e Flags Did
The `-e` flag sets an environment variable inside the container when it starts.
- `MINIO_ROOT_USER=cloudadmin` sets the administrator username for MinIO.
- `MINIO_ROOT_PASSWORD=CloudNova2026!` sets the administrator password.

These are the credentials I used to log in to the web console. Passing them as environment variables means the server is configured at startup without editing any config files.

## Steps Taken
1. Launched a KillerCoda Ubuntu Playground.
2. Ran the `docker run` command above to start the MinIO container.
3. Verified the container was running with `docker ps`.
4. Opened port 9001 through KillerCoda's Traffic / Ports menu.
5. Logged in with the credentials above.
6. Created the `client-photos` bucket and uploaded a test file.

## Screenshots
- `screenshots/minio-deployed.png`
- `screenshots/minio-bucket-upload.png`

## AI Disclosure
An AI assistant helped me troubleshoot the image pull errors and draft this documentation. I verified the steps against what I did.
