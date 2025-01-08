# Install Pipewire for Audio

sudo add-apt-repository ppa:pipewire-debian/pipewire-upstream
sudo apt install pipewire pipewire-pulse pipewire-tests pipewire-locales gstreamer1.0-pipewire libspa-0.2-bluetooth libspa-0.2-jack pipewire-audio-client-libraries
sudo apt install pipewire libspa-0.2-bluetooth pipewire-audio-client-libraries
sudo systemctl disable --global pulseaudio
sudo systemctl enable --global pipewire-pulse
systemctl --user --now disable pulseaudio.service pulseaudio.socket
systemctl --user mask pulseaudio
sudo touch /usr/share/pipewire/media-session.d/with-pulseaudio
systemctl --user --now enable pipewire-media-session.service
systemctl --user restart pipewire-session-manager
systemctl --user daemon-reload

