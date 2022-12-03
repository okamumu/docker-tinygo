# docker-tinygo-ide

A docker image for a lightweight integrated development environment for TinyGo

## Installed packages

- TinyGo: 0.26.0
- Go: 1.18.8
- Code-Server: latest (4.8.3)

## Usage

```sh
docker run -it --rm --namge tinygo-ide \
    -p 8080:8080 \
    -v $PWD:/home/vscode \
    -e VSCODE_PASSWORD=password \
    -e VSCODE_USER=vscode \
    -e VSCODE_UID=1000 \
    -e VSCODE_HOME=/home/vscode \
    tinygo-ide
```

## Environment

- VSCODE_UID: uid for login user
- VSCODE_USER: username for login user
- VSCODE_PASSWORD: password for login user
- VSCODE_GID: gid for the group of login user
- VSCODE_GROUP: groupname for the group of login user
- VSCODE_HOME: home directory for login user
- VSCODE_GRANT_SUDO: The grant of sudo
    - yes: the user can execute sudo but the password is required
    - no: the user cannot execute sudo
    - nopass: the user can execute sudo without password

