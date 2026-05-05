`git config feature.manyFiles true`

By using this configuration option , you can inform Git that it is managing a large repository. This setting will enable a newer index file version that is smaller in size and thus gets rewritten faster after modifying files in the index. It will also enable an untracked files cache.



---
`git config core.fsmonitor true`

A daemon to watch the working directory for file and directory changes using platform-specific filesystem notification facilities.
Available only on a limited set of supported platforms. Currently, this includes Windows and MacOS.


---
`git maintenance start`

Run tasks to optimize Git repository data, speeding up other Git commands and reducing storage requirements for the repository.
