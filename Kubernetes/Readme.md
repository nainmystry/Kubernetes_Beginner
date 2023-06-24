These are sample K8s scripts required to create and host a Mongo DB and Mongo DB service.

1. We will create 2 Deployment Pod
2. 2 Services (Internal comm and to handle external requests)
3. 1 ConfigMap file to store all the configs
4. 1 Secrets File.


The flow of application will be as follows: 
1. Request Comes from browser -> 
2. (Goes to the external service)Mongo Express External Service ->
3. (The request is then forwarded to Mongo Express pod) -> 
4. (pod will connect to internal service of mongo DB)Mongo DB internal service -> 
5. (then the request will be forwarded to the Mongo Db pod. Inside that the request will be authenticated and further action will be done) Mongo DB Pod.


TO use the secrets from secret file inside the other files, secrets file needs to created and excuted first on K8s.

