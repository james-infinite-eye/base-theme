## Output Images

### Display image full size
```php
echo \InfiniteEye\Theme\Media::image(6);
```

### Display image relative to assets/img path
```php
echo \InfiniteEye\Theme\Media::image('image.png');
```

### Display image from acf field
```php
echo \InfiniteEye\Theme\Media::image(get_field('profile_image'));
```

### Output image specific size
```php
echo \InfiniteEye\Theme\Media::image(6)
    ->size('thumbnail');
```

### Output image dynamic size
```php
echo \InfiniteEye\Theme\Media::image(6)
    ->size(100);
```

### Output image with specific srcset sizes
```php
echo \InfiniteEye\Theme\Media::image(6)
    ->srcset([
        // at 1024 display 400px wide image
        1024 => 400,
        // at 768 display 200px wide image
        768 => 200,
        // at 480 display 100px wide image
        480 => 100
    ])
    ->size(500);
```