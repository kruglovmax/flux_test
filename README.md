eksctl create cluster -f ClusterConfig.yml

EKSCTL_EXPERIMENTAL=true eksctl \
    -f ClusterConfig.yml \
    enable repo \
    --git-url=git@gitlab.allabout.me:infra/eks/devz.git \
    --git-email=fluxcd@all.me \
    --git-user=fluxcd \
    --namespace=flux --


EKSCTL_EXPERIMENTAL=true eksctl \
    -f ClusterConfig.yml \
    enable repo \
    --git-url=git@github.com:kruglovmax/flux_test.git \
    --git-email=fluxcd@all.me \
    --git-user=fluxcd \
    --namespace=flux --

EKSCTL_EXPERIMENTAL=true eksctl \
    enable profile \
    --git-url git@github.com:kruglovmax/flux_test.git \
    --git-email fluxcd@all.me \
    --git-user=fluxcd \
    -f ClusterConfig.yml \
    app-dev