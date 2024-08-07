PRODUCT CREATION - (PRODUCT MODULE ASSIGNMENT)
Using EntityEngine

Step 1 - Create a new product by entering all the required fields. Select is Virtual Product as Y
For Parent Product . Click on Create Product.

![alt text](images/1.png)
Fig 1.1

Step 2 - Create a new Product that is supposed to be a variant of the base product or parent product . Change the ProductID in order to avoid duplicate Key error.Set isVirtualProduct as N and isVariantProduct as Y , as this will be a Variant of the base product as seen in Fig1.2

![alt text](images/2.png)
Fig1.2

Step 3 - In the entityEngine web tool , search for productAssoc in order to associate a variant product to a base product. In ProductID set the base product ID , and in the ProductID to set the variant product id . Set the ProductAssocType as VARIANT_PRODUCT to justify the variant product and also set the From date which is a required field. as seen in Fig1.3

![alt text](images/3.png)
Fig1.3

Step 4 - To verify if the Variant Product is setted to its Base Product , in the entity engine go to ProductAssoc and search the product using Parent Product ID as seen in Fig1.4, here we can notice the association of our variant product with our base product

![alt text](images/4.png)
Fig1.4



USING XML

In the webTool -> import/export -> XML DataImport , by this we can write XML code with ProductAssoc fragment to associate a Child Product i.e a Variant Product with its Base Product i.e Parent Product as seen in Fig2.1

![alt text](images/5.png)
Fig2.1

![alt text](images/4.png)
Fig2.2
Associating Product With Store

First we create a new Product Category so that we can link the product with the productCategory. as seen in Fig3.1

![alt text](images/6.png)
Fig3.1

In order to link the Product with product category we will use ProductCategoryMember which is an assoc entity as seen in Fig3.2

![alt text](images/7.png)
Fig3.2


Now we have to create a new product catalog for our new product.We can do that by creating a new catalog from entity engine as seen in Fig3.3
![alt text](images/8.png)
Fig3.3

Now that we have created a new product catalog , we can link product catalog and product category using ProdCatalogCategory which is an assoc Entity. We can link both catalog and category by added their Unique id’s in the assoc entity.as seen in Fig3.4

![alt text](images/9.png)
Fig3.4

Now to show our product in the store we can make a new store , by using productStore entity from entityEngine. For that we can set a unique ID to store and give it a name.as seen in Fig3.5
![alt text](images/10.png)
Fig3.5

In order to link product store and product catelog we will use another assoc entity that is Product store catalog , where we can enter unique id’s of both Product Store as well as Prod Catalog .
as seen in Fig3.6

![alt text](images/11.png)
Fig3.6

Now that we have completed all the steps , we can check our product by running this query

![alt text](images/12.png)
Fig3.7

![alt text](images/13.png)
Fig3.8

Here is the result as seen in Fig3.8

![alt text](images/14.png)
![alt text](images/15.png)
![alt text](images/16.png)
![alt text](images/17.png)









