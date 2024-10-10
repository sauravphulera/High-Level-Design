# High-Level-Design


## E Commerce App
**1.ConfiGurable UI - Home Page**
**2.Browse & Purchase**


**Functional Requirements** 

<code>Browse Product</code> 

 - Search 
  
 - Filter 
  
 - Product Listing 
  
 - Product Detail 

<code>Add to Cart</code> 

 - Chart Page 

 - Change Quantity 
  
 - Price Summary 
  

<code>Purchase Product</code> 

 - Checkout Page 
  
 - Address 
  
 - Apply Coupen 
  
 - Price Breakup 

**Non Functional Requirements** 

<code>Device Support</code> 

<code>Auth Layer</code> 

- Route Guards 

<code>i18/i10 (Different Languages)</code> 

<code>SEO</code> 

<code>Optimization</code> 

<code>Security</code> 


**Architecture**

<code>View</code>

- Browse Page Listing
- Product Detail Page
- Cart Page
- Checkout

<code>Storage</code>

- State Management Redux
- Browser Storage
- Service Worker
- API Cache Layer

<code>Controller</code>

- Search
- Filter
- Address
- Coupen
- Cart

<code>Service</code>
- Browse
- Adress
- Coupen
- Cart


**Data Model**

 <code>Product</code>

 - id
 - title
 - assets (image/video)
 - description
 - mrp
 - discounted price
 - currency

 <code>Cart Item</code>

 - id
 - productId
 - quantity
 - price(final price)

 <code>Address</code>

 - id
 - name
 - cuntry
 - state
 - city
 - pincode
 - landmark

 <code>Payment</code>

 - id
 - price
     - product prices
     - coupens
     - taxes
     - deivery charge

 <code>Coupen</code>

 - id
 - type (FIXED/ Percentage)
 - details
 - value
 - rules []


**API Requirement**
- Search/Filter. (OFFSET based pagination, cursor based pagination)
- Product Detail.
- Cart Update(Change quantity, ADD, Delete ).
- Cart Listing.
- GET payment summary.
- GET addresses, Add address(POST).
- GET coupens.
- PG related API (payment gateway).

**Optimization**
- Lazy loading/ code splitting
- ATF(Above the fold)
    - Defer/ async
    - prefetch
- web/cdn/ service worker, Lazy loading of images(load=lazy) | Image priority | Device Pixek ratio(DPI)
- Adaptive loading (depending on network quality)


**SEO**
<title></title>
<meta>
sitemap.xml (page with all possible links)
robots.txt (go to flipkart/robots.txt it contains what is allowed or disallowed)


