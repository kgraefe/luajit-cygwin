# luajit-cygwin

This is a an updated recipe to build and package [LuaJIT][1] for [Cygwin][2].
The recipe is based on the unmaintained [Cygwin package][3].

To build the packages run the following command:

```sh
cygport luajit.cygport download prepare compile install package
```

To install the packages you can just extract them into the root directory:

```sh
eval "$(cygport luajit.cygport vars PVR)"
tar -C / -xjvf luajit-$PVR.x86_64/dist/luajit/luajit-$PVR.tar.xz
tar -C / -xjvf luajit-$PVR.x86_64/dist/luajit/lujait-devel/luajit-devel-$PVR.tar.xz
```

**WARNING:** Uninstallation is not supported. Hence you have to remove all
files manually.

[1]: http://luajit.org/luajit.html
[2]: http://www.cygwin.com/
[3]: https://cygwin.com/cgit/cygwin-packages/luajit/tree/?id=6a7b8824c0e10a7e954b4559af7fe10d9c87ca8f
