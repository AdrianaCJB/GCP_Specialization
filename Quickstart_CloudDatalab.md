## Quickstart Cloud Datalab

- Get the latest gcloud command:
```
gcloud components update
```
- Install the gcloud datalab component:
```
gcloud components install datalab
```

- Create a Cloud Datalab instance:
```
datalab create datalab-instance-name --zone us-central1-a
```

- Open the Cloud Datalab home page in your browser:
```
http://localhost:8081
```

-  If the terminal command window is closed or interrupted, the connection will terminate,
and you will need to run the following command to reestablish the connection:
```
datalab connect instance-name
```

- Clean Up (You incur charges from the time of creation to the time of deletion of the Cloud Datalab VM instance. 
You are also charged for the Persistent Disk where notebooks are stored) 
```
datalab delete --delete-disk instance-name
gcloud compute firewall-rules delete datalab-network-allow-ssh
gcloud compute networks delete datalab-network
gcloud source repos delete datalab-notebooks
```
