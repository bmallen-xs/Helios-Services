# Web Terminal

## Create Project

```sh
# Create Project
helios project add apt-cache --repo https://github.com/bmallen-xs/Helios-Services --ref main --path apt-cache

# Clone / Pull
helios project pull apt-cache
```

## Run

```sh
helios project up apt-cache
```

## How To Use

### Local Builds

Add the following to your Dockerfile

```Dockerfile
RUN echo 'Acquire::HTTP::Proxy "http://172.17.0.1:3142";' >> /etc/apt/apt.conf.d/01proxy \
 && echo 'Acquire::HTTPS::Proxy "false";' >> /etc/apt/apt.conf.d/01proxy
```

