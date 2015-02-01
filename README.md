# Sharlin

An utility for sharing a secure web link to a given file on your computer using your NAS.

## Examples

#### Dropbox-like context menu

Right click on the given file and choose "Share NAS link". The link will be
copied to your clipboard.

#### Command line usage

    $ sharlin add ~/Desktop/screenshot.png
    https://your.domain/jkl2kyvtmt41dp7/screenshot.png

## Prerequisites

- A public IP address or a domain pointing out to your NAS.
- A static file web server on the NAS.
- An AFP share keeping the directory from which your web server takes files.
- Context menu works only on OS X.

## Install

    git clone https://github.com/AlexeyMorozov/sharlin.git
    cd sharlin
    cp sharlin /usr/local/bin/
    cp -R "context_menu/Share NAS Link.workflow" ~/Library/Services/
    cp sharlin.conf.example ~/.sharlin.conf
    open ~/.sharlin.conf

Then you need to set your domain, an AFP share URL, a mount directory and a
public web directory. After that just save the config and you're ready!
