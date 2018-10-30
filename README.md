ContentApiBundle
================

[![Build Status](https://travis-ci.com/libero/content-api-bundle.svg?branch=master)](https://travis-ci.com/libero/content-api-bundle)

This is a [Symfony](https://symfony.com/) bundle that implements the Libero content API.

Getting started
---------------

Using [Composer](https://getcomposer.org/) you can add the bundle as a dependency:

```
composer require libero/content-api-bundle
```

If you're not using [Symfony Flex](https://symfony.com/doc/current/setup/flex.html), you'll need to enable the bundle in your application.

Configure your application to add one (or more) content APIs:

```yaml
services:
    Libero\ContentApiBundle\Adapter\NullItems: ~

content_api:
    services:
        research-articles:
            items: Libero\ContentApiBundle\Adapter\NullItems
        blog-articles:
            items: Libero\ContentApiBundle\Adapter\NullItems
```

And add the following to your routing file:

```yaml
content_api:
    resource: .
    type: content_api
```

This example will create two content APIs, with the prefixes `research-articles` and `blog-articles`.

Getting help
------------

- Report a bug or request a feature on [GitHub](https://github.com/libero/libero/issues/new/choose).
- Ask a question on the [Libero Community Slack](https://libero-community.slack.com/).
- Read the [code of conduct](https://libero.pub/code-of-conduct).
