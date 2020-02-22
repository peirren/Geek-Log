---
layout: post
title: "Shopline theme notes"
date:   2020-02-11 10:30:00 +0800
---

### [Theme templates](https://help.shopify.com/en/themes/development/templates)
Shopify themes are made up of Liquid template files, each serving their own unique purpose. For example, collection.liquid is used to display multiple products, and product.liquid is used to show the details of a single product. Shopify themes also include a settings_schema.json file, which is a form that makes it easy for the user to customize the look-and-feel of the theme.

### Theme structure
A Shopify theme includes the following directories:

- assets
- config
- layout
- locales
- ections
- nippets
- emplates

### Shopline官方資源
- HOPLINE Layout Document：https://shopline-layout.readme.io/docs
- Github Liquid Document：http://shopify.github.io/liquid/
- Liquid template language：https://getbootstrap.com/

1. Step 1: Install Theme Kit
2. Step 2: Setting up API credentials
3. 


Entering Shopfiy Parterner
1. App > Manage private apps
2. Create private app: Admin API > Theme templates and theme assets > Read and write Save
3. theme get --password=[your-api-password] --store=[your-store.myshopify.com] --themeid=[your-theme-id], replacing the [square bracket placeholders] with your own information.
4. Creating a theme from scratch
[Reference](https://www.shopify.com/partners/blog/95401862-3-simple-steps-for-setting-up-a-local-shopify-theme-development-environment)
5. Push updates to your theme : `theme watch` _automatically_ push them to your theme!


- API password
- URL paht
- Theme ID

- - -
theme get --list -p=[0e074e40c32ac19fc72ac9075ccaa9d0] -s=[randy24app.myshopify.com/]


theme get --password=c3ecf901dd7ea8f7e278931c3da5478c --store=randy24app.myshopify.com --themeid=89046155397


theme get --password=01464d4e02a45f60a23193ffc3a8c1b3 --store=the-soap-store.myshopify.com --themeid=170199178
- - -
#### Reference
[A comprehensive list of articles about Shopify Theme Development](https://www.shopify.com/partners/blog/topics/shopify-theme-development)







