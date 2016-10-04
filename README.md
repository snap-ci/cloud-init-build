[![Build Status](https://snap-ci.com/snap-ci/cloud-init-build/branch/master/build_image)](https://snap-ci.com/snap-ci/cloud-init-build/branch/master)

This repo contains scripts needed to build rpms for various versions of cloud-init. To report an issue, [please contact the Snap.ci support team.](https://snap-ci.com/contact-us)

# CentOS/RHEL

<pre>
$ yum install -y rpm-build rpmdevtools readline-devel ncurses-devel gdbm-devel tcl-devel openssl-devel db4-devel byacc
$ bundle install --path .bundle
</pre>

# How to build one of the packages

<pre>
$ rake
</pre>
