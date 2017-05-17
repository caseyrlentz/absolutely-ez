[logo]: http://i.imgur.com/OP9EOUP.jpg "ABSOLUTELY / EZ"
[config]: http://i.imgur.com/B4NXmci.png "Config settings"
[connection]: http://i.imgur.com/veE7UJ6.png "mysql connection"
![alt text][logo]
# ABSOLUTELY/AZ : 
### A DEAD SIMPLE VAGRANT BOX FOR EZ CMS

## Dependancies
1. GIT 
2. Vagrant
3. Virtualbox
4. Symfony ( specifically have the composer command availabile at a global level). 
5. Some way to interact with a Database ( Gui or Command line will do).


## GETTING UP AND RUNNING WITH ABSOLUTELY/EZ 
1. CLONE THIS REPO.
2. Create a `public/` folder next the the Vagrantfile.
3. Run `Vagrant up`.

## GETTING EZ CODE BASE
1. change directories into your newly created public directory `cd public`.
2. Clone the ez codebase into the public directory without any parent folder. ` git clone https://github.com/ezsystems/ezplatform.git .`. Please note the space and the period at the end of this commend.
3. run `composer install` inside of the public directory. This may take a minute to complete and you will most likely be asked to put in some configuration values. The values should be as follows: ![alt text][config]
4. `vagrant ssh` into the guest box and run `php -d memory_limit=-1 app/console ezplatform:install --env prod clean` to exe the EZ install command. Make sure you're in the correct directory `/var/www/public`.

## Connecting to a Database
1. If you use sequal pro your settings should look like this: ![alt text][connection]

2.You should now see the EZ platform at `192.168.33.10`. You can also log into the backend of ez via `/ez` using the `username: admin` and `password: publish`.

### Enjoy! If this was helpful in any way please share it.
### If you find any issues please log them in repo issue tracker. 


