# Install Pipewire for Audio

```sh
sudo add-apt-repository ppa:pipewire-debian/pipewire-upstream
```

```sh
sudo apt install pipewire pipewire-pulse pipewire-tests pipewire-locales gstreamer1.0-pipewire libspa-0.2-bluetooth libspa-0.2-jack pipewire-audio-client-libraries
```

```sh
sudo apt install pipewire libspa-0.2-bluetooth pipewire-audio-client-libraries
```

```sh
sudo systemctl disable --global pulseaudio
```

```sh
sudo systemctl enable --global pipewire-pulse
```

```sh
systemctl --user --now disable pulseaudio.service pulseaudio.socket
```

```sh
systemctl --user mask pulseaudio
```

```sh
sudo touch /usr/share/pipewire/media-session.d/with-pulseaudio
```

```sh
systemctl --user --now enable pipewire-media-session.service
```

```sh
systemctl --user restart pipewire-session-manager
```

```sh
systemctl --user daemon-reload
```
