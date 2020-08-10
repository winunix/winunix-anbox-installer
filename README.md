# Anbox Installer

## How to install Anbox

``` bash
wget -qO - "https://winunix.github.io/debian/public.key" | sudo apt-key add -
echo "deb https://winunix.github.io/debian focal main" | sudo tee /etc/apt/sources.list.d/winunix-focal.list
sudo apt update
sudo apt install winunix-anbox-installer
```

## How to install some apk

``` bash
apk-install yourapp.apk
```

## How to remove some apk

You can use GUI programs like Muon, Discover or Synaptic.
You can also use APT using:

``` bash
sudo apt purge my.id.of.my.android.app
```

## How to generate deb file

Use the command `apk2deb` to generate file `config.data` and folder `package`.
You can edit de file `config.data` and modify options to add screenshot and description.
Now run the command `deb-boilerplate` to generate of files necessaries to compile the project.

``` bash
cd /path/of/folder/from/your/apk/file/
apk2deb yourapp.apk
deb-boilerplate
```