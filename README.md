# Service Bus Explorer - Extended Edition
**Original project:** https://github.com/paolosalvatori/ServiceBusExplorer

This version was extended to listen to a event hub with a "Listen Only" access key. All other features of version 5.0.4 continue to work the same with the "Root" access key.

## How this version works
With this modified version, you can use a connection string whose Shared Access Key has only the 'Listen' claim.
All you need is add the following parameters to the connection string, where [EventHubName] is the name of the desired Event Hub and [NumberOfPartitions] the corresponding total number of partitions: 
- **EntityPath=[EvenHubName];PartitionsCount=[NumberOfPartitions]**

### Example connection string:
  
```
Endpoint=sb://mynamespace.servicebus.windows.net/;SharedAccessKeyName=ListenOnlyKey;SharedAccessKey=AbCdEfGhIjKlMnOpQrStUvWxYz0123456789////====;EntityPath=myeventhub;PartitionsCount=4
```

![image](https://user-images.githubusercontent.com/12596820/146998382-993a5db3-8c6a-47d8-af94-df50f523008a.png)


