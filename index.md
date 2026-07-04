# git-lazy-mount documentation

New here? Start with the [project README](https://github.com/linyiru/git-lazy-mount/blob/138cebb4b0555ce1ebec906335fd900a4147c29a/README.md). It covers what this is, why it exists, and how to install it. Then pick a track below.

## Using it

- [Compatibility](/git-lazy-mount/compatibility.md): which `git` commands work through the mount, and how lazily they run.
- [Limitations](/git-lazy-mount/limitations.md): what's deferred or fundamentally constrained, and why.

## How it works

- [Architecture overview](/git-lazy-mount/architecture.md): the moving parts, end to end.
- [Worktree model](/git-lazy-mount/worktree-model.md): the read-only baseline plus the durable writable overlay.
- [Git state model](/git-lazy-mount/git-state-model.md): what stock git owns vs. what the mount synthesizes.
- [FUSE semantics](/git-lazy-mount/fuse-semantics.md): inodes, file handles, and the implemented operations.
- [Object fetching](/git-lazy-mount/object-fetching.md): materialization, single-flight coalescing, filters, and exact size/metadata.
- [Index & scalability](/git-lazy-mount/index-strategy.md): the real `.git/index` (`read-tree HEAD`) and scalability notes.
- [FSMonitor](/git-lazy-mount/fsmonitor.md): the durable change journal and the `core.fsmonitor` hook.
- [Startup & deadlock avoidance](/git-lazy-mount/deadlock-startup-recovery.md): the mount startup sequence and the FUSE/git deadlock invariants.
- [Durability & security](/git-lazy-mount/durability-security.md): overlay durability, auth/offline, and the threat model.

## Reference

- [Specification](/git-lazy-mount/design.md): the lean, authoritative design the implementation is built and tested against.
- [Other platforms](/git-lazy-mount/future-platforms/windows.md): the project is Linux-only. Notes on the Windows ([ProjFS](/git-lazy-mount/future-platforms/windows.md)) and macOS ([FSKit](/git-lazy-mount/future-platforms/macos.md), [on-device](/git-lazy-mount/future-platforms/macos-fskit-ondevice.md)) backends.
