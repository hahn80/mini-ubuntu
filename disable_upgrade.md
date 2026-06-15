# Disable Kernel Upgrade


## Mark hold kernel updates

```sh
sudo apt-mark hold linux-image-$(uname -r) linux-headers-$(uname -r) linux-modules-$(uname -r) linux-generic linux-image-generic linux-headers-generic
```

One extra safety net — edit apt config to always skip kernel packages:

```sh
echo 'Package: linux-*
Pin: release *
Pin-Priority: -1' | sudo tee /etc/apt/preferences.d/block-kernel-updates
```

## Mark unhold kernel updates

```sh
sudo apt-mark unhold linux-image-$(uname -r) linux-headers-$(uname -r) linux-modules-$(uname -r) linux-generic linux-image-generic linux-headers-generic
```

