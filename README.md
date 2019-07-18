# A "go" short-link service

_This service is a fork of [Kelly Norton's golinks implementation](https://github.com/kellegous/go)_

## Background

From Kelly's description:

> The first time I encountered "go" links was at Google. Anyone on the corporate network could register a URL shortcut and it would redirect the user to the appropriate page. So for instance, if you wanted to find out more about BigTable, you simply directed your browser at http://go/bigtable and you would be redirected to something about the BigTable data storage system. I was later told that the first go service at Google was written by [Benjamin Staffin](https://www.linkedin.com/in/benjaminstaffin) to end the never-ending stream of requests for internal CNAME entries. He described it as AOL keywords for the corporate network. These days if you go to any reasonably sized company, you are likely to find a similar system. Etsy made one after seeing that Twitter had one ... it's a contagious and useful little tool. So contagious, in fact, that many former Googlers that I know have built or contributed to a similar system post-Google. I am no different, this is my "go" link service.

## Installation

We use this tool as a Docker image which can be found [here](https://cloud.docker.com/u/buzzfeed/repository/docker/buzzfeed/golinks/tags).

## Setup

There are several ways you can setup the `go` domain. If you are in a VPN, this will be relatively straightforward.

Fortunately or unfortunately (depends on how you look at it) for us, we don't use a VPN. We use an internal service for auth based on Beyond Corp's zero trust policy called [SSO](https://github.com/buzzfeed/sso/). In order for us to set this up, we had to add a search domain to  `resolv.conf` across company computers (accomplished using jamf).

## Using the Service

Once you have it all setup, using it is pretty straight-forward.

### Create a new shortcut

Type `go/edit/my-shortcut` and enter the URL.

### Visit a shortcut

Type `go/my-shortcut` and you'll be redirected to the URL.

### Shorten a URL

Type `go` and enter the URL.
