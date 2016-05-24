# PKIUtils

## install
```sh
    git clone https://github.com/paulmaelzer/PKIUtils.git
    cd PKIUtils
    mvn install
```
## usage
####pom.xml
```xml
    <dependency>
        <groupId>se.kth.hopsworks.util</groupId>
        <artifactId>PKIUtils</artifactId>
        <version>1.0</version>
        <packaging>jar</packaging>
    </dependency>
```
####inside the project
```java
import se.kth.hopsworks.util.PKIUtils;


 /**
 * Signs a verified Certificate Signing Request
 * @param  csr the X.509v3 certificate signing request (ASCII/Base64) as a String
 * @param  confDirPath the path to the intermediate certificate authority, containing the openssl.cnf file
 * @param  keyStorePass the password protecting the intermediate certificate authority's private key
 *
 * @return the signed public certificate (ASCII/Base64) as a String  
 * @throws IOException, InterruptedException 
 */
PKIUtils.signWithServerCertificate(String csr, String confDirPath, String keyStorePass)
```
