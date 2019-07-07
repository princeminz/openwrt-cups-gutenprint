# lede-cups

git clone https://github.com/lede-project/source

cd source

echo "src-git printing https://github.com/princeminz/openwrt-cups-gutenprint" >> feeds.conf.default

./scripts/feeds update -a

./scripts/feeds install -a

make menuconfig (set Network->Printing->cups as "M")

make

copy /source/bin/packages/<arch>/cups/*.ipk to machine & opkg install 
