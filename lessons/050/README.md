# How to Install MongoDB on Kubernetes?

[YouTube Tutorial]()

helm fetch bitnami/mongodb

helm template bitnami/mongodb -f mongodb/values.yaml --output-dir mongo-standalone

https://grafana.com/grafana/dashboards/12594


https://github.com/bitnami/bitnami-docker-mongodb#setting-up-replication

kubectl port-forward svc/mongodb-headless 27017:27017 -n database

db.auth({ user: "root", pwd: "password123" })
db.auth({ user: "username", pwd: "password" })

db.auth("username", "password")

mongo -u username -p password --authenticationDatabase database
mongo -u root -p password123

Collections are analogous to tables in relational databases.
MongoDB stores data records as documents (specifically BSON documents) which are gathered together in collections. A database stores one or more collections of documents.

db.books.insertMany([
   { title: "Moby Dick", author: "Herman Melville" },
   { title: "The Great Gatsby", author: "F. Scott Fitzgerald" },
   { title: "One Hundred Years of Solitude", author: "Gabriel Garcia Marquez" }
]);

db.books.find({}).pretty()


set -B                  # enable brace expansion

for i in {1..1000}; do curl localhost:5000/books; done