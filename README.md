https://www.youtube.com/watch?v=ajUST-jUMeg

composer require laravel/sanctum
php artisan vendor:publish
	Provider: Laravel\Sanctum\SanctumServiceProvider

Use the Laravel\Sanctum\HasApiTokens trait in the user model.

Seed DB







$user->createToken('token-name', ['server:update'])





php artisan make:controller AuthController


finish the controller and routes

Laravel 11:

php artisan install:api




php artisan serve


curl --location 'http://127.0.0.1:8000/api/login' \
--form 'email="test@example.com"' \
--form 'password="password"'



curl --location --request POST 'http://127.0.0.1:8000/api/me' \
--header 'Authorization: ••••••'


https://medium.com/@abdelra7manabdullah/api-authentication-using-laravel-sanctum-v10-x-21dfe130cda
https://flixtechs.co.zw/posts/how-to-authenticate-apis-with-laravel-sanctum
https://viblo.asia/p/tao-api-va-authenticate-nhanh-chong-voi-package-laravel-sanctum-eW65G1EJZDO

https://stackoverflow.com/questions/77035623/what-are-the-technical-differences-between-using-laravel-sanctum-vs-tymon-jwt-au
https://fkrihnif.medium.com/laravel-sanctum-laravel-passport-and-jwt-unveiling-the-guardians-of-laravel-authentication-a9953aed1132
