#  E-Commerce Back End

## Description
This is the back end for an e-commerce site, with Get, Post, Put and Delete catalogs that includes product, categories, tags. I uses Express.js API to use Sequelize to interact with a MySQL database.

![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)

  
## Table of Contents
* [Description](#description)
* [Walkthough](#walkthrou)
* [Installation](#installation)
* [Tests](#tests)
* [Contact](#contact)


## Installation
The package.json has everything you need, just tun "npm install", the folder structure is important so please be aware and do not change it. 
There is a sql for the database schema please run it using your user and credential
After that npm run seed to load the basic data before you test

## Tests
Just run "npm start", the aplication runs at localserver port 3001.
Please use insomnia or any tool you be familiar with to run the test, these are the routes you can test:
* Product: new product (POST), retrive all products (GET), select one product (GET), update product (PUT) and delete product (DELETE).
* Category: new category (POST), retrive all categories (GET), retrive one category (GET), update category (PUT) and delete category (DELETE). 
* Tag: new tag (POST), retrive all tags (GET), retrive one tag (GET), update tag (PUT) and delete tag (DELETE).



## Walkthrough Video

To see the use of the API watch this Walkthrough Video [Walkthrough Video](https://drive.google.com/file/d/1OZxSXJWvHqiLy1NfLcTojNMbfBgtxQWC/view)

### Database Models

The database contains the following four models:

* `Category`

  * `id`
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment.

  * `category_name`
    * String.
    * Doesn't allow null values.

* `Product`

  * `id`
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment.

  * `product_name`
    * String.
    * Doesn't allow null values.

  * `price`
    * Decimal.
    * Doesn't allow null values.
    * Validates that the value is a decimal.

  * `stock`
    * Integer.
    * Doesn't allow null values.
    * Set a default value of `10`.
    * Validates that the value is numeric.

  * `category_id`
    * Integer.
    * References the `Category` model's `id`.

* `Tag`

  * `id`
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment.

  * `tag_name`
    * String.

* `ProductTag`

  * `id`
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment.

  * `product_id`
    * Integer.
    * References the `Product` model's `id`.

  * `tag_id`
    * Integer.
    * References the `Tag` model's `id`.



## Technologies 

* JavaScript
* Node.js
* MySQL
* Express package
* MySQL2 package
* Sequelize package
* dotenv package
* Insomnia

## Autor
    For any question or inquiery
* GitHub: [mariopatino](https://github.com/mariopatino)

## License 
  This project is license under the "https://opensource.org/licenses/MIT"
