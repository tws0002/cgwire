# Docker Zou

Docker container for [Zou](https://zou.cg-wire.com) and [Kitsu](https://kitsu.cg-wire.com/).

See [Gazu](https://gazu.cg-wire.com/) for details regarding the Python API towards this interface.

### Usage

```bash
$ docker build -t cgwire .
$ docker run -ti --rm -p 80:80 --name cgwire cgwire
```

In order to enable data persistence, use a named volume for database and thumbnails:

```bash
$ docker build -t cgwire .
$ docker run -ti --rm -p 80:80 --name cgwire -v zou-storage:/var/lib/postgresql -v zou-storage:/opt/zou/zou/thumbnails cgwire
```

Credentials:

* login: admin@example.com
* password: default


### About authors

This Dockerfile is written by CG Wire, a company based in France. We help small
to midsize CG studios to manage their production and build pipeline
efficiently.

We apply software craftmanship principles as much as possible. We love
coding and consider that strong quality and good developer experience matter a
 lot.
Through our diverse experiences, we allow studios to get better at doing
software and focus more on the artistic work.

Visit [cg-wire.com](https://cg-wire.com) for more information.

[![CGWire Logo](https://zou.cg-wire.com/cgwire.png)](https://cgwire.com)
