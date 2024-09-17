# Start PHP before you can run laravel:
`brew services start php`

<br>

# How to create a new laravel project:
`composer create-project laravel/laravel <app_name>`

<br>

# How to start laravel's local development server:
`php artisan serve` 

<br>

# Where to store images in laravel?

- ***You have to distinguish between publicly available images like a banner, background etc and restricted ones. The former can and should go in public/images.***

<br>

- ***But for user profile photos, I'd suggest keeping them somewhere safe and not public. E.g. if you put them in storage/images/profiles/, access them like this:***

`use Intervention\Image\Facades\Image;`

`public function getImage($image_path)`
`{`
        `// Check if the visitor/user is allowed to view the image.`
        `return Image::make(storage_path('/images/profiles/') . $image_path)->response('jpg');`
`}`
