# github-example-package

## Setting.xml

<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
                      http://maven.apache.org/xsd/settings-1.0.0.xsd">

  <activeProfiles>
    <activeProfile>github</activeProfile>
  </activeProfiles>

  <profiles>
    <profile>
      <id>github</id>
      <repositories>
        <repository>
          <id>central</id>
          <url>https://repo1.maven.org/maven2</url>
        </repository>
        <repository>
          <id>github</id>
          <url>https://maven.pkg.github.com/apoorvpandey-ap/github_package</url
          <snapshots>
            <enabled>true</enabled>
          </snapshots>
        </repository>
      </repositories>
    </profile>
  </profiles>

  <servers>
    <server>
      <id>github</id>
      <username>apoorvpandey-ap</username>
      <password>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</password>
    </server>
  </servers>
</settings>





---
---
## pom.xml
<dependency>
            <groupId>org.example</groupId>
            <artifactId>github_package</artifactId>
            <version>1.0.0-SNAPSHOT</version>
        </dependency>
          
	<distributionManagement>
        <repository>
           <id>github</id>
           <name>GitHub OWNER Apache Maven Packages</name>
           <url>https://maven.pkg.github.com/apoorvpandey-ap/github_package</url>
   </repository>
</distributionManagement>  
