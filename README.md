VIA VAB-820/AMOS-820 BSP release
================================

To get the whole BSP, you have to use the `repo` utility.

To install `repo`:

    $: mkdir ~/bin
    $: curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
    $: chmod a+x ~/bin/repo

To download the BSP source:

    $: PATH=${PATH}:~/bin
    $: mkdir via-vab820-bsp
    $: cd via-vab820-bsp
    $: repo init -u https://github.com/viaembedded/via-vab820-bsp-platform -b dora
    $: repo sync

At the end of this process, you will have all the metadata to start to work with.

    $: source ./setup-environment build
    $: bitbake via-image-x11

You can use any directory on your host computer to be the build directory (just replace
`build` above with your desired path).
