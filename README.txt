Assorted OpenCart vQmods
========================
A collection of my vQmods for OpenCart 1.5.6. See below for details on each mod.

Note: Other than the mod files in this directory, I'm in no way affiliated with the modules that they may enhance. The modules that my particular vQmods affect are written by other authors and might be commercial products, that can be bought from various OpenCart extensions catalogs.

All product and company names are trademarks™ or registered® trademarks of their respective holders. Use of them does not imply any affiliation with or endorsement by them.


General Requirements
====================

 - OpenCart 1.5.6
   http://www.opencart.com/index.php?route=download/download

 - vQmod 2.X
   https://github.com/vqmod/vqmod


Installation
============
To install any vQmod file copy it to 'vqmod/xml/' in your OpenCart installation directory directly, or use vqModManager (or similar tool) to istall the mod from your site's admin interface.


vQmods descriptions
===================

Admin Link to Product Page
--------------------------
Adds a button to "Product" add/edit page in admin interface, which when clicked opens that product page on shop frontend.


Admin Order Auto Copy Fields on Input
-------------------------------------
A little jQuery JavaScript for "Order" creation form in admin interface, that automatically copies input made to "Payment" form part to "Shipping" form part. Since most of the time the order is paid and received by the same person it's annoying and error prone for a manager to type in the same information to "Buyer information", "Payment" and "Shipping" form parts. This mod will automatically copy fields from "Buyer information" form part to "Payment" form part, and every field from "Payment" form part to "Shipping" form part once the field looses focus, if the destination form's field is empty. Therefore if these data should differ the input should be performed in reverse order. 
This enhancement greatly decreases the time needed for the manager to add the new order from admin interface. 
There are also a few commented lines in 'admin_order_auto_copy_fields_on_input.xml' which allow to automatically preselect "Country", "City" based on "_zone_id" and vice versa. These might be useful if most orders are made to the same location. You might need to uncomment and edit those to fit your situation.


Products Default Sort by Quantity
---------------------------------
Changes default sorting rule for product listings to "Quantity Descending"  for: Category, Manufacturer, Search and Special pages. This leads to "Sold Out" products being displayed last. This enhances the user experience in a way, that a user doesn't spend time scrolling products she/he won't be able to buy anyway.


Show Options on Product Listing Pages
-------------------------------------
Adds options displaying below product name for every product with options on all product listing pages: Category, Search, Manufacturer, Special, Bestseller module, Featured module, Latest module, Special module. Also supports FilterPro(separate commercial module) results page. Options names and values are used from standard OpenCart options created in admin interface. To modify the styling, see the first 'file' block in 'show_options_on_product_listing_pages.xml'.


Show Package Weight and Size on Product Page
--------------------------------------------
Adds package weight and size display to every product page near other product info like product code, available quantity, etc.. The values are taken from standard OpenCart data for every product, set via product edit form in admin interface. To modify the display styles see the last 'file' block in 'show_package_weight_and_size_on_product_page.xml'.


Spoiler Mod for FilterPro
-------------------------
A little jQuery JavaScript for FilterPro filters block, that allows to display only "main" filters initially and show more once the "Show filters" is clicked. See 'spoiler_mod_for_filter_pro.xml' to modify the height of the block with initial "main" filters for your setup and styling.
Requires: "FilterPro" module.


Twitter Export admin menu mod
-----------------------------
Adds a shortcut link for "Twitter Export" module in admin menu.
Requires: "Twitter Export" ("Экспорт в Твиттер") module


VK Export admin menu mod
------------------------
Adds a shortcut link for "VK Export" module in admin menu.
Requires: "VK Export" ("Экспорт в ВКонтакте") module


Yandex.Market Feed Free Delivery and Custom Vendor Code Mod
-----------------------------------------------------------
Initially "Yandex.Market feed" doesn't support providing variable delivery cost for each product. In the module settings you set delivery price and in the feed it's the same for every product. However it's common for shops to have a price threshold for items, above which the delivery is free.
This module does exactly that... It allows to set a price threshold in "Yandex.Market feed" settings interface in admin. When the feed is created, the products with the price above the specified threshold will have their delivery cost set to zero in the resulting feed, while other products will have the default delivery cost.
Another problem solved by this mod is... Yandex.Market feed format has "Vendor code" field, which is used by the Market itself to decide in which product's card to put your offer. If this field is filled with the OpenCart's "Product code" product field, which usually contains shop's own code for each item, your offer might get a separate product card (which most likely will be put in the end of search results) or just be put in the wrong product card on the Market. In order to fix this issue, create an attribute for products which will contain manufacturers code for each product and use this mod. This mod adds a setting to "Yandex.Market feed" settings interface in admin, that allows you to choose the attribute name containing manufacturers code. The value from the specified attribute for each product will be put in that product's "Vendor code" field in resulting feed.
Note: The mod works as is if the feed is made dynamically by OpenCart on request from the Market. But it the feed is formed manually or by Cron job, then vQmod is not used and this mode will not take its effect. If you use Cron to form the feed beforehand, then you'll have to manually modify the "Yandex.Market feed" module file. See comments in 'yandex_market_feed_free_delivery_and_custom_vendor_code_mod.xml' to know what to modify.
Requires: "Yandex.Market feed" ("Выгрузка в Яндекс.Маркет") module


LICENSE
=======
The MIT License (MIT)

Copyright (c) 2014 Nikita Solovyev

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.