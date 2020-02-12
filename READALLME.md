```
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
```


```
[ℹ]  subnets for eu-central-1b - public:192.168.0.0/19 private:192.168.96.0/19
[ℹ]  subnets for eu-central-1c - public:192.168.32.0/19 private:192.168.128.0/19
[ℹ]  subnets for eu-central-1a - public:192.168.64.0/19 private:192.168.160.0/19
```
