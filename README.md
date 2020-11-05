# externaldns-helm
externaldns helm chart

# Install 
helm install ./externaldns-chart

# Test

Just kubectl apply this service

```
apiVersion: v1
kind: Service
metadata:
  name: mytest-externaldns-service
  annotations:
    external-dns.alpha.kubernetes.io/hostname: testtest.alnk.eu
spec:
  type: ExternalName
  externalName: local.alnk.eu
```
