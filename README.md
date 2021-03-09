# Bugger
Bug reporting made easier.

## Project Description

This is a web application that allows users to report issues with software applications, by selecting a product's specific product area - and listing out the specific reports. These reports would be mapped to the corresponding products.

This project uses three main models, based on [Django](http://www.djangoproject.com/)'s Model-View-Template (MVT) pattern:

* `Report`: This is the main model that the application is about. It
  contains the fields `id` (primary key), `title`, `description` (text field), `client_id`
  (foreign key to Product model),
  `priority` (integer field, will be unique for each product's bug
  report), `target_date` (the desired date for this feature request) and 
  `product` (foreign key to the `ProductEnum` model)
* `Product`: This is a model with a name that will be used to persist the
  products that have the bug issues
* `ProductEnum`: Another model similar to Product, will persist the product
  areas of each bug report.
