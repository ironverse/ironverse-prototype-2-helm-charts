# helm-charts

## package a chart

`helm package ironverse/`
`helm repo index .`

## create a chart

`helm create chart`

## deploy a chart

`kubectl create secret docker-registry regcred --docker-server=registry.digitalocean.com --docker-username=<access_token> --docker-password=<access_token>`

`kubectl create secret generic ironverse-database-url -n ironverse --from-literal=database_url='postgres://app:PASSWORD@cockroachdb-public.cockroachdb.svc.cluster.local:26257'`

`helm install -f ironverse-values.yaml ironverse ./ironverse`


`k port-forward svc/ironverse 8080:80`