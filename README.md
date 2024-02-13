helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update

helm pull prometheus-community/prometheus --untar

helm repo add argo https://argoproj.github.io/argo-helm
helm repo update

helm pull argo/argo-cd --untar

helm install argo ./argo-cd -f ./argo-cd/values.yaml

Add namespace

create application

