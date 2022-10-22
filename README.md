Get All Products
curl http://localhost:8080/products

[{“id”:”622a3b5a77776216a961c6f0",”name”:”Big Latte”,”price”:2.99},{“id”:”622a3b5a77776216a961c6f2",”name”:”Green team”,”price”:1.99},{“id”:”622a3b5a77776216a961c6f1",”name”:”Big Decaf”,”price”:2.49}]

Get Product By Id
curl http://localhost:8080/products/622a3b5a77776216a961c6f0

{“id”:”622a3b5a77776216a961c6f0",”name”:”Big Latte”,”price”:2.99}

Save the Product
curl -X POST \
http://localhost:8080/products \
-H ‘postman-token: ef1b4117–5b40-a11b-60dd-94eb3926f931’ \
-d ‘{
“name” : “Malai Milk”,
“price” : 3.10
}’

Response:

{
“id”: “622a3d8477776216a961c6f3”,
“name”: “Malai Milk”,
“price”: 3.1
}

Get All Products:
curl -X GET \
http://localhost:8080/products \
-H ‘cache-control: no-cache’ \
-H ‘postman-token: 7ec36e73–5dce-1080-b598–25ee29144db1’

[
{
“id”: “622a3b5a77776216a961c6f0”,
“name”: “Big Latte”,
“price”: 2.99
},
{
“id”: “622a3b5a77776216a961c6f2”,
“name”: “Green team”,
“price”: 1.99
},
{
“id”: “622a3b5a77776216a961c6f1”,
“name”: “Big Decaf”,
“price”: 2.49
},
{
“id”: “622a3d8477776216a961c6f3”,
“name”: “Malai Milk”,
“price”: 3.1
}
]

Update Product
curl -X PUT \
http://localhost:8080/products/622a3d8477776216a961c6f3 \
-H ‘cache-control: no-cache’ \
-H ‘content-type: application/json’ \
-H ‘postman-token: ab3a2dc3–0a2f-8256-afee-39de92646128’ \
-d ‘{
“name” : “Malai Milk”,
“price” : 3.99
}’

Response:

{
“id”: “622a3d8477776216a961c6f3”,
“name”: “Malai Milk”,
“price”: 3.99
}

Delete Product By Id
curl -X DELETE \
http://localhost:8080/products/622a3d8477776216a961c6f3 \
-H ‘cache-control: no-cache’ \
-H ‘postman-token: 2132d665–587f-d793-bf86–9bc4eff866a9’
