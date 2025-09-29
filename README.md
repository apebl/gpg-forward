# gpg-forward

A simple script to forward the GPG agent to a remote system over SSH. This
allows you to use GPG on the remote system while keeping your secret keys on
your local machine.

Note: The remote system still needs the corresponding GPG public keys locally.

## Installation

It's just a script file. Copy the file to your PATH. e.g.:

```sh
curl -sSL https://apebl.github.io/gpg-forward/gpg-forward | sudo tee /usr/local/bin/gpg-forward
sudo chmod +x /usr/local/bin/gpg-forward
```

## Usage

```
$ gpg-forward -h
Usage:
  gpg-forward [OPTIONS] DEST
Options:
  -t DURATION  Close session after DURATION
  -h           Print this help message

DURATION is a floating point number with an optional suffix:
s for seconds (default), m for minutes, h for hours, or d for days.
```

```
$ gpg-forward user@remote
Connected
```

## Links

- https://wiki.gnupg.org/AgentForwarding

