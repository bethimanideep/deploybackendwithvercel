video explaination 
https://drive.google.com/file/d/12OE4mu4st7MHI9-bb-A1RrVH8wBOkk84/view <br/> 
Demonstrating the API's
#User api's

1. Register <br />
   API endpoint = (/api/register) <br />
   method : "POST" <br />
   payload : { <br />
   "name": "user1", <br />
   "email": "user1@gmail.com", <br />
   "password": "password", <br />
   "address": { <br />
   "street": "street1", <br />
   "city": "city1", <br />
   "state": "state1", <br />
   "country": "country1", <br />
   "zip": "zip1" <br />
   } <br />
   } <br />

2. Login <br />
   API endpoint = (/api/login) <br />
   method : "POST" <br />
   payload : { <br />
   "email": "user1@gmail.com", <br />
   "password": "password", <br />
   } <br />

3. Reset Password <br />
   API endpoint = (/api/user/:id/reset) <br />
   id = Id of that user's document <br />
   method : "PATCH" <br />
   payload : { <br />
   "currentPassword": "", <br />
   "newPassword": "", <br />
   } <br />



#Restaurant api's


1. Get all restaurants <br />
   API endpoint = (/api/restaurants) <br />
   method : "GET" <br />

2. Get single restaurant using id <br />
   API endpoint = (/api/restaurants/:id) <br />
   method : "GET" <br />

3. Menu of a Restaurant <br />
   API endpoint = (/api/restaurants/:id/menu) <br />
   method : "GET" <br />

4. Create a Restaurant <br />
   API endpoint = (/api/addrestaurant) <br />
   method : "POST" <br />
   payload : { <br />
   "name": "restaurant3", <br />
    "address": { <br />
        "street": "street3", <br />
        "city": "city3", <br />
        "state": "state3", <br />
        "country": "country3", <br />
        "zip": "zip3" <br />
    },<br />
    "menu":[<br />
      {<br />
        "name": "item1",<br />
        "description": "food item to eat",<br />
        "price": 170,<br />
        "image": "item1Image"<br />
      }<br />
      ]<br />
   } <br />


#Order api's


1. Place an order <br />
   API endpoint = (/api/orders) <br />
   method : "POST" <br />
   payload : { <br />
   "items": <br />
      [<br />
        {<br />
          "name": "product1",<br />
          "price": 20,<br />
          "quantity": 2<br />
        },<br />
        {<br />
          "name": "product2",<br />
          "price": 30,<br />
          "quantity": 2<br />
        }<br />
      ],<br />
    "restaurantId":String<br />
    "userId":String
    }<br />
   } <br />

2. Get an order <br />
   API endpoint = (/api/orders/:id) <br />
   method : "GET" <br />

3. change the status of order <br />
   API endpoint = (/api/orders/:id) <br />
   method : "PATCH" <br />
   payload : { <br />
   "status": "", <br />
   } <br />  
   "default status value" : "placed"  <br />
   "status" accepting values = ["placed", "preparing", "on the way", "delivered"] <br />
