c5-example-package
==============================================

How to install
----------------------------------------------

### Download the concrete5

	wget https://github.com/concrete5/concrete5-5.7.0/archive/5.7.3.1.tar.gz
	tar zxvf 5.7.3.1.tar.gz

### Setup the composer

	cd concrete5-5.7.0-5.7.3.1
	composer init

### Edit the installation path

Open the **composer.json**.

	vi composer.json

Change the path of the **vendor-dir**.

```json
"config": {
    "vendor-dir": "web/packages"
}
```

Change the path of the **installer-paths**.

```json
"extra": {
    "installer-paths": {
        "web/packages/{$name}/": [
            "type:concrete5-package"
        ]
    }
}
```

### Install the package

	composer require composer/installers:~1.0
	composer require holyshared/c5-example-package:dev-master
