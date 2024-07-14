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
AGENT_JENKINS_URL=http://your-ip:port
AGENT_JENKINS_SECRET1='Your secret generated'
```

> **Note:** This value *AGENT_JENKINS_SECRET1* is generated after configuring a node permanently in the jenkins administrative panel.
