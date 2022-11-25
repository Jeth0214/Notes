
# How to fix laravel composer update  error on unmatched PHP version
 When running `composer update` in newly cloned laravel repo and got like this problem in terminal.

```
Root composer.json requires php ^7.1.3 but your php version (8.1.6) does not satisfy that requirement.
or
script @php artisan package:discover handling the post-autoload-dump event returned with error code 255
```

There is a big possibility that your xampp or PHP installed in your machine didn't match the repo.
Also, be sure to  create `.env` copy all details from `.env.example` and paste it in your newly created `.env` file. 

### To fixed the error:

- #### Check the PHP version installed in your machine.  
    - run `php -v` in your terminal. Open the `composer.json` file and check the php version of the laravel project matches the version on your terminal.
    ```
    "require": {
        "php": "^7.1.3",
        ...some packages
    },
    ```
- #### Rename your installed xampp  in your machine like to its version.
    `C:\xampp` to `C:\xampp816`

- #### Download and Install the desire xampp version [here](https://sourceforge.net/projects/xampp/files/XAMPP%20Windows/). The installation includes Apache distribution containing MySQL, PHP, and Perl. You will see the newly installed xampp at `C:\xampp`.

- #### Add the php path in environment variables.
    - Open  **Edit the environment variables** on searchbar located at the taskbar.
    - Click **Environment Variables** at **Advanced** tab.
    - Click **path** on system varibles and click  **Edit** button.
    - Click **Edit** in the newly showed modal and paste the php path file under the newly installed xampp.
        ` C:\xampp\php `.
- #### Reopen the command prompt and run `php -v`. If it is successfully changed to the desire version. Go to your Laravel project and run `composer update`.  