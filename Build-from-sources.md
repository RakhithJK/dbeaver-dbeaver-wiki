#### Prerequisites:

 1. JDK 17+. <a href="https://adoptium.net/" target="_blank">OpenJDK 17</a> is our default Java at the moment.
 2. <a href="https://maven.apache.org/" target="_blank">Apache Maven 3.8.6+</a>
 3. git
 4. Internet access

#### Build

```sh
git clone https://github.com/dbeaver/dbeaver.git dbeaver
cd dbeaver
mvn package
```
Binaries are in `product/standalone/target/products`
