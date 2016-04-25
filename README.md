# spring-cloud-stream-app-maven-plugin
Maven plugin for generating spring cloud stream applications from the spring-cloud-stream-app-starters repository

** Build

mvn clean package [Requires JDK 8]

**Sample Configuration**

``xml

<plugin>
				<groupId>org.springframework.cloud.stream.app.plugin</groupId>
				<artifactId>spring-cloud-stream-app-maven-plugin</artifactId>
				<version>1.0.0.BUILD-SNAPSHOT</version>
				<configuration>
					<generatedProjectHome>${session.executionRootDirectory}/apps</generatedProjectHome>
					<generatedProjectVersion>${project.version}</generatedProjectVersion>
					<applicationType>stream</applicationType>
					<bom>
						<name>scs-bom</name>
						<groupId>org.springframework.cloud.stream.app</groupId>
						<artifactId>spring-cloud-stream-app-dependencies</artifactId>
						<version>1.0.0.BUILD-SNAPSHOT</version>
					</bom>

					<binders>
                    						<kafka />
                    						<rabbit />
                    					</binders>
                    					<generatedApps>

                    					<time-source />
                                        	<transform-processor />
                                        	<trigger-source />
                                        </generatedApps>
                                        </plugin>

					``xml