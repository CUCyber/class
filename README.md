Cybersecurity Seminar Class Presentations
=========================================

In this repository are the markdown sources to presentations given by the cybersecurity seminar at Clemson.


## Dependencies

* make
* git
* rsync
* python3
* python3-watchdog (optional; for automatic rebuilding on presentation change)


### Get Repository 

```sh
$ git clone https://github.com/CUCyber/class.git
```


### Debian/Ubuntu/Kali

```sh
$ sudo apt install make git rsync python3 python3-watchdog
```


### RedHat/CentOS

```sh
$ sudo yum install epel-release
$ sudo yum install make git rsync python36
$ sudo pip3 install watchdog
```


### Fedora

```sh
$ sudo dnf install make git rsync python3-watchdog
```


### Arch

```sh
$ sudo pacman -S make git rsync python-watchdog
```


### Gentoo

```sh
$ sudo emerge dev-vcs/git dev-python/watchdog
```


### macOS

Requires [Homebrew](https://brew.sh/). Use `gmake` instead of `make`.

```sh
$ brew install make git rsync python3 wget
$ pip3 install watchdog
```


## Building

To build all of the presentations into a hostable directory, edit the 'makefile' as desired and run `make`. All of the necessary files that should be put on a web server will be created in the 'public' directory.


## Testing

To build all of the presentations and host them on a temporary local server, edit the 'makefile' as desired and run `make serve`. Open your web browser to 'http://localhost:8080/'.


## Updating

To build all of the presentions and upload them to the website automatically, edit the 'makefile' as desired and for the website git repository location and run `make update`. You must have push access to the repository at the specified directory.


## Cleaning

To clean out any generated files, run `make clean`.


## Presenting

The presentations are easy enough to give, but can be improved by using speaker view. To pull up speaker view, press 's' from the presentation. This opens a page that includes a timer, speaker notes, and images of the current and next slides. If not using the multiplex described below, add `?present` to the end of the URL to remove speaker notes from the shown slides.

## Output to PDF

Use `?print-pdf`to output the slides to a pdf format.


### Multiplex

Each presentation can be configured as a presentation master that can control receiving instances of the presentation. This means that from one computer, you can control movement of the slides on several other computers. Additionally, this removes visible speaker notes from the receiving instances.

To make a presentation the master, add `?master` to the end of the URI but before the `#` if there is one. For each receiving instance, add `?receiver` to the end of the URI but before the `#` if there is one. You must load the master presentation first to generate the key that the receiver instances will retrieve.
