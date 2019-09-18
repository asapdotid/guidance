# Update NPM on NVM

## Use CMD (AppData\Roaming\nvm\v10.16.3)

``` bash
cd %APPDATA%\nvm\v10.16.3
move npm 6.9.0
move npm.cmd 6.9.0.cmd
cd node_modules\
move npm 6.9.0
cd 6.9.0\bin
node npm-cli.js i -g npm@latest
```

* Done

> Remove old npm in (AppData\Roaming\nvm\v10.16.3)

``` bash
rmdir /s /q "node_modules\ 6.9.0"
del /f 6.9.0 6.9.10.cmd
```

## Use Git Bash (AppData\Roaming\nvm\v10.16.3)

``` bash
cd AppData\Roaming\nvm\v10.16.3
mv npm 6.9.0
mv npm.cmd 6.9.0.cmd
cd node_modules\
mv npm 6.9.0
cd 6.9.0\bin
node npm-cli.js i -g npm@latest
```

* Done

> Remove old npm (AppData\Roaming\nvm\v10.16.3)

``` bash
rm -rf "node_modules\ 6.9.0"
rm -f 6.9.0 6.9.10.cmd
```
