### Setup

1/ Cloning the repo and build 

<div class="highlighter-rouge"><div class="highlight"><pre class="highlight" style="background-color: greydark;"><code style="font-size: 12.0px;">COMP10619:pej$ <span style="font-weight: bold">git clone https://github.com/ptabasso2/SpringTest0.git</span>
COMP10619:$ <span style="font-weight: bold">cd springTestCorrelation</span>
COMP10619:$ <span style="font-weight: bold">./gradlew build</span>
</code></pre></div></div>


<span style="font-weight: bold">Cloning into 'SpringTest0'...</span>
<span style="font-weight: bold">remote: Enumerating objects: 44, done.</span>
<span style="font-weight: bold">remote: Counting objects: 100% (44/44), done.</span>
<span style="font-weight: bold">remote: Compressing objects: 100% (38/38), done.</span>
<span style="font-weight: bold">remote: Total 44 (delta 8), reused 31 (delta 1), pack-reused 0</span>
<span style="font-weight: bold">Unpacking objects: 100% (44/44), done.</span>


COMP10619:pej$ cd SpringTest0
COMP10619:SpringTest0 pej$ ls -lrt
total 26456
-rw-r--r--  1 pejman.tabassomi  staff      1515 Mar 14 17:33 README.md
-rw-r--r--  1 pejman.tabassomi  staff    138869 Mar 14 17:33 Result.png
-rw-r--r--  1 pejman.tabassomi  staff      1004 Mar 14 17:33 build.gradle
drwxr-xr-x  3 pejman.tabassomi  staff        96 Mar 14 17:33 gradle
-rwxr-xr-x  1 pejman.tabassomi  staff      5046 Mar 14 17:33 gradlew
-rw-r--r--  1 pejman.tabassomi  staff      2314 Mar 14 17:33 gradlew.bat
-rw-r--r--  1 pejman.tabassomi  staff       165 Mar 14 17:33 manifest.yml
-rwxr-xr-x  1 pejman.tabassomi  staff      7058 Mar 14 17:33 mvnw
-rwxr-xr-x  1 pejman.tabassomi  staff      5006 Mar 14 17:33 mvnw.cmd
-rw-r--r--  1 pejman.tabassomi  staff      1854 Mar 14 17:33 pom.xml
drwxr-xr-x  4 pejman.tabassomi  staff       128 Mar 14 17:33 src
COMP10619:SpringTest0 pej$



2/ Make sure the DD agent is running and listening on port **8126** 

3/ Start the server with agent instrumentation
<div class="highlighter-rouge"><div class="highlight"><pre class="highlight" style="background-color: greydark;"><code style="font-size: 12.0px;">COMP10619:$ <span style="font-weight: bold">java -javaagent:./dd-java-agent-0.17.0.jar
-Ddd.agent.host=localhost -Ddd.agent.port=8126 -Ddd.service.name=springtest
-jar build/libs/springtest-1.0.jar --server.port=9393</span>
</code></pre></div></div>

4/ Testing the application
In another termnial window lauch the following command:

<div class="highlight"><pre class="highlight" style="background-color: greydark;"><code style="font-size: 12.0px;">COMP10619:$ <span style="font-weight: bold">curl localhost:9393/ServiceC</span>
</code></pre></div>

This should normally display this type of lines:

<figure>
<img src="https://github.com/ptabasso2/springTchibo/blob/master/Result.png" style="height: 200px; width: auto; margin-left: 150px">
</figure>
