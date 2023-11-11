# Docker Image Build and Push to GitHub Packages

## Build and Push Docker Image

```bash
# Build Docker Image
docker build -f Dockerfile -t ghcr.io/s-gulomov/pdp-python-3.11/pdp-python-3.11:$IMAGE_VERSION .

# Login to GitHub Container Registry
export CR_PAT=$YOUR_TOKEN
echo $CR_PAT | docker login ghcr.io -u trm-build-bot --password-stdin

# Push Docker Image
docker push ghcr.io/s-gulomov/pdp-python-3.11/pdp-python-3.11:$IMAGE_VERSION
