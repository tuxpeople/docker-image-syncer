> [!IMPORTANT]
> **This image is no longer maintained** and this repository is archived. The last image (`v1.5.4`, 2024-05) stays available but gets no updates.
>
> Alternatives: the [upstream release binaries](https://github.com/AliyunContainerService/image-syncer/releases) of image-syncer, or other registry sync tools such as [`skopeo sync`](https://github.com/containers/skopeo), [regsync](https://github.com/regclient/regclient) or `crane copy` from [go-containerregistry](https://github.com/google/go-containerregistry).

# image-syncer

This is my container image of https://github.com/AliyunContainerService/image-syncer

`image-syncer` is a docker registry tools. With `image-syncer` you can synchronize docker images from some source registries to target registries, which include most popular public docker registry services.

## Features

- Support for many-to-many registry synchronization
- Supports docker registry services based on Docker Registry V2 (e.g., Alibaba Cloud Container Registry Service, Docker Hub, Quay.io, Harbor, etc.)
- Network & Memory Only, doesn't rely on any large disk storage, fast synchronization
- Incremental Synchronization, ignore unchanged images automatically
- BloB-Level Concurrent Synchronization, adjustable goroutine numbers
- Automatic Retries of Failed Sync Tasks, to resolve the network problems (rate limit, etc.) while synchronizing
- Doesn't rely on Docker daemon or other programs