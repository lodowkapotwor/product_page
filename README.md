### Which components should this page consist of?
Navigation bar:
  - MobileMenu
  - GoToHomepageButton
  - SearchComponent
  - FavoritesComponent
  - ShoopingCartComponent
  - AuthComponent
  
Product Showroom section:
  - CarouselComponent
  - BreadcrumdComponent
  - ProductItemTitle
  - ProductItemPrice
  - 2x ItemOptionsComponent
  - InputComponent
  - AddToCartComponent
  - AddToFavoritesComponent
  - AddToCompareComponent

Product details section:
  - ProductDetailsDescription
  - ProductDetailsAttributes
  
Reviews section:
  - ReviewDescription
  - ReviewSubmitForm

Related and Similar products:
  - SectionTitle
  - ProductCard

Ad banner

Newsletter
  - NewsletterDescription
  - NewsletterSubmitForm
  
Footer: 
  - FooterLinksList
  - FooterSocialContainer


### How to maintain the core/theme separation? 
Project should contain 2 main separated sections for components. Core and CustomComponents.
Core can be created for each project or injected as library/framework. 

#### Core:
  - Whole logic responsible for fetching data, filtering and validation. Also routing, tracking and data storage.
  - Second part of core should contain more project/framework-related functionality like for eg. for e-commerce. There would be components like AddToCart, ProductItem, CarouselContainer etc.

#### CustomComponents:
  - In vue we can extend core components using mixins, each one or create library. Custom components like eg. ProductShowroom needs to use carousel but always with different styles, content. We can create html markup and styles inside of ProductShowrom, here we can also set which data should be passed into carousel. We will inherit main functionality like slides movement, next/back arrows. 




In my example I wanted to show simple way to create own html markup for components and extends core logic.

Product.Vue is an example of core part. It contain default settings and default functions related to every product.

ProductCard.Vue extends Product and pass data from Application. ProductCard is custom one, it has his own markup but like other components it needs to use some base functionality like AddToCart. 

App.vue can be a main component like ProductPage. It will contain layout, order of components and also it's a place where main data should be passed into business part of project like product-name(from my example). ProductCard is a proxy between client side of app and core.



### Project setup
```
yarn install
yarn run serve
```
