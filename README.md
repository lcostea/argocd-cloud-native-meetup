# argocd-cloud-native-meetup

* Create a cluster, mine will be done with kind
* Install Argo CD with kustomize from the kustomize-installation folder
  * `kustomize build kustomize-installation | kubectl apply -f -`
* Apply the Application on the argocd ns
  * `kubectl apply -f argocd-app.yaml`
* Profit! - let's upgrade it