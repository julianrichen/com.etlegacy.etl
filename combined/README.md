# ET: Legacy Flatpak Manifest
## x86_64
```
git submodule add https://github.com/flathub/shared-modules.git
flatpak-builder --force-clean --repo=etlegacy build com.etlegacy.etl.yaml
flatpak remote-add --user etlegacy etlegacy
flatpak install --user com.etlegacy.etl.data
flatpak update -y
```

## i386
```
git submodule add https://github.com/flathub/shared-modules.git
flatpak-builder --force-clean --arch=i386 --repo=etlegacy build com.etlegacy.etl.yaml
flatpak remote-add --user etlegacy etlegacy
flatpak install --user com.etlegacy.etl.data
flatpak update -y
```

## Uninstall
```
flatpak uninstall -y com.etlegacy.etl
flatpak remote-delete --user etlegacy
```
