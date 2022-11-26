# Mongodb - Laravel installation and integration
This is the process on how to install mongodb compass , mongodb php driver and Laravel integration.
#### Download and Install Mongodb compass
- You can download mongoDb compass [here](https://www.mongodb.com/try/download/compass). You select any solutions that you want. I chose the community edition. `NOTE: ` For MongoDB Community Server version 6, you need to install [mongoDB Shell](https://www.mongodb.com/try/download/shell).
- Install the downloaded  Mongodb Compass. It will start after the installation.
- Extract mongosh(mongoDb Shell) in C drive `C:\mongosh-1.6.0-win32-x64`. You can find then installed MongoDb in your Program Files.
#### Add the path your environment variables and create data folder.
- Set  the mongosh path `C:\mongosh-1.6.0-win32-x64` and mongodb `C:\Program Files\MongoDB\Server\6.0\bin` path to system variables.
- create db folder in your C drive and create db folder under it. `C:\data\db`
#### Check mongo db in command prompt.
- Open command prompt. run `mongod`, `mongod --version`, `mongosh` in your terminal to check if you successfully install mondoDB.
- If you encounter `'mongo' is not recognized as an internal or external command, operable program or batch file` error. Try this [solutions](https://stackoverflow.com/questions/51224959/mongo-is-not-recognized-as-an-internal-or-external-command-operable-program-o) from [stackoverflow](https://stackoverflow.com/questions/51224959/mongo-is-not-recognized-as-an-internal-or-external-command-operable-program-o).
#### Download and install MongoDb PHP Driver.
- Check the version of PHP in your local machine. Run `php -v` in your command prompt. 
- Go to [PECL](https://pecl.php.net/package/mongodb/1.8.0beta1/windows) to download The PHP MongoDb Extension. Make Sure to select the DLL that matched your PHP version.
- Go to the downloaded php_mongodb file. You can extract all or just copy the `php_mongodb.dll` file. 
- Go to xampp folder. Open php extension folder (C:\xampp\php\ext) adn paste the dll file.
- Open `php.ini` file in your editot (NotePad or VS Code). and add `extension=php_mongodb.dll` in the extensions section. 
- From here we can use or add MongoDB PHP Library like `composer require mongodb/mongodb` or `Jenssegers` library for our Laravel project.
## Sources 
- [Stack OverFlow](https://stackoverflow.com/).
- [MongoDb](https://www.mongodb.com/home).
- [MongoDb PHP Driver ](https://www.mongodb.com/docs/drivers/php/).
- [Jenssegers/laravel-mongodb](https://github.com/jenssegers/laravel-mongodb)
## Acknowledgement
- Youtube - [Juniors raw code](https://www.youtube.com/watch?v=QAMl_fZIGE0&t=16s)
