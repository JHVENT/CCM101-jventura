# Mission 5 Reflection

Object storage is better suited for millions of photos because it stores each photo as a self-contained object with a unique ID and metadata in a flat structure. A traditional block storage drive stores raw blocks that a file system organizes into folders, so it is limited by the capacity of one disk and by file system overhead, and it becomes slow and hard to manage as files pile up. Object storage scales out by adding more nodes and is reached through an API, which makes it cheaper and easier to grow.

Docker made deploying MinIO much easier because I did not have to install dependencies or configure the server by hand. The image already packages MinIO with everything it needs, so a single `docker run` command with the right ports and credentials started the server.

A bucket is the top-level container in cloud storage that holds objects. It works like a folder but is flat, with a unique name and its own access rules. Every object I uploaded had to live inside a bucket.

I think large enterprises keep their data safe through replication and erasure coding. Copies or coded fragments of each object are spread across many drives and servers. If a physical server crashes, the system rebuilds the missing pieces from the remaining ones, and background health checks repair damaged data, so users usually do not notice the failure.

My confidence in the Linux command line is growing steadily. At first the commands felt intimidating and easy to mistype. By repeating commands like `docker run`, `docker ps`, and `docker logs`, and by reading error messages carefully, I learned to troubleshoot instead of panicking. Fixing the failed image pull, where I had to switch to a different image, taught me that errors are clues, not roadblocks. I now feel comfortable navigating, running, and checking things in the terminal.

## Sources
[1] MinIO. *Erasure Coding 101.* https://www.min.io/blog/erasure-coding. Accessed September 28, 2026.
[2] MinIO. *Erasure Coding* (documentation). https://min.io/docs/minio/linux/operations/concepts/erasure-coding.html. Accessed September 28, 2026.
