# Use Flyway Maven Plugin

## Setup pom.xml

In our maven java project, add the following plugin setting under <build><plugins> section:

```html
<plugin>
	<groupId>org.flywaydb</groupId>
	<artifactId>flyway-maven-plugin</artifactId>
	<version>6.0.4</version>
	<configuration>
		<url>jdbc:postgresql://localhost:5432/cross_post_db</url>
		<user>cross_post</user>
		<password>admin</password>
	</configuration>
</plugin>
```

## Run the maven plugin on command line

`mvn flyway:migrate`


