# Docker weex
Non-interactive FTP client for updating web pages

Weex is an utility designed to automate the task of remotely maintaining a web page or other FTP archive. With weex, the maintainer of a web site or archive that must be administered through FTP interaction can largely ignore that process. The archive administrator simply creates a local directory that serves as an exact model for the off-site data. All modifications and direct interaction is done locally to this directory structure. When the administrator wishes to coordinate the data on the remote site with that of the local model directory, simply executing weex accomplishes this in the most bandwidth-efficient fashion by only transferring files that need updating. The program will create or remove (!) files or directories as necessary to accurately establish the local model on the remote server.

# Build the image

docker build -t jeko/weex:latest .

# Usage

```sh
$ docker run --rm -it jeko/weex [OPTIONS] HOST...

options:
  -h | --help           display this help and exit
  -s | --silent         suppress normal non-error messages
  -f | --force          force sending all files
  -m | --monochrome     output messages in monochrome
  -t | --test           not modify remote files
  -r | --rebuild-cache  rebuild cache file
  -d | --debug-config   display configuration of each hosts
  -D | --debug-ftplib   output debugging information for ftplib
  -V | --version        display version information and exit
```
