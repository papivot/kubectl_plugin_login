# kubectl_plugin_login

**Requirements -**

1. PKS 1.4.x enviornment with UAA enabled as OIDC provider
2. PKS CLI downloaded and installed in PATH. 

**HOW-TO**

1. Clone the repo.
3. *Chmod +x kubectl-login*
2. Copy *kubectl-login* to your PATH
2. Execute *kubectl login -h* for help
3. Command Line options - 
```
kubectl login [ -u USERNAME|Optional. Defaults to $USER if not provided ] \
              [ -p PASSWORD|Optional. Cleartext is passed in command line - for use in automation] \
              [ -a PKS_API_Endpoint|Optional. e.g.api.pks.mydomain.com. Can be provided later in the execution ] \
              [ -c CLUSTER|Optional. If multiple clusters exist then CLUSTER needs to be specified ]
              
Usage examples - 

kubectl login -u alana -p Passw0rd -a api.pks.mydomain.com -c cluster00
kubectl login -u alana -p Passw0rd -a api.pks.mydomain.com 
kubectl login -u alana -p Passw0rd 
kubeclt login -u alana
kubectl login


```
WIP: TODO: To capture cluster name during the execution when multiple clusters exist. 
