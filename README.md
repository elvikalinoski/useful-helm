# Useful Helm


## Delete all releases
helm delete $(helm ls |awk '{if (NR!=1) {print $1}}')

## Add repository
helm repo add {name} {repository link}

## Update 
helm repo update

## Test Rendering
helm template . --values test/test.yaml --set deploymentHash=fdeds

## Updating
helm package src/pom-v7 --destination ./docs
helm repo index ./docs --url https://github.com/elvikalinoski/useful-helm

## Install a chart:
helm repo install webplates/[CHART]
