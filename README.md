# jdkdb-data - JDK Metadata Database

This repository collects metadata from list of currently available Java JRE/JDK distributions and stores it as JSON files in the [`metadata/`](./metadata) directoryy.

This information in this repository is updated daily using the [jdkdb-scraper project](https://github.com/jbangdev/jdkdb-scraper)
This project is based on [Joschi's Java Metadata project](https://github.com/joschi/java-metadata) and incorporates ideas from the [Foojay's Disco API project](https://github.com/foojayio/discoapi).

## Supported distributions

* [AdoptOpenJDK](https://adoptopenjdk.net/)
* [Corretto](https://aws.amazon.com/corretto/)
* [Dragonwell](https://cn.aliyun.com/product/dragonwell)
* [Eclipse Temurin](https://adoptium.net/)
* [GraalVM Community Edition](https://www.graalvm.org/)
* [IBM Semeru](https://developer.ibm.com/languages/java/semeru-runtimes/)
* [Java SE Reference Implementations](https://jdk.java.net/)
* [Liberica](https://bell-sw.com/)
* [Mandrel](https://github.com/graalvm/mandrel)
* [Microsoft OpenJDK](https://www.microsoft.com/openjdk)
* [OpenJDK](https://jdk.java.net/)
* [Oracle JDK](https://www.oracle.com/java/)
* [Oracle GraalVM](https://www.graalvm.org/)
* [SapMachine](https://sap.github.io/SapMachine/)
* [Tencent Kona](https://cloud.tencent.com/document/product/1149)
* [Trava OpenJDK](https://github.com/TravaOpenJDK/)
* [Zulu Community](https://www.azul.com/products/zulu-community/)

## Metadata structure

| Field name      | Description                           |
| --------------- | ------------------------------------- |
| `architecture`  | Supported machine architecture        |
| `checksum`      | Distro checksum of the artifact       |
| `checksum_type` | Distro checksum of the artifact       |
| `filename`      | Filename of the artifact              |
| `features`      | Features of the distribution          |
| `file_type`     | The file extension of the artifact    |
| `image_type`    | JRE (`jre`) or JDK (`jdk`)            |
| `java_version`  | Java version the artifact is based on |
| `jvm_impl`      | JVM implementation                    |
| `md5`           | MD5 checksum of the artifact          |
| `os`            | Supported operating system            |
| `release_type`  | `ca` (stable) or `ea` (early access)  |
| `sha1`          | SHA-1 checksum of the artifact        |
| `sha256`        | SHA-256 checksum of the artifact      |
| `sha512`        | SHA-512 checksum of the artifact      |
| `size`          | Size of the artifact in bytes         |
| `url`           | Full source URL of the artifact       |
| `vendor`        | Name of publishing organization       |
| `version`       | Version of the JDK/JRE distribution   |

Example:

```json
{
  "architecture": "x86_64",
  "checksum": "f07e67b9773cadaf539e67b4e26957b9d85220b7",
  "checksum_type": "sha1",
  "features": [
    "javafx"
  ],
  "filename": "zulu8.44.0.13-ca-fx-jdk8.0.242-linux_x64.tar.gz",
  "file_type": "tar.gz",
  "image_type": "jdk",
  "java_version": "8.0.242",
  "jvm_impl": "hotspot",
  "md5": "fda058637e054eae280eb8761824d064",
  "os": "linux",
  "release_type": "ga",
  "sha1": "f07e67b9773cadaf539e67b4e26957b9d85220b7",
  "sha256": "e35bad183b6309384fd440890b4c7888b30670006a6e10ce3d4fefb40fbefc93",
  "sha512": "2f650295baf38d99794343b04dd2dd81ebeff92fa9c3a8bf110700118d1879e20016c6ff441f4488e87dd1fc733b87836e90ec9ba26184d8288c400e11bc9057",
  "size": 155585453,
  "url": "https://static.azul.com/zulu/bin/zulu8.44.0.13-ca-fx-jdk8.0.242-linux_x64.tar.gz",
  "version": "8.44.0.13",
  "vendor": "zulu"
}
```

See also the files inside the [`metadata/`](./metadata/) directory.

## Disclaimer

This project is in no way affiliated with any of the companies or projects offering and distributing the actual JREs and JDKs.

All respective copyrights and trademarks are theirs.
