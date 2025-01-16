# frontface

## Create namespace

    kubectl create namespace exam

## Add label to namespace

    kubectl label namespace exam monitoring=true


## Fontos

Töröltem fixáltam a portot a deploynál, amit majd vissza kell álítani

## Template létrehozása

    helm create exam-chart

## Template megjelenítése (be kell lépni a chart mappába)

    helm template exam-chart .

## Helm chart telepítése (be kell lépni a chart mappába)

    helm install exam-chart . -n exam

## Helm chart frisítése (be kell lépni a chart mappába)

    helm upgrade exam-chart . -n exam

## Helm Release létrehozása

    helm upgrade --install frontface . -f .\forntface-values.yaml -n exam

## Helm Chart szerkeszése

- Először is át kell álítani a containerPort-ot 8080-re 
- A service file-ben törljük a type értékét
- A value-ben az ingress-t álítsuk true-ra
- Állítsuk be a hostot
- Állítsuk be a pathType: Prefix