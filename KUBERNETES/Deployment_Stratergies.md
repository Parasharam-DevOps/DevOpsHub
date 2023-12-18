Blog Link - https://www.weave.works/blog/kubernetes-deployment-strategies
Free Handson UI - https://killercoda.com/playgrounds/scenario/kubernetes


## Updating an application: 
>> Updating an already running application can be a tedious task. As it may result in downtime of our application which is not ideal in such a cut throat competitive world. 
>> Kubernetes deployment strategies allow us to update ours running application with zero downtime. 
>> Rolling update is a default deployment strategy used in Kubernetes. 
## Various deployment strategies available in Kubernetes
1. Recreate: It will release the new update and terminate the old one. this procedure will result in downtime and ideally not used in production. 
2. Rolling : It is default deployment strategy ,release a new version on a rolling update fashion, one after the other.
3. Blue/green: Release a new version alongside the old version then switch traffic.
4. Canary: release a new version to a subset of users, then proceed to a full rollout.

## Terms used in strategy definition inside deployment manifest: 
1. type: Define type of strategy used for updation of application. 
2. maxSurge: Number of pods that be increased in the cluster during updation of an application. 
3. maxUnavailable: Number of pods that can be taken down/unavailable during update. 
4. minReadySeconds: Time taken by pods to get in ready state. 
5. revisionHistoryLimit: Number of versions of update maintained by the cluster, default value is 10. 

## Commands
>> command to check rollout status : kubectl rollout status deployment deployment-name
>> command to check rollout history : kubectl rollout history deployment deployment-name
>> command to check rollout history with specifc revision: kubectl rollout history deployment deployment-name --revision revision-number
>> command to rollout deployment via imperative approach : kubectl set image deployment myapp-deployment nginx-container=nginx:1.15
>> command to update change-cause in rollout history: kubectl annotate deployment deployment-name kubernetes.io/change-cause="Need to mention cause here"
>> command to add change-use in rollout without annotate: kubectl set image deployment myapp-deployment nginx-container=1.15 --record=true
>> command to undo rollout: kubectl rollout undo deployment deployment-name 
>> command to undo rollout to specific version: kubectl rollout undo deployment deployment-name --to-revision=revision_number
>> command to pause rollout: kubectl rollout pause depolyment deployment-name
>> command to resume rollout: kubectl rollout resume deployment deployment-name
