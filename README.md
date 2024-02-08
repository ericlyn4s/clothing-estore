# Clothing E-Store

## Description

I created the clothing e-store to continue my learning about object relational mapping. I utilized my knowledge on models by creating four models and exporting these for use throughout the project. Each model contained fields with certain criteria, with some fields existing as primary or foreign keys in relation to one another. Using Sequelize, I created a database and seeded data into it. Finally, I incorporated my understanding of CRUD operations by creating routes for displaying, adding, adjusting or deleting the data within this database. The end product is an application that displays the inventory levels for different products for a hypothetical clothing store. Overall I found this project to be a culmination of the past three units, and found it satisfyingly challening to create the end product.

## Installation

My project can be forked from my GitHub repository here:

https://github.com/ericlyn4s/clothing-estore

## Usage

Two walkthrough videos of this application can be viewed below:

[Part 1: Models and seeding data into the database](https://www.youtube.com/watch?v=uJV85eveT4U) \
[Part 2: Running the server and executing CRUD operations](https://www.youtube.com/watch?v=U2xX3FmOVfo)

After forking the data, setup the .env file, install the necessary packages, seed the data and boot up the server as such:

1. `npm install dotenv`
2. `npm install i`
3. `npm install sequelize`
4. `npm install express`
5. `npm run seed`
6. `npm start`

The database should be correctly seeded and the server will be running at localhost:3001, or wherever you defined `PORT`. You can then boot up Insomnia and run the following CRUD operations:

1. GET all categories `http://localhost:3001/api/categories/`
2. GET one category `http://localhost:3001/api/categories/:id`
3. POST a new category `http://localhost:3001/api/categories/` - followed by new category information as a JSON request:

```
{
    category_name: "Sunglasses"
}
```

4. PUT a change onto an existing category `http://localhost:3001/api/categories/:id`- followed by adjusted category information as a JSON request:

```
{
    category_name: "Sunglasses"
}
```

5. DELETE a category `http://localhost:3001/api/categories/:id`

------------

6. GET all products `http://localhost:3001/api/products/`
7. GET one product `http://localhost:3001/api/products/:id`
8. POST a new product `http://localhost:3001/api/products/` - followed by new product information as a JSON request:

```
{
      product_name: "Basketball",
      price: 200.00,
      stock: 3,
      tagIds: [1, 2, 3, 4]
}
```

9. PUT a change onto an existing product `http://localhost:3001/api/products/:id` - followed by adjusted product information as a JSON request:

```
{
      product_name: "Basketball",
      price: 200.00,
      stock: 3,
      tagIds: [1, 2, 3, 4]
}
```

10. DELETE a product `http://localhost:3001/api/products/:id`

------------

11. GET all tags `http://localhost:3001/api/tags/`
12. GET one tags `http://localhost:3001/api/tags/:id`
13. POST a new tag `http://localhost:3001/api/tags/` - followed by new information as a JSON request:

```
{
    tag_name: "white shoes"
}
```

14. PUT a change onto an existing tag `http://localhost:3001/api/tags/:id` - followed by adjusted information as a JSON request:

```
{
    tag_name: "white shoes"
}
```

15. DELETE a tag `http://localhost:3001/api/products/:id`

<image src="assets/example_category_call.png" alt="Example call within Insomnia to the Category table." width="650"/>

## Credits

I had a tutor session with Charles Puente Matos on 2/7/2024.

## License

MIT License

Copyright (c) 2024 Eric Peterson

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
