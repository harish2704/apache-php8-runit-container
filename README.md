# apache-php8-runit-container
apache2 php server container along with dropbear sshd and runit init system


## Usage

**compose.yml**
```yaml
services:
  www:
    image: 'ghcr.io/harish2704/apache-php8-runit-container:latest'
    tty: true
    volumes:
      - ./srvroot:/var/www/html
      - ./authorized_keys:/root/.ssh/authorized_keys
    # entrypoint: ["/bin/bash", "-c", "trap \"echo Shutting down; exit 0\" SIGTERM SIGINT SIGKILL; /bin/sleep infinity & wait"]
    ports:
      - "2022:22"
      - "2080:80"
      - "2443:443"

```
