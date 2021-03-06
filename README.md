featured_image
=========================================================================================
A [Zenphoto20](https://github.com/ZenPhoto20/ZenPhoto20) plugin to attach an image from the gallery to a Zenpage article, category or page as an "featured image". You can use this image for example for headers of your single article/page/category pages or within the news article list as a thumbnail. 

The benefit compared to the embedding an image within the text content statically is that you can control the size of it via your theme's layout dynamically as with gallery items.
 
 
Put the file in your `/plugins` folder. Your theme requires support for it. To use it you need to modify your theme used if it has no built in support already. 

##Usage examples:
  
###a) Object model 

```php
$featuredimage = getFeaturedImage(<object of the Zenpage item>);
if($featuredimage) { // if an feature image exists use the object model
  ?>
  <img src="<?php echo pathurlencode($featuredimage->getThumb()); ?>" alt="<?php echo  html_encode($featuredimage->getTitle()); ?>">
  <?php
}
```
  
###b) Theme function for pages.php and news.php for the current article, category or page
```<?php printSizedFeaturedImage(NULL,'My featured image',500); ?>```
   
Requirement: Zenpage CMS plugin and a theme supporting it

License: GPL v3

Based on acrylians [featured_image](https://github.com/acrylian/featured_image) for ZenPhoto.