# Pandomium [![Build Status](https://travis-ci.org/dzikoysk/Pandomium.svg?branch=master)](https://travis-ci.org/Panda-Programming-Language/Pandomium)
Pandomium is the JCEF (Java Chromium Embedded Framework) implementation dedicated for the maven projects 

#### Example
<!-- ![PandomiumTest.java - Windows x64](https://panda-lang.org/screenshot/5d8KeBJg.png) -->
<!-- ![PandomiumTest.java - Linux x64](https://panda-lang.org/screenshot/5E5ZgE9A.png) -->
<!-- ![PandomiumTest.java - Linux x64](https://panda-lang.org/screenshot/bZwbEGmm.png) -->
![PandomiumTest.java - Both x64](https://pandomium.panda-lang.org/github/preview-both.png)

```java
Pandomium pandomium = new Pandomium(PandomiumSettings.getDefaultSettings());
pandomium.initialize();

PandomiumClient client = pandomium.createClient();
PandomiumBrowser browser = client.loadURL("https://panda-lang.org");
```
Full example: [PandomiumTest.java](https://github.com/dzikoysk/Pandomium/blob/master/pandomium/src/test/java/org/panda_lang/pandomium/PandomiumTest.java)

#### Maven
```xml
<dependency>
    <groupId>org.panda-lang</groupId>
    <artifactId>pandomium</artifactId>
    <version>67.0</version>
</dependency>
```
```xml
<repository>
    <id>panda-repository</id>
    <url>https://repo.panda-lang.org/</url>
</repository>
```

If you don't want to use maven you can download the latest version here: [Pandomium 67.0](https://repo.panda-lang.org/org/panda-lang/pandomium/67.0/pandomium-67.0.jar)

#### Supported platforms
* **OS**: Windows x64 / Linux x64
* **Java**: Java 8

#### Building
* [Windows x64](https://github.com/dzikoysk/Pandomium/wiki/Windows-x64-Build)
* [Linux x64](https://github.com/dzikoysk/Pandomium/wiki/Linux-x64-Build)
* [macOS](https://github.com/dzikoysk/Pandomium/wiki/macOS-Build)

#### Repository structure
```
pandomium/
+--pandomium/                 Pandomium Library module
   +----/src                  Sources of Pandomium Library module
   +----pom.xml               The main maven build script for Pandomium Library module
+--pandomium-linux/           Linux implementation of Pandomium Library module
   +----/libs                 Platform specified libraries
   +----/native               Platform specified natives
   +----/src                  Platform implementation
   +----pom.xml               The main maven build script for Linux module
+--pandomium-macos/           MacOS implementation of Pandomium Library module
   +----/libs                 Platform specified libraries
   +----/native               Platform specified natives
   +----/src                  Platform implementation
   +----pom.xml               The main maven build script for macOS module
+--pandomium-win/             Windows implementation of Pandomium Library module
   +----/libs                 Platform specified libraries
   +----/native               Platform specified natives
   +----/src                  Platform implementation
   +----pom.xml               The main maven build script for Windows module
+--pom.xml                    The main maven build script
```

#### TODO
* [x] Build natives & jcef
* [x] Basic implementation
* [x] Builds available in the maven repository
* [x] Pandomium wrapper for JCEF objects
* [ ] Win32, Linux32 & macOS support
* [ ] Advanced Java <-> JS bridge
* [ ] ByteBuffer implementation
