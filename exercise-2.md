# Updating Packages

You can choose to update a single package, multiple packages, or all packages at once. If any dependencies of the package (or packages) you update have updates available themselves, then they are updated too.

# Updating a Single Package

To update a single package, run the following command as root:

```
yum update package_name
```

For example, to update the udev package, type:

```
~]# yum update udev
Loaded plugins: langpacks, presto, refresh-packagekit
Updating Red Hat repositories.
INFO:rhsm-app.repolib:repos updated: 0
Setting up Update Process
Resolving Dependencies
--> Running transaction check
---> Package gdb.x86_64 0:7.2.90.20110411-34.fc15 will be updated
---> Package gdb.x86_64 0:7.2.90.20110429-36.fc15 will be an update
--> Finished Dependency Resolution

Dependencies Resolved

================================================================================
 Package     Arch         Version                          Repository      Size
================================================================================
Updating:
 gdb         x86_64       7.2.90.20110429-36.fc15          fedora         1.9 M

Transaction Summary
================================================================================
Upgrade       1 Package(s)

Total download size: 1.9 M
Is this ok [y/N]:
```