# README

## Pasos

	1.- crear el main branch
	2.- crear el gh-pages branch
	3.- crear el feature branch

## check CRDs version

	kubectl get crd  | grep external

	kubectl describe crd externalsecrets.external-secrets.io

## Loging

-- login

	helm registry login  

-- privado

	helm repo add argocd-helm-charts https://raw.githubusercontent.com/ligo-dev/argocd-helm-charts/gh-pages --username pepe --password pepe  

-- publico

	helm repo add argocd-helm-charts https://raw.githubusercontent.com/ligo-dev/argocd-helm-charts/gh-pages  

-- pull

	helm dependency build  

## Test

	helm upgrade dummy --install . -f values-example.yaml -n dummy --dry-run --debug

	helm upgrade eks-test-ci --install . -f values-example.yaml