# k8s-lbtest
test application for basic deployment and service hello world via FluxCD


Setup:
```
$ kind create cluster
$ export GH_USER=<my-user>
$ export REPO_NAME=<my-repo>
$ export KEY_FILE=~/.ssh/id_rsa

$ flux bootstrap git \
  --url=ssh://git@github.com/${GH_USER}/${REPO_NAME} \
  --branch=main \
  --path="" \
  --private-key-file=${KEY_FILE}

#$ fluxctl identity --k8s-fwd-ns flux
#$ fluxctl sync --k8s-fwd-ns flux

```

