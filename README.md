![hclyn](https://raw.githubusercontent.com/hlcynprjct/manifest/twelve/res/logo.png)

## Building _hlcyn_

### Download _hlcyn_ Source
Now, let's Download _**hlcyn**_ Source

- First, make directory for _**hlcyn**_ Source, and then enter to the directory.
```
 mkdir -p ~/hlcyn
 cd ~/hlcyn
```

- Second, initialize _**hlcyn**_ Source manifest in the directory
```
 repo init -u git://github.com/hlcynprjct/manifest.git -b twelve
```

- Just in case you just want save more space and data, you can use command below
```
 repo init --depth=1 -u git://github.com/hlcynprjct/manifest.git -b twelve
```

- Third, start downloading the _**hlcyn**_ Source.
```
 repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j$(nproc --all)
```

### Start building
Now, let's start compilation

- Call building environtment setup script.
```
 source build/envsetup.sh
 lunch halcyon_<device_codename>-userdebug
 make bacon -j$(nproc --all)
```
