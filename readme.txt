工号:11012
姓名:阳中兴

-------------------------MVN-----------------------------------
命令:
----在MVN\consumerBanking 目录下执行 mvn clean compile

----在MVN\consumerBanking 目录下执行 mvn clean compile exec:java -Dexec.mainClass="com.companyname.bank.App" -Dexec.args="arg0 arg1 arg2"





----------------------mvn1----------------------------

命令:

修改webtest的pom.xml文件，将下面加入(已执行)

 <plugins>
      <plugin>
                <groupId>org.eclipse.jetty</groupId>
                <artifactId>jetty-maven-plugin</artifactId>
                <version>9.2.11.v20150529<version>
                <configuration>
                    <webAppConfig>
                        <allowDuplicateFragmentNames>true</allowDuplicateFragmentNames>
                    </webAppConfig>
                </configuration>
            </plugin>
    </plugins>

在\mvn1\webtest目录下执行  mvn jetty:run

