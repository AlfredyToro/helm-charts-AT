# helm-charts-AT
Helm Charts OCI Artifacts

/
helm pull fairwinds-stable/polaris --untar
helm package polaris/ -d charts/  

helm repo index .  --url https://alfredytoro.github.io/helm-charts-at/
helm repo index . --merge index.yaml --url https://alfredytoro.github.io/helm-charts-at/
git add . && git commit -m "final" && git push origin gh-pages
(wait until the deployment of github pages)
helm repo add githubat2 https://alfredytoro.github.io/helm-charts-at
helm install nginx githubat2/nginx --namespace nginx --create-namespace 