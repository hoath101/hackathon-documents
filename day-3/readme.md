# Day_3  Data_Migration_Template_2.

## Given API Base URL:

``https://hackathon-apis.vercel.app/api/products``

### Description:

This endpoint retrieves a list of products available in the store. Each product includes detailed information such as the product's name, description, price, category, initial quantity, tags, and an image URL. The response provides an array of products in JSON format.

### Example Response:

[
  {

    "name": "The Poplar suede sofa",
    
    "description": "A timeless design, with premium materials features as one of our most popular and iconic pieces. The dandy chair is perfect for any stylish living space with beech legs and lambskin leather upholstery.",
    
    "image": "https://cdn.sanity.io/images/ri847jqu/production/9b6a4fc8c65bbb4e5793fb0e1116b510d73dc9e8-630x375.png",
    
    "_id": "65453ffd-e476-4b6b-a388-7e3de1bb632a",
    
    "features": [
        "Premium material",
        "Handmade upholster",
        "Quality timeless classic"
    ],
    
    "dimensions": {
        "width": "110cm",
        "height": "110cm",
        "depth": "50cm"
    },
    
    "category": {
        "name": "Tableware",
        "slug": "tableware"
    },
   
    "price": 980,
    
    "tags": [
        "popular products"    
    ] 
  }
]


## Importing Api data into my sanity project.

To import api data in my sanity projects i followed these steps.

### 1. cloned this repo ``https://github.com/bilalmk/hackathon-template02.git`` using following command:

 ``git clone https://github.com/bilalmk/hackathon-template02.git``

note it is not necessary to clone this repo in your project.I suggest you to clone
this repo outside of your actual project.

### 2. Navigate to the sanity-migration folder and run the following command

Open the command prompt in ``sanity-migration`` floder and run the following command:
 
 ``npm install``

![example](/images/example.jpg)

### 3. create a .env in sanity-migration folder and define following three variables and values

__projectId: Your Sanity project ID.__

__dataset: Your Sanity dataset name__

__token: Your Sanity token (if required).__

### 4. Run the Script:

node importData.js

![example](/images/example-2.jpg)

This will fetch the data from the API and import it into your Sanity project.

## Following are the schema you can use to update sanity records after migration

**ProductsSchema:**
https://github.com/bilalmk/hackathon-template02/blob/main/schema/product.ts

**CategorySchema:**
https://github.com/bilalmk/hackathon-template02/blob/main/schema/product.ts

After adding these schema types in your index.ts file your products will be shown in Sanity.

![productsInSanity](/images/sanity-products.jpg)