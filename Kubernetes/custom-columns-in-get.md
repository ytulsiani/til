### Get custom fields when getting a Kubernetes object



`kubectl get pod -o custom-columns=KEY1:VALUE1,KEY2:VALUE2`

Example:

If you want to get all the name of a pod along with the names of all of the containers on that pod:

`kubectl get pod -o custom-columns=NAME:.metadata.name,CONTAINERS:.spec.containers[*].name`