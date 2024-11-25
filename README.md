# 2420-Assignment-3
### Assignment 3 Linux

#### Click on the link to visit the working server [164.92.88.167](http://164.92.88.167/)

If you also want to also setup a new server, this is a quick guide to help you do that.


## Setting Up a New Server

#### Intial Step
We will be creating a user, using the following command:

``` linux
sudo useradd --system -d /var/lib/webgen -s /usr/sbin/nologin webgen
```

This will simply create a system user for you called `webgen`

#### Create Directories and Changing Ownership
Now we'll make directories for the necessary files inside of webgens home directory
``` linux
sudo mkdir /var/lib/webgen/HTML
sudo mkdir /var/lib/webgen/bin
```
We will run the following command
``` linux
sudo chown -R webgen:webgen /var/lib/webgen
```

This ensures that the ownership is changed to our new user `webgen` for all directories we've created and other directories inside of `/var/lib/webgen`

`webgen` user tree should look like the following:

``` linux
/var/lib/webgen/

├── bin/
│   └── generate_index   # copy the generate_index into bin
└── HTML/
    └── index.html       # copy the index.html into HTML folder
```

#### Move .service and .timer Files
