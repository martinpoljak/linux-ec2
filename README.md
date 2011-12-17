Arch Linux Kernel EC2 Package
=============================

**linux-ec2** [AUR][1] package builds the standard [Arch Linux][2] kernel
with [Xen][3] Xsave patch and [EC2][4] suitable kernel configuration. Sources are 
derived from standard distribution kernel (the `linux` package), so from
standard kernel of [Linux][5].

Issues
------

Currently it's intended for `x86_64` machines only because I haven't been
able to get the `i686` build to run. This kernel also doesn't run on
some older availabiality zones of some regions (specially for example
on `us-east-1a`) for microinstances. This issue is known to Amazon, but
reasons aren't clear. Simply use some newer availiability zone or 
download older image from:

    http://s3.amazonaws.com/archlinux-ec2/arch-linux-64bit-ebs-20110415-minimal-ext4-bash.img.xz
    http://s3.amazonaws.com/archlinux-ec2/arch-linux-64bit-ebs-20110415-standard-ext4-zsh.img.xz

...unpack it, upload it to [S3][6] and register it as your own 
private AMI. Be warn, they are small for download but 8 GB big unpacked.

**If anyone know how to configure the i686 kernel to work on EC2,
write me and I will release it to all AWS regions. Thank You.**


Contributing
------------

1. Fork it.
2. Create a branch (`git checkout -b 20101220-my-change`).
3. Commit your changes (`git commit -am "Added something"`).
4. Push to the branch (`git push origin 20101220-my-change`).
5. Create an [Issue][9] with a link to your branch.
6. Enjoy a refreshing Diet Coke and wait.


Copyright
---------

Copyright &copy; 2011 [Martin Kozák][10]. See `LICENSE.txt` for
further details.

[9]: http://github.com/martinkozak/linux-ec2/issues
[10]: http://www.martinkozak.net/
