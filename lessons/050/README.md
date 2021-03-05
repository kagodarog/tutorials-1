# How to Install MongoDB on Kubernetes?

[YouTube Tutorial]()

https://grafana.com/grafana/dashboards/12594

```
kubectl port-forward svc/mongodb-headless 27017:27017 -n database
```
```
mongo -u drage -p secretpassword123 --authenticationDatabase inventory
```
```
use inventory
db.books.insertMany([
   { title: "Moby Dick", author: "Herman Melville" },
   { title: "The Great Gatsby", author: "F. Scott Fitzgerald" },
   { title: "One Hundred Years of Solitude", author: "Gabriel Garcia Marquez" }
]);
db.books.find({}).pretty()
```

```
kubectl port-forward svc/drage 4000:4000 -n staging
```

```
for i in {1..1000}; do curl localhost:4000/books; done
```
```
db.isMaster()
```