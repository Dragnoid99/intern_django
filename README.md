# Instructions

 You need to download this repository and should have docker and django installed on your local system. 
 Then run the following commands on your local system to host both the servers. Note the mysite is the server 1 and server 2 is the server 2. 
```console
$ cd mysite
$ sudo docker build -t polls -f Dockerfile .
$ sudo docker run -itd --net host polls
$ cd ..
$ cd server2
$ sudo docker build -t server2 -f Dockerfile .
$ sudo docker run -itd --net host server2
$ cd ..
```
<p> Then you will be good to go and server 1 will be hosted on http://127.0.0.1:8000/ and server 2 will be hosted http://127.0.0.1:8080/ </p>
<p> http://127.0.0.1:8000/polls/ -> list of all questions </p>
<p> http://127.0.0.1:8000/polls/1/details/ -> list of choices of question 1 </p>
<p> http://127.0.0.1:8000/polls/1/results/ -> result of question 1 </p>
<p> http://127.0.0.1:8080/app/ -> list of choices of question 1 of server 1 </p>
<p> http://127.0.0.1:8080/app/results -> result of question 1 of server 1 </p>
