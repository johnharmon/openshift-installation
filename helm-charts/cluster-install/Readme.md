## CHART: cluster-install
#### Usage
- This chart must be built in the correct order to function properly as some resources within it reference others that should also be built by this chart beforehand
- bash/zsh: ```oc login <cluster-login-info> && for tpl in $(ls helm-charts/cluster-install/templates); do helm template helm-charts/cluster-install --show-only helm-charts/cluster-install/templates/$tpl | oc apply -f -; done```
- fish: ```oc login <cluster-login-info> && for tpl in (ls helm-charts/cluster-install/templates); do helm template helm-charts/cluster-install --show-only helm-charts/cluster-install/templates/$tpl | oc apply -f -; end```


#### Variables
| Name | Type | Default | Explaination |
|------|------|---------|--------------|
| sno | boolean | false | Indicates that this is a sno cluster. Various sections of template are gated by the value of this variable 
| clusterName | String | None | The name of the cluster to be installed. Does not include the base domain

