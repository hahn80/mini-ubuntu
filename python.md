# Build Python from Source

1. Install the following libs:

	```sh
	sudo apt install build-essential pkg-config
	sudo apt install uuid-dev zlib1g-dev liblzma-dev
	sudo apt install libbz2-dev libffi-dev libsqlite3-dev
	sudo apt install libgdbm-dev libgdbm-compat-dev
	sudo apt install libncurses5-dev libreadline6-dev libssl-dev
	```

2. Download and build the source:

	```sh
	export CFLAGS="-fPIC"
	./configure --enable-optimizations --prefix=/opt/python --enable-shared
	make
	```

3. Add python LIB to LD_LIBRARY_PATH

    ```sh
    sudo nano /etc/ld.so.conf.d/python3.8.conf
    # and add the lib path to it
    /opt/python/lib
    # update ldconfig
    sudo ldconfig
    # check the config
    ldconfig -p | grep libpython
    ```

4. Alias python

    ```sh
    sudo ln -s /opt/python/bin/python3.8 /usr/local/bin/python
    ```

5. Update pip

    ```sh
    sudo python -m pip install pip -U
    ```
 


