# Начнем писать документацию

## Статичный сайт. За основу беру www.mkdocs.org. Пусть пока будет отдельно в одноименной папке.

1. mkdocs - это библиотека. Лежит по этому пути: "/usr/local/bin/mkdocs"

код предельно прост:

``` bash
#!/usr/bin/python
# -*- coding: utf-8 -*-
import re
import sys

from mkdocs.__main__ import cli

if __name__ == '__main__':
    sys.argv[0] = re.sub(r'(-script\.pyw?|\.exe)?$', '', sys.argv[0])
    sys.exit(cli())
```

2. ок. Едем дальше.

``` bash
mkdock new my-project
```
создает папочку с файликами - это сгененированный шаблон сайта (благодаря ранее установленной либе click-man из пакета pip)

Доступные методы можно увидеть, выполнив: mkdocs serve

Сейчас будет copy-paste:

Commands
mkdocs new [dir-name] - Create a new project.
mkdocs serve - Start the live-reloading docs server.
mkdocs build - Build the documentation site.
mkdocs help - Print this help message.

Project layout
mkdocs.yml    # The configuration file.
docs/
    index.md  # The documentation homepage.
    ...       # Other markdown pages, images and other files.


3.

