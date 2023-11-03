# SymPHP
SymPHP is a concolic execution engine for PHP-based applications leveraging the idea of symbolic interpreter analysis. It uses a modified S2E concolic execution engine on an enhanced PHP interpreter to realize this purpose.

We will release SymPHP soon!

## Installation
1. Install S2E
We forked and enhanced various components of S2E.
Follow the building [instructions](https://s2e.systems/docs/s2e-env.html#id2) to install our modified S2E. 

- 1.1. Dependencies
S2E has several dependent packages and libraries, which can be found in the [Dockerfile](https://github.com/secureweb/s2e/blob/master/Dockerfile).

- 1.2. s2e-env
```sh
sudo apt-get install git gcc python3 python3-dev python3-venv

git clone https://github.com/secureweb/s2e-env.git
cd s2e-env

python3 -m venv venv
. venv/bin/activate
pip install --upgrade pip

pip install .
```

- 1.3 S2E
```sh
# after starting the venv above, create a new S2E analysis env in /home/user/s2e
s2e init /home/user/s2e 

cd /home/user/s2e && source s2e_activate

s2e build
```

2. Install PHP interpreter
```sh
# clone our modified PHP interpreter first.
git clone https://github.com/secureweb/php-src
cd php-src

# we provide two versions PHP7 and PHP8
git checkout symphp-7
# git checkout symphp-8

./install-php.sh
```

## Use
TODO.

## License
SymPHP is under MIT License. 
SymPHP uses various libraries that may have their own licenses.
Please refer to the LICENSE file in each directory or to the header of each source file.