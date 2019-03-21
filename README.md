### Setup

1/ Cloning the repo and build 


<figure>
<img src="https://github.com/ptabasso2/springTest0/blob/master/Images/Readme1.png" width=auto height="110px">
</figure>


<figure>
<img src="https://github.com/ptabasso2/springTest0/blob/master/Images/Readme2.png" width=auto height="110px">
</figure>


<figure>
<img src="https://github.com/ptabasso2/springTest0/blob/master/Images/Readme3.png" width=auto height="110px">
</figure>




2/ Make sure the DD agent is running and listening on port **8126** 

3/ Start the server with agent instrumentation

<figure>
<img src="https://github.com/ptabasso2/springTest0/blob/master/Images/Readme4.png" width=auto height="110px">
</figure>


4/ Testing the application
In another termnial window lauch the following command:

<div class="highlight"><pre class="highlight" style="background-color: greydark;"><code style="font-size: 12.0px;">COMP10619:$ <span style="font-weight: bold">curl localhost:9393/ServiceC</span>
</code></pre></div>
