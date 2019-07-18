# kubectl login plugin

**Requirements -**

* PKS 1.4.x enviornment with UAA enabled as OIDC provider - use *kubectl-login-oidc*. 
* If OIDC is not enabled and/or access will be thru token/password - use *kubectl-login-token*.
* curl/jq/openssl installed 

Validated on Linux and Mac.  Can be used in interactive or automaded mode.

**HOW-TO**

1. Clone the repo.

> `https://github.com/papivot/kubectl_plugin_login.git`

2. Copy the relevent *kubectl-login-[oidc/token]* to your PATH as *kubectl-login*. E.g.

> `cp kubectl-login-oidc /usr/local/bin/kubectl-login`

or

> `cp kubectl-login-token /usr/local/bin/kubectl-login`

3. Execute `kubectl login -h` for help (if it fails to execute, validate that kubectl-login is set to **executable**)
4. Command Line options - 

```
kubectl login [ -u USERNAME|Optional. Defaults to $USER if not provided ] \
              [ -p PASSWORD|Optional. Cleartext is passed in command line - for use in automation] \
              [ -a PKS_API_Endpoint|Optional. e.g.api.pks.mydomain.com. Can be provided later in the execution ] \
              [ -c CLUSTER CLUSTER_NAME to be used for context ] \
              [ -m CLUSTER_API_EP|Optional. e.g. cluster.mydomain.com:8443. Can be provided later ] \
              
Usage examples - 

kubectl login -u naomi -p Passw0rd -a api.pks.mydomain.com -c cluster00 -m cluster.mydomain.com:8443
kubectl login -u naomi -p Passw0rd -a api.pks.mydomain.com 
kubectl login -u naomi -p Passw0rd 
kubeclt login -u naomi
kubectl login
```
