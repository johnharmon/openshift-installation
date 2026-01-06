## CHART: cluster-install
#### Usage
- This chart must be built in the correct order to function properly as some resources within it reference others that should also be built by this chart beforehand
- bash/zsh: ```oc login <cluster-login-info> && cd helm-charts/cluster-install && for tpl in $(ls ./templates); do helm template ./ --show-only templates/$tpl | oc apply -f -; done```
- fish: `oc login <cluster-login-info> && cd helm-charts/cluster-install && for tpl in $(ls ./templates); helm template ./ --show-only templates/$tpl | oc apply -f -; end`
