[VM12 by Team Nocturnal](http://team-nocturnal.com)
====================================


Download the source
--------------

Please read the [VM12 building instructions](http://forums.team-nocturnal.com/index.php/forum/62-) before proceeding.

Initialize:

Create the build directory :

    $ mkdir ~/dev
    $ mkdir ~/dev/vm12
    $ cd ~/dev/vm12
Init core trees without any device/kernel/vendor :

    $ repo init -u https://github.com/vm12/platform_manifest.git -b vm12

sync repo

    $ repo sync

***

Building
--------

After the sync is finished, please read the [instructions from the Android site](http://s.android.com/source/building.html) on how to build.

    . build/envsetup.sh
    brunch
    make -j4


You can also build (and see how long it took) for specific devices like this:

    . build/envsetup.sh
    time brunch vm12_hammerhead-user
    make -j4

Remember to `make clobber` every now and then!

