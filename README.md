# tiny-aosp-mirror
## Usage
`tiny-aosp-mirror [file ...]`

This scripts creates/updates a local aosp mirror in `$PWD`. Within the mirror
subprojects are deactivated for sync with upstream which are not used by one
or more aosp or aosp related projects (like lineage).
You should use this mirror only if you want to have full history within the
git repos rather then shallow copies. If you are fine with cloning only a
certain branch as a shallow copy, do not use this script, but rather init with
`repo init -u <manifest> -b <branch> --depth=1` and then sync with
`repo sync -c --no-clone-bundle` to reduce bandwidth.

## Caveats
You have to update your other projects manually to sync with the local mirror.
Also the mirrors manifest at `platform/manifest.git` does not reflect the
removed projects.
