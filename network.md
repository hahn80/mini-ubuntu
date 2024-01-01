## Manage Network in Gnome

1. Set wifi-network manually: We need to create a netplan file
2. Go to /etc/netplan and create a file: `00-installer-config-wifi.yaml`
with the content below

```YAML
network:
  version: 2
  wifis:
    wlp0s20f3:
      access-points:
        R9999999:
          password: Password
      dhcp4: true
```

3. `chmod 600 00-installer-config-wifi.yaml`

4. Run bash commands:

    ```sh
    sudo netplan generate
    sudo netplan apply
    sudo service NetworkManager restart
    ```

5. Write netplan for all network.
Firs, delete the file `00-installer-config-wifi.yaml` created when installed. Then create a new one:

```sh
sudo nano /etc/netplan/01-network-manager-all.yaml
```

6. Add content

```yaml
network:
  version: 2
  renderer: NetworkManager
```

7. Chmod 600 and generate as showed above.



