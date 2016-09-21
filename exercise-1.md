Exercise #1

You can see the live version of this content here:

https://docs.fedoraproject.org/en-US/Fedora/21/html/System_Administrators_Guide/ch-yum.html#sec-Checking_For_Updates


Checking For Updates
To see which installed packages on your system have updates available, use the following command:

yum check-update

For example:

~]# yum check-update
Loaded plugins: langpacks, presto, refresh-packagekit

PackageKit.x86_64                    0.6.14-2.fc15                 fedora
PackageKit-command-not-found.x86_64  0.6.14-2.fc15                 fedora
PackageKit-device-rebind.x86_64      0.6.14-2.fc15                 fedora
PackageKit-glib.x86_64               0.6.14-2.fc15                 fedora
PackageKit-gstreamer-plugin.x86_64   0.6.14-2.fc15                 fedora
PackageKit-gtk-module.x86_64         0.6.14-2.fc15                 fedora
PackageKit-gtk3-module.x86_64        0.6.14-2.fc15                 fedora
PackageKit-yum.x86_64                0.6.14-2.fc15                 fedora
PackageKit-yum-plugin.x86_64         0.6.14-2.fc15                 fedora
gdb.x86_64                           7.2.90.20110429-36.fc15       fedora
kernel.x86_64                        2.6.38.6-26.fc15              fedora
rpm.x86_64                           4.9.0-6.fc15                  fedora
rpm-libs.x86_64                      4.9.0-6.fc15                  fedora
rpm-python.x86_64                    4.9.0-6.fc15                  fedora
yum.noarch                           3.2.29-5.fc15                 fedora

The packages in the above output are listed as having updates available. The first package in the list is PackageKit, the graphical package manager. The line in the example output tells us:

PackageKit — the name of the package
x86_64 — the CPU architecture the package was built for
0.6.14 — the version of the updated package to be installed
fedora — the repository in which the updated package is located

The output also shows us that we can update the kernel (the kernel package), Yum and RPM themselves (the yum and rpm packages), as well as their dependencies (such as the kernel-firmware, rpm-libs, and rpm-python packages), all using yum.
