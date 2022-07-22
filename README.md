# Site Connectivity Checker

> An application that checks if one or more websites are online at a given moment.

<a href="https://github.com/FernandoTorresL/rpchecker_project/commits/main" target="_blank">![GitHub last commit](https://img.shields.io/github/last-commit/FernandoTorresL/rpchecker_project)</a> <a href="https://github.com/FernandoTorresL/rpchecker_project" target="_blank">![GitHub repo size](https://img.shields.io/github/repo-size/FernandoTorresL/rpchecker_project)</a>

 The app will take a list of target URLs at the command line and check them for connectivity either synchronously or asynchronously.

Follow the tutorial [Build a Site Connectivity Checker in Python](https://realpython.com/site-connectivity-checker-python/) from [Real Python site](https://realpython.com)



## Installation

1. Create a Python virtual environment

OS X & Linux:

```sh
$ python -m venv ./venv
$ source venv/bin/activate
(venv) $
```

Windows:

```sh
$ python -m venv venv
$ .\venv\Scripts\activate
(venv) $
```
> This prompt may vary if you use another shell configuration, like pk10

Later, to deactivate the virtual environment
OS X & Linux & Windows:

```sh
(venv) $ deactivate
$
```

2. Install the requirements

OS X & Linux & Windows:

```sh
(venv) $ python -m pip install -r requirements.txt
```

## Run the project

```sh
(venv) $ python -m rpchecker -u python.org
The status of "python.org" is: "Online!" 👍
```
### Features

RP Checker provides the following options:

- `-u` or `--urls` takes one or more URLs and checks if they're online.
- `-f` or `--input-file` takes a file containing a list of URLs to check.
- `-a` or `--asynchronous` runs the check asynchronously.

Show the help message
```sh
(venv) $ python -m rpchecker -h
usage: rpchecker [-h] [-u URLs [URLs ...]] [-f FILE] [-a]

check the availability of websites

options:
  -h, --help            show this help message and exit
  -u URLs [URLs ...], --urls URLs [URLs ...]
                        enter one or more website URLs
  -f FILE, --input-file FILE
                        read URLs from a file
  -a, --asynchronous    run the connectivity check asynchronously
```

Check some urls
```sh
(venv) $ python -m rpchecker -u python.org pypi.org peps.python.org
The status of "python.org" is: "Online!" 👍
The status of "pypi.org" is: "Online!" 👍
The status of "peps.python.org" is: "Online!"👍
```

Results from a non existing site
```sh
(venv) $ python -m rpchecker --urls non-existing-site.org
The status of "non-existing-site.org" is: "Offline?" 👎
  Error: "[Errno 8] nodename nor servname provided, or not known"
```

Using a txt file with a list of urls
```sh
(venv) $ python -m rpchecker -f sample-urls.txt
The status of "python.org" is: "Online!" 👍
The status of "pypi.org" is: "Online!" 👍
The status of "docs.python.org" is: "Online!" 👍
The status of "peps.python.org" is: "Online!" 👍
```

Checking the sites asynchronously
```sh
(venv) $ python -m rpchecker -u python.org pypi.org peps.python.org -a
The status of "pypi.org" is: "Online!" 👍
The status of "python.org" is: "Online!" 👍
The status of "peps.python.org" is: "Online!"
```

### What learn with this project

- Create **command-line interfaces (CLI)** in Python with **argparse**
- Check if a website is online using Python’s **http.client**
- Run **synchronous** checks on multiple websites
- Check if a website is online using **aiohttp**
- Check the connectivity of multiple websites **asynchronously**

## About the original author

Leodanis Pozo Ramos - Email: leodanis@realpython.com
## Release History

* 0.0.1
    * Project ready with asynchronous requests

## Contributing

1. Fork it (<https://github.com/FernandoTorresL/rpchecker_project/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request
## Meta

<div align="center">
    <a href="https://fertorresmx.dev/">
      <img height="150em" src="https://raw.githubusercontent.com/FernandoTorresL/FernandoTorresL/main/media/FerTorres-dev1.png">
  </a>
</div>

#### :globe_with_meridians: [Twitter](https://twitter.com/FerTorresMx), [Instagram](https://www.instagram.com/fertorresmx/): @fertorresmx
