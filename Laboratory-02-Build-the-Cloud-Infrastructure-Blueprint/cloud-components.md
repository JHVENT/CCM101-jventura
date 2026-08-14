Cloud Infrastructure Components

Compute Resources

Compute is just the raw processing power of a machine, its CPU and RAM, and it's really the whole point of renting a cloud server in the first place. You're not paying for a box sitting in a data center, you're paying for the ability to run your app or website without owning that hardware yourself. What makes cloud compute actually useful is that you can scale it up or down on demand instead of being stuck with whatever you bought.

On the KillerCoda machine, I checked this with lscpu for the CPU model and core count, and free -h for the RAM. Even though it's a small single VM, it's functioning exactly like a scaled-down version of an AWS EC2 instance or an Azure VM. Same idea, just smaller.

Storage Resources

Storage is where everything actually lives, files, the OS itself, logs, whatever data the system needs to keep around after it's powered off. This matters a lot in the cloud because businesses need somewhere reliable to keep their data, and they need to be able to grow that storage without buying new physical drives every time they run out of space.

Running df -h on the KillerCoda VM showed a 19G disk on /dev/vda1, split across mount points like /, /boot, and /boot/efi. That's basically a miniature version of how real cloud storage gets partitioned and allocated.

Networking Resources

Networking is what connects a machine to everything else, other servers, the internet, users trying to reach it. Without it, a cloud server is just an isolated machine nobody can actually use. This is what makes remote access possible and lets different services talk to each other, which is the backbone of basically every cloud app.

I found the hostname and IP address using hostname and hostname -I. These are how this VM gets identified on a network, which is the same logic cloud providers use to assign network identities to every VM they spin up.

Operating System

The OS is the layer that manages all the hardware underneath it and gives every other piece of software a place to run. In cloud computing, the OS you pick affects what software is compatible, how security patches get handled, and how efficiently the hardware actually gets used, which is why most providers let you choose your OS image when you launch something.

cat /etc/os-release and uname -r showed this machine is running Ubuntu 24.04 LTS with a specific kernel version. That's the foundation everything else, compute, storage, networking, is actually built on top of.
