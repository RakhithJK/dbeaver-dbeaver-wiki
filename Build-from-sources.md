## Build DBeaver from sources

#### Prerequisites:

 1. Java (JDK) 11+.
 2. Apache Maven 3+
 3. Internet access

#### Build

```sh
git clone https://github.com/dbeaver/dbeaver.git dbeaver
cd dbeaver
mvn package
```
Binaries are in `product/standalone/target/products`
