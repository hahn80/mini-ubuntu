# Install Multiple Java Versions

1. Install version 11:

    ```sh
    sudo apt install openjdk-11-jdk-headless
    ```

2. Install version 21:

    ```sh
    sudo apt install openjdk-21-jdk-headless
    ```


3. Update the version to Java version

a) List all java versions:

    ```sh
    update-java-alternatives --list
    ```

b) Set java version as default (needs root permissions):

    ```sh
    sudo update-alternatives --config java
    ```


