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
