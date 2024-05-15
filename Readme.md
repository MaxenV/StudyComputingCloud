docker scout cves maxenv/server-image:lab8_c
docker scout quickview maxenv/server-image:lab8_c
docker buildx build -f Dockerfile_classic -t maxenv/server-image:lab8_c --sbom=true --provenance=mode=max --push .
