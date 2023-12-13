# Jenkins with Docker

## Environment .env

### Jenkins

```
JENKINS_PORT=0.0.0.0:8080
JENKINS_PORT_CONNECTOR:0.0.0.0:50000
JENKINS_OPTS='--prefix=/your_context'
```

### Jenkins Agents

```
AGENT_IMAGE=jenkins/ssh-agent:jdk11
AGENT_RSA=<YOUR_RSA>
```

Example format RSA:

```
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDrSF2XICucxX//hz0PVgDVv3EisY6C99u9sA1QoZSdHuXW/H5i/1BT3CtUzBAsCOJxdSuadKfJZnNDEL98lmagU79tAgNjVgCnUyoKEkaEOz4J416cUsF/hR/rKUeRimcox6BncwixYsfmmcZMo1ImKWqdYIDu6TJV0RjhdpZyfn1RTxV0VXP1cn5yLO4aGz8ZCPLmvxVONykc0FLBVz3XgbpFW9xY3O4iaSrpoYn9Ce0m+Txx0lPYlm5bt6C2F6hp0LaBACsekAZz0oAXCKAel9gj27l8vXNj0eN2J8fxQdsTDtZ6Pnnd73ATfK114ceLDHL2VyV8m1KxD5Cm+zFgB7AfZ0xBsN+KGBtPqha7971lZSUvjKvRNXnPk3xrzwTPGKL8vnJOUidsx+6KzSTPB/sk8L9YsEy9i023KZTQMXTv0IrLp8Bbm3V4wWGsdfmviLMq3x2QMSMXlpE00alCar2eSah0425POSpyEtLFEDj2tURVjP+LmKroc8bOILc= jenkins@yourdomain.com
```
