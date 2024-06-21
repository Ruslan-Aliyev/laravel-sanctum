# Laravel Sanctum Token

Main tutorial: https://www.youtube.com/watch?v=ajUST-jUMeg

```
composer require laravel/sanctum
php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
```

Use the `Laravel\Sanctum\HasApiTokens` trait in the `User` model.

Ready the DB seeder.

Finish the controller and routes.

In Laravel 11, remember to run: `php artisan install:api`.

```
php artisan migrate:fresh --seed
php artisan serve
```

Login (get token):
```
curl --location 'http://127.0.0.1:8000/api/login' \
--form 'email="test@example.com"' \
--form 'password="password"'
```

See your own info using token:
```
curl --location --request POST 'http://127.0.0.1:8000/api/me' \
--header 'Authorization: ••••••'
```

---

You can also generate token like this: `$user->createToken('token-name', ['server:update'])`

then:  
```php
if ($user->tokenCan('server:update')) {
    // return 403 error
}
```

- https://laravel.com/docs/8.x/sanctum#token-abilities

- https://medium.com/@abdelra7manabdullah/api-authentication-using-laravel-sanctum-v10-x-21dfe130cda
- https://flixtechs.co.zw/posts/how-to-authenticate-apis-with-laravel-sanctum
- https://viblo.asia/p/tao-api-va-authenticate-nhanh-chong-voi-package-laravel-sanctum-eW65G1EJZDO

- https://stackoverflow.com/questions/77035623/what-are-the-technical-differences-between-using-laravel-sanctum-vs-tymon-jwt-au
- https://fkrihnif.medium.com/laravel-sanctum-laravel-passport-and-jwt-unveiling-the-guardians-of-laravel-authentication-a9953aed1132
