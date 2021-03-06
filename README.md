# ![](https://gravatar.com/avatar/11d3bc4c3163e3d238d558d5c9d98efe?s=64) aptible/php

[![Build Status](https://travis-ci.org/aptible/docker-php.svg?branch=master)](https://travis-ci.org/aptible/docker-php)

Aptible PHP Base Image

## Installation and Usage

    docker pull quay.io/aptible/php
    docker run quay.io/aptible/php [options]

## PHP Patch

For 5.6, this image carries a PHP patch to allow disabling SSL verification for
MySQL PDO connections via the `PDO::MYSQL_ATTR_SSL_VERIFY_SERVER_CERT`
attribute (set it to `false` to disable verification; it otherwise defaults to
`true`). For other versions, this patch was incorporated by the PHP team in
mainline PHP, so those images don't carry additional patches.

This is a fix for: https://bugs.php.net/bug.php?id=71003

Make sure you understand the implications before using this attribute. If
you're deploying on Aptible, feel free to reach out to support.

## Available Tags

* `7.2`
* `7.1`
* `7.0`
* `5.6`
* `latest`: currently `7.2` (not recommended: this tag changes over time)

## Copyright and License

MIT License, see [LICENSE](LICENSE.md) for details.

Copyright (c) 2016 [Aptible](https://www.aptible.com) and contributors.
