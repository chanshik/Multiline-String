Java Multiline String
=====================

Original source code from AdrianWalker.org
(http://www.adrianwalker.org/2011/12/java-multiline-string.html)


Build for Mac
-------------

Original *pom.xml*
```xml
   <dependencies>
     <dependency>
       <groupId>sun.jdk</groupId>
       <artifactId>tools</artifactId>
       <version>LATEST</version>
       <scope>system</scope>
       <systemPath>${java.home}/../lib/tools.jar</systemPath>
     </dependency>
   </dependencies>
```

In Mac OS X, tools.jar no more exist. 

Reference: [JavaDevTools.html](https://developer.apple.com/library/mac/documentation/Java/Conceptual/Java14Development/02-JavaDevTools/JavaDevTools.html)


Modified *pom_mac.xml*
```xml
   <dependencies>
     <dependency>
       <groupId>sun.jdk</groupId>
       <artifactId>tools</artifactId>
       <version>LATEST</version>
       <scope>system</scope>
       <systemPath>${java.home}/../Classes/classes.jar</systemPath>
     </dependency>
   </dependencies>
```


Build
```
   $ mvn -f pom_mac.xml claen compile
```
