# Jenkins with Docker

## Environment .env

### Jenkins Master

```
JENKINS_PORT=0.0.0.0=8080
JENKINS_PORT_CONNECTOR=0.0.0.0:50000
JENKINS_OPTS='--prefix=/your_context'
```

### Jenkins Agents

```
JENKINS_MASTER_URL=http://your-ip:port
JENKINS_AGENT_SECRET='Your secret value'
```
