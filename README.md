# SilverBullet plug template
Insert your plug description here. 

## Development preparation
1. In your (development) space, create a folder under `Library/` that you can use as a namespace, for instance using your Github username:
```bash
mkdir -p ~/myspace/Library/you
```

2. Symlink this plug's folder into your namespaced folder:

```bash
ln -s $PWD ~/myspace/Library/you/hello
```

3. Update the `name` attribute in `PLUG.md` to match the location of that PLUG file in your space, and the file name of the destination `.plug.js` file as well e.g.
```
---
name: Library/you/hello/PLUG
tags: meta/library
files:
- myplug.plug.js
---
```

## Build
To build this plug, make sure you have [Deno installed](https://docs.deno.com/runtime/). Then, build the plug with:

```shell
deno task build
```

Within ~20s SilverBullet will automatically sync your plug code, just watch your browser's JavaScript console to see when this happens. Then run the `Plugs: Reload` command to reload and reactivate the plug (no reload required).

## Distribution
1. Commit the compiled `.plug.js` file to the repository
2. Other people can now install your plug via the `Library: Install` command using the URL to your PLUG.md file as URI, e.g. `https://github.com/silverbulletmd/silverbullet-plug-template/blob/main/PLUG.md`
