### Setup

1/ Cloning the repo and build 


<figure>
<img src="https://github.com/ptabasso2/springTest0/blob/master/Images/Readme1.png" style="height: 200px; width: auto; margin-left: 150px">
</figure>


<figure>
<img src="https://github.com/ptabasso2/springTest0/blob/master/Images/Readme2.png" style="height: 200px; width: auto; margin-left: 150px">
</figure>


<figure>
<img src="https://github.com/ptabasso2/springTest0/blob/master/Images/Readme3.png" style="height: 100px; width: auto; margin-left: 150px">
</figure>




2/ Make sure the DD agent is running and listening on port **8126** 

3/ Start the server with agent instrumentation
<div class="highlighter-rouge"><div class="highlight"><pre class="highlight" style="background-color: greydark;"><code style="font-size: 12.0px;">COMP10619:$ <span style="font-weight: bold">java -javaagent:./dd-java-agent-0.17.0.jar
-Ddd.agent.host=localhost -Ddd.agent.port=8126 -Ddd.service.name=springtest
-jar build/libs/springtest-1.0.jar --server.port=9393</span>
</code></pre></div></div>

<figure>
<img src="https://github.com/ptabasso2/springTest0/blob/master/Images/Readme4.png" style="height: 100px; width: auto; margin-left: 150px">
</figure>




4/ Testing the application
In another termnial window lauch the following command:

<div class="highlight"><pre class="highlight" style="background-color: greydark;"><code style="font-size: 12.0px;">COMP10619:$ <span style="font-weight: bold">curl localhost:9393/ServiceC</span>
</code></pre></div>
