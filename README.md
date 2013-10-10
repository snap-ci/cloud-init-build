This repo contains scripts needed to build rpms for various versions of cloud-init

# CentOS/RHEL

<pre>
$ yum install -y rpm-build rpmdevtools readline-devel ncurses-devel gdbm-devel tcl-devel openssl-devel db4-devel byacc
$ bundle install --path .bundle
</pre>

# How to build one of the packages

<pre>
$ rake
</pre>
