# Yazi setup

Notes on how to install Yazi on Windows and Ubuntu systems.

## Windows

TODO

## Ubuntu

Update & install optional deps
```
sudo apt update
sudo apt upgrade
sudo apt install ffmpeg p7zip-full jq poppler-utils fd-find ripgrep fzf zoxide imagemagick unzip chafa
```

Download the latest .zip release (replace version if needed)
```
wget -qO yazi.zip https://github.com/sxyazi/yazi/releases/download/v25.5.31/yazi-x86_64-unknown-linux-gnu.zip
```

Extract to a temp directory
```
unzip -q yazi.zip -d yazi-temp
```

Move executables (yazi + ya) into /usr/local/bin
```
sudo mv yazi-temp/*/yazi /usr/local/bin/
sudo mv yazi-temp/*/ya /usr/local/bin/
```

Optionally clean up
```
rm -rf yazi-temp yazi.zip
```

Verify installation
```
yazi --version
ya --version
```

Verify detailed installation info. Check if there is any dependencies missing or yazi is not able to find
```
yazi --debug
```