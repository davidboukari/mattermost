# mattermost
```
docker pull mattermost/mattermost-preview
docker run --name mattermost-preview -d --publish 8065:8065 --add-host dockerhost:192.168.0.1 mattermost/mattermost-preview
```
Go to http://192.168.0.1:8065/

## Create the incoming webhook
* Menu -> Integrations -> Incoming Webhooks -> Add

* https://stackoverflow.com/questions/53712149/how-to-send-mattermost-notifications-in-jenkins-using-groovy
In the Jenkinsfile
```
...
       mattermostSend (
          color: "#2A42EE",
          channel: 'essai',
          endpoint: 'http://192.168.0.133:8065/hooks/wfoscr4wdiyyie51n17815sxie', 
          message: "Hello from jenkins"
        ) 

```
