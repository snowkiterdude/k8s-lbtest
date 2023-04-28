# k8s-lbtest
test application for basic deployment and service hello world via FluxCD


Setup:
```
$ kind create cluster
$ kubectl create ns flux
$ export GH_USER=<my-user>
$ export REPO_NAME=<my-repo>
$ fluxctl install \
--git-user=${GH_USER} \
--git-email=${GH_USER}@users.noreply.github.com \
--git-url=git@github.com:${GH_USER}/${REPO_NAME} \
--git-path=namespaces,k8s-lbtest-manifests \
--namespace=flux | kubectl apply -f -
```

