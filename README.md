Arch Linux EC2 Kernel Package
=============================

**linux-ec2** [AUR][1] package builds the standard [Arch Linux][2] kernel
with [Xen][3] Xsave patch and [EC2][4] suitable minimal kernel configuration. 
Sources are derived from standard distribution kernel (the `linux` package), 
so from the standard [Linux kernel][5].

Repository
----------
Binary packages repository for the EC2 `x86_64` kernel is available at:

    [archlinux-ec2]
    Server = https://downloads.sourceforge.net/project/archlinux-ec2/repo/x86_64
    
It includes also binary packages of other EC2 related tools from [AUR][1].
For use the kernel at `i386`, please, build your own. At this time, 
I haven't available reasonable build machine for regular `i386` building.
 

Issues
------
This kernel might not run on some older availability zones of some 
regions (specially for example on `us-east-1a`) at microinstances. 
This issue is known to Amazon, but reasons aren't clear and difficulties
vary a lot. Simply use some newer availability zone in case of 
necessity or download an older image from:

    http://s3.amazonaws.com/archlinux-ec2/arch-linux-64bit-ebs-20110415-minimal-ext4-bash.img.xz
    http://s3.amazonaws.com/archlinux-ec2/arch-linux-64bit-ebs-20110415-standard-ext4-zsh.img.xz

...unpack it, upload it to [S3][6] and register it as your own 
private AMI. Be warn, they are small for download but 8 GB big unpacked.

The `i386` version builds fully functional but full kernel. If someone is 
able to provide me the minimal EC2 configuration for i386 platform, let's 
do it. The `x64` version builds kernel with at EC2 usable modules only,
but maintains some modules which probably can be removed from the build too.


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

Everything is Public Domain. Author is [Martin Kozák][10].

[1]: http://aur.archlinux.org/
[2]: http://www.archlinux.org/
[3]: http://xen.org/
[4]: http://aws.amazon.com/ec2/
[5]: http://www.kernel.org/
[6]: http://aws.amazon.com/s3/
[9]: http://github.com/martinkozak/linux-ec2/issues
[10]: http://www.martinkozak.net/
