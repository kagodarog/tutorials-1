# How to Install MongoDB on Kubernetes?

[YouTube Tutorial]()

https://grafana.com/grafana/dashboards/12594







aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 424432388155.dkr.ecr.us-east-1.amazonaws.com
docker tag drage:v0.1.4 424432388155.dkr.ecr.us-east-1.amazonaws.com/drage:v0.1.4
docker push 424432388155.dkr.ecr.us-east-1.amazonaws.com/drage:v0.1.4


kubectl port-forward svc/mongodb-headless 27017:27017 -n database
mongo -u drage -p secretpassword123 --authenticationDatabase inventory

use inventory
db.books.insertMany([
   { title: "Moby Dick", author: "Herman Melville" },
   { title: "The Great Gatsby", author: "F. Scott Fitzgerald" },
   { title: "One Hundred Years of Solitude", author: "Gabriel Garcia Marquez" }
]);
db.books.find({}).pretty()

kubectl port-forward svc/drage 4000:4000 -n staging

for i in {1..1000}; do curl localhost:4000/books; done