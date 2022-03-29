# argocd-cloud-native-meetup

* Create a cluster, mine will be done with kind
* Install Argo CD with kustomize from the kustomize-installation folder
  * `kustomize build kustomize-installation | kubectl apply -f -`
* If we have time login to the UI:
  * `kubectl get secret argocd-initial-admin-secret -o yaml -n argocd`
  * `kubectl port-forward svc/argocd-server -n argocd 9091:80`
* Apply the Application on the argocd ns
  * `kubectl apply -f argocd-app.yaml -n argocd`
* Profit! - let's upgrade it
