# Build Python from source

## Support lzma

Install the following libs:
	```sh
	sudo apt install liblzma-dev
	sudo apt install lzma libbz2-dev
	```

Download the source and build:

	```
	./configure --enable-optimizations --prefix=/opt/python
	```
