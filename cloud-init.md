# Disable cloud-init in Ubuntu

## Prevent loading at start-up

- Create an empty file to prevent the service from starting

		sudo touch /etc/cloud/cloud-init.disabled

## Uninstall

- Disable all services (uncheck everything except "None"):

		sudo dpkg-reconfigure cloud-init

- Uninstall the package and delete the folders

		sudo dpkg-reconfigure cloud-init
		sudo apt-get purge cloud-init
		sudo rm -rf /etc/cloud/ && sudo rm -rf /var/lib/cloud/

- Restart the computer

		sudo reboot

## Sources

- https://cloudinit.readthedocs.io/en/latest/topics/boot.html#generator
- https://www.blackmoreops.com/2019/04/19/remove-cloud-init-from-ubuntu/
