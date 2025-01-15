# wis2box-release

This repository tests how GitHub releases associated to a separate "wis2box-release" repository can be used to track which images belong to which wis2box-release.

In this example a reference file `wis2box.images` list all images that form a specific wis2box-release.

Upon publishing a new release of this repository, the `wis2box.images` files is published as an artifact of the release.

This allows the script "wis2box-ctl.py" to retrieve the list of images associated to a specific wis2box-release when an update is required.

When new images are published containing security updates or bug fixes, the `wis2box.images` file is to be updated and a new release-reference is published.

TODO: add automated scripts that tests if the latest version of the images in this repository passes the latest tests defined in the wis2box-repository.