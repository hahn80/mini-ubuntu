# Handle HEIF/HEIC on Linux


1. Recompile libheif:


Remove the old packages:

```sh
sudo apt purge -y libheif1 libheif-dev heif-gdk-pixbuf libheif-examples
```

Install depency:

```sh
libde265-dev  libx265-dev  libjpeg-dev  libpng-dev  libaom-dev  libdav1d-dev  libgdk-pixbuf2.0-dev  libgio2.0-cil-dev  gdk-pixbuf2.0-dev
```


Clone source:

```sh
git clone https://github.com/strukturag/libheif.git
cd libheif
git checkout v1.19.5
mkdir -p build
cd build
```

CMake

```sh
cmake .. -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Release -DWITH_EXAMPLES=ON -DWITH_GDK_PIXBUF=ON -DWITH_LIBDE265=ON -DWITH_X265=ON -DWITH_AOM=ON -DWITH_DAV1D=ON
```

Make & Instal

```sh
make -j$(nproc)
sudo make install
pkg-config --modversion libheif
```

Install plugin for Gnome Image Viewer:

```sh
sudo apt install heif-gdk-pixbuf heif-thumbnailer
```


2. Build HEIF Plugin for GIMP

```sh
clone https://github.com/strukturag/heif-gimp-plugin
cd heif-gimp-plugin
./autogen.sh
./configure
make
sudo cp src/heif-gimp-plugin /usr/lib/gimp/2.0/plug-ins
```


