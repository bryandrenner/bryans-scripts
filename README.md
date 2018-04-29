# Bryan's Scripts

This repository contains my personal configuration and initialization scripts for various machines, operating systems, and applications.

## Taxonomy

My scripts may be classified by the following properties:

1. product name
2. product version
3. hosting product

The classification of a script results in a string.  As a bare minimum, every script must have an applicable product name.  For example, a script that applies to all versions of Vim may simply be classified as `vim`.  A script that applies to all versions of Ubuntu may be classified as `ubuntu`.

The remaining properties may be supplied as needed, in order and separated by a hyphen.  For example, if a script only applies to Vim 7.x, it should be classifed as `vim-7.x`.  If it only applies to Vim 7.x on Ubuntu, it should be classified as `vim-7.x-ubuntu`.

Hosting products may be nested.  If it only applies to Vim 7.x on Ubuntu running on my personal machine, "Nadia", it should be classified as `vim-7.x-ubuntu-nadia`.

The reality is that I won't often be aware of specific classifications, such as the range of versions to which it applies, or the range of hosting operating system versions to which the script applies.  I will simply classify these scripts *to the best of my knowledge*.

## Folder structure

Root level folders represent the script classifications.  For example, a root level folder, `vim-windows` would contains scripts that only apply to Vim running under Windows.

Under each root level folder, scripts may be classified into two kinds: `init` and `config`.  Initialization scripts should only run once for a particular environment.  Config scripts may change over time.  So, for example, `vim-windows/init` contains scripts to initialize Vim in Windows.

## Symbolic links

One method of enabling a config script is to create a symlink from its native location to its location in this repository.  For example, a Bash configuration script could be pointed to `bash/config/.bash_profile`.
