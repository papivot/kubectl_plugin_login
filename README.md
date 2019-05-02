# kubectl_plugin_login

**Requirements -**

1. PKS 1.4.0 enviornment with UAA enabled as OIDC provider
2. PKS CLI downloaded and installed in PATH. 

**HOW-TO**

1. Clone the repo.
2. Copy the file *kubectl-login* to your path
2. Execute *kubectl login -h* for help
3. Command Line options - 
```
kubectl login [ -u USERNAME|defaults to $USER if empty ] \
              [ -p PASSWORD|Cleartext is passed in command line - for use in automation] \
              [ -a PKS_API_Endpoint|e.g.api.pks.mydomain.com] \
              [ -c CLUSTER|Optional. If multiple clusters exist then CLUSTER needs to be specified ]
```

