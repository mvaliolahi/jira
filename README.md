#### Setup

1. $ docker-compose up
2. goto localhost:8080 and ...

#### Licence Key!

$ docker exec -it jira bash
$ java -jar /opt/atlassian/jira/atlassian-agent.jar -d -m yourname@gmail.com -n BAT -p jira -o https://your-domain -s your-ip

#### Behind Proxy

$ docker exec -it jira bash 
$ find / -name "server.xml"
$ vim path/server.xml

comment default connector and uncomment proxy like below: `consider to proxyName` it should be chnaged to your domain

        <Connector port="8080" relaxedPathChars="[]|" relaxedQueryChars="[]|{}^&#x5c;&#x60;&quot;&lt;&gt;"
                   maxThreads="150" minSpareThreads="25" connectionTimeout="20000" enableLookups="false"
                   maxHttpHeaderSize="8192" protocol="HTTP/1.1" useBodyEncodingForURI="true" redirectPort="8443"
                   acceptCount="100" disableUploadTimeout="true" bindOnInit="false" secure="true" scheme="https"
                   proxyName="<subdomain>.<domain>.com" proxyPort="443"/>


