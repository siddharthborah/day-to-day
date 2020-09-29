## List of important k8s commands


### Getting detail of resources

```
kubeclt get pods          // list all the resources of a type, 
kubeclt get nodes         // you can use any resource type instead of nodes
kubectl get ns            // gets detail of namespaces
kubeclt describe po <podname> // shows the detail os a particulat resource
kubectl get pods -o wide // get more details like ip and hostname
```

#### Getting deatil in yaml or json
`-o` to get it in `yaml` or `json` type
```
kubeclt get pods pod-id -o yaml
```

### Working with labels
#### Search or filter by labels
`-l` option allows filtering and searching by labels

```
kubectl get po -l <label:condition>       // eg: kubectl get po -l app=myapp
kubectl get po -l <label:condition> -o yaml
```
#### Showing labels
```
kubectl get po -L // shows all the labels
```

### Using namespaces
Most often we will have more than one namespaces in our workspace. Using `--namespace` allows us to use a spacific name for the commans

```
kubectl get ns
kubectl --namespace=myNamespace get pods
```

## Getting help
```
kubectl <command> --help
kubectl options
kubectl explain <resorce-type>
kubectl explain services
```

## Resources

```
kubectl api-resources      // gets the list of all resource types

NAME                              SHORTNAMES
bindings                                    
componentstatuses                 cs        
configmaps                        cm        
endpoints                         ep        
events                            ev        
limitranges                       limits    
namespaces                        ns        
nodes                             no        
persistentvolumeclaims            pvc       
persistentvolumes                 pv        
pods                              po        
podtemplates                                
replicationcontrollers            rc        
resourcequotas                    quota     
secrets                                     
serviceaccounts                   sa        
services                          svc       
challenges                                  
orders                                      
mutatingwebhookconfigurations               
validatingwebhookconfigurations             
customresourcedefinitions         crd,crds  
apiservices                                 
controllerrevisions                         
daemonsets                        ds        
deployments                       deploy    
replicasets                       rs        
statefulsets                      sts       
workflows                         wf        
tokenreviews                                
localsubjectaccessreviews                   
selfsubjectaccessreviews                    
selfsubjectrulesreviews                     
subjectaccessreviews                        
horizontalpodautoscalers          hpa       
cronjobs                          cj        
jobs                                        
certificaterequests               cr,crs    
certificates                      cert,certs
clusterissuers                              
issuers                                     
certificatesigningrequests        csr       
backendconfigs                              
leases                                      
daemonsets                        ds        
deployments                       deploy    
ingresses                         ing       
networkpolicies                   netpol    
podsecuritypolicies               psp       
replicasets                       rs        
capacityrequests                  capreq    
nodes                                       
pods                                        
managedcertificates               mcrt      
ingresses                         ing       
networkpolicies                   netpol    
runtimeclasses                              
updateinfos                       updinf    
poddisruptionbudgets              pdb       
podsecuritypolicies               psp       
clusterrolebindings                         
clusterroles                                
rolebindings                                
roles                                       
priorityclasses                   pc        
csidrivers                                  
csinodes                                    
storageclasses                    sc        
volumeattachments                           
```

### References
* https://kubernetes.io/docs/reference/kubectl/cheatsheet/
* https://kubernetes.io/docs/reference/kubectl/jsonpath/

