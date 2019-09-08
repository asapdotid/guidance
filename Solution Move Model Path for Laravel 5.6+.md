# Solution for Laravel 5.6+

## 1. Move the files to the new directory

Say you want to move the models to `app/Models`

## 2. Change the namespace of the models

For each model change :

> `namespace App;`

to

> `namespace App\Models;`

## 3. Change the references in other files

Check these files and search especially `app\User`

* `app/Http/Controllers/Auth/RegisterController.php`
* `config/auth.php`
* `config/services.php`
* `database/factories/ModelFactory.php`
* `database/factories/UserFactory.php`
* `Your Controllers`

And change `App/ModelExample` to `App/Models/ModelExample`

## 4. Autoload files

Run `composer dump-autoload`

Done congratulations!
