---
id: 20120601
title: Referencias de nativepaths en iOS y Android de AS3
date: 2012-06-01T11:27:07+00:00
author: Gorka
layout: post
permalink: /2012/06/referencias-de-nativepaths-en-ios-y-android-de-as3/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2012/06/hierarchy.png" alt="Hierarchy" />

Sin explicar nada, quien necesite esto agradecerá que aqui está:

**Android**

```AS3
File.applicationDirectory.nativePath: (vacío)
File.applicationStorageDirectory.nativePath: /data/data/air.[App ID]/[App name (sin espacios)]/Local Store
File.documentsDirectory.nativePath: /mnt/sdcard
File.userDirectory.nativePath: /mnt/sdcard
```

**iOS**

```AS3
File.applicationDirectory.nativePath: /var/mobile/Applications/ [RANDOM CODE] /[Output file]
File.applicationStorageDirectory.nativePath: /var/mobile/Applications/ [RANDOM CODE] /Library/Application Support/[App  ID]/Local Store
File.documentsDirectory.nativePath: /var/mobile/Applications/ [RANDOM CODE] /Documents
File.userDirectory.nativePath: /var/mobile/Applications/ [RANDOM CODE]
```

**Windows 7 (sólo de referencia)**

```AS3
File.applicationDirectory.nativePath: C:\Users\[USER]\[PATH TO FILE]
File.applicationStorageDirectory.nativePath: C:\Users\[USER]\AppData\Roaming\[App ID]\Local Store
File.documentsDirectory.nativePath: C:\Users\[USER]\Documents
File.userDirectory.nativePath: C:\Users\[USER]
```

Referencia de Adobe: http://help.adobe.com/en_US/as3/dev/WS5b3ccc516d4fbf351e63e3d118666ade46-7fe4.html

Saludos, <br />
Gorka

