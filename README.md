# rsync-backup-operator
Kubernetes Operator that provides access to Persistent Volume snapshots via rsync+ssh.

**Important:** This project is nowhere near a state that it should be considered for any sort of
productive application. There is no timeline as of yet and especially progress may be slow.

## Vision
As a cluster administrator, I want to transparently back up my Persistent Volumes
using an rsync+ssh client (e.g. via [BackupPC](https://backuppc.github.io/backuppc/))
and a storage provider with snapshot support configured.

There is no intention to provide any sort of backup functionality in the application itself.

I want to be able to configure which PVCs are eligible for backup and how long snapshots
are retained until they are cleaned up. Once a client connects, a snapshot is taken
(how?), mounted (how?), and served.

