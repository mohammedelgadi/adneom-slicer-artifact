# adneom-slicer-artifact

Provides a partition utility method for chunking a list into multiple sublists with specific sizes.

This library contains three implementations of the partition method :

* AdneomCustomArrayUtils : This class uses a custom recursive algorithm.
* AdneomArrayUtils :  This second class implements the methode partition using the Guava library.
* AdneomGuavaArrayUtils : Uses java8 collectors class helper using "groupingBy" method

You can download the source code from the github repository:
>	https://github.com/mohammedelgadi/adneom-slicer

## How to use the "Adneom-slicer" library
There are many ways to use our library :
1. Checkout the library source code from the github repository : 
>	https://github.com/mohammedelgadi/adneom-slicer
2. Using this github as maven repository (like nexus in professional context):

This method will uses the github as maven repository
* First you have to add the repository to you maven configuration file <b>pom.xml</b> by adding the code bellow :
####
	<repositories>
		<repository>
			<id>mvn-repo</id>
			<url>https://rawgit.com/mohammedelgadi/adneom-slicer-artifact/master</url>
			<releases>
				<enabled>true</enabled>
				<updatePolicy>always</updatePolicy>
			</releases>
			<snapshots>
				<enabled>true</enabled>
				<updatePolicy>always</updatePolicy>
			</snapshots>
		</repository>
	</repositories>
####


* Secondly, you must add the library to your dependencies using the code (see below) :

####
	<dependency>
		<groupId>fr.adneom</groupId>
		<artifactId>array-slicer</artifactId>
		<version>1.0.0</version>
	</dependency>
    
####

* Now you only have to use the partition method :


* This is the JavaDoc description of partition method

![Description of partition method](https://github.com/mohammedelgadi/adneom-slicer-artifact/blob/master/img/partition-javadoc.png)

## Astuce & Remarque :

To instantiate the beans, you can use the default constructor. But If your are using spring to inject beans, your have to :
* create a configuration class, and declare the bean function,
* or declare the Adneom class in you injection xml file for the old versions of spring.

Example of configuration spring class :
```
@Configuration
public class AdneomConfiguration {

    @Bean
    public AdneomArrayUtils adneomArrayUtils(){
        return new AdneomArrayUtils();
    }

}
```



 ## Our versions
 * V 1.0.0 : First version of library, created as recruitment test



