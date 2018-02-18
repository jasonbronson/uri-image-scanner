# uri-image-scanner
Wordpress plugin to scan and read all images in a directory based on URI

Example
If you had an image slider you could use like this

```
<div class="images-gallery">
        <ul id="lightSlider">
            <?php foreach ( UriImageScanner::getPictures() as $index => $folder ): ?>
                     <li data-thumb="<?php echo $folder['relativepath']; ?>/<?php echo $folder['filename']; ?>" data-src="<?php echo $folder['relativepath']; ?>/<?php echo $folder['filename']; ?>">
                        <img src="<?php echo $folder['relativepath']; ?>/<?php echo $folder['filename']; ?>" class="img-responsive" />
                     </li>
            <?php endforeach; ?>
         </ul>
</div>
```

And the results in the page from a path like  /bella-sirena-1/

```
<li data-thumb="/wp-content/uploads/bella-sirena-1/159d071b-bc84-44cb-a79b-edb55181b6d4.c10.jpg" data-src="/wp-content/uploads/bella-sirena-1/159d071b-bc84-44cb-a79b-edb55181b6d4.c10.jpg">
                                                        <img src="/wp-content/uploads/bella-sirena-1/159d071b-bc84-44cb-a79b-edb55181b6d4.c10.jpg" class="img-responsive" />
                                                    </li>
                                                    
```                                                    
