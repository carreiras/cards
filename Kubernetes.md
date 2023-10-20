# Cards Kubernets

## CLI GCloud (GCP)
- Autenticar na GCloud
```
$ gcloud auth login
```

- Verificar usuario logado
```
$ gcloud auth list
```

## Minikube e kubectl
- Iniciar
```
$ minikube start
```

- Verificar status
```
$ minikube status
```


- Acessar  cluster
```
$ minikube ssh
```

- Exemplo de arquivo .yaml para criação de Pod
```
apiVersion: v1
kind: Pod
metadata:
  name: app-html
  labels:
    app: app-html
spec:
  containers:
  - name: app-html
    image: httpd:latest
    ports:
    - containerPort: 80
```

- Ver os clusters
```
$ kubectl get svc
```

- Ver os nodes
```
$ kubectl get nodes
```

- Ver os pods
```
$ kubectl get pod

// ou
$ kubectl get pods

// para informações adicionais
$ kubectl get pod -o wide
```

- Criar novo pod
```
$ kubectl apply -f .\[arquivo].yaml
```
- Excluir pod
```
$ kubectl delete pod [nome]
```