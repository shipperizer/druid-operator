.PHONY=s3

AWS?=aws
S3_ENDPOINT?=http://localstack.svc.cluster.local:4566
S3_BUCKET?=druid
AWS_SECRET_ACCESS_KEY?=0
AWS_ACCESS_KEY_ID?=0
AWS_REGION?=eu-west-1
HELM3?=helm

.EXPORT_ALL_VARIABLES:

s3:
	$(AWS) s3 mb s3://$(S3_BUCKET) --endpoint-url $(S3_ENDPOINT)

helm:
	$(HELM3) repo add bitnami https://charts.bitnami.com/bitnami
	$(HELM3) repo add localstack-charts https://localstack.github.io/helm-charts
	$(HELM3) repo update	