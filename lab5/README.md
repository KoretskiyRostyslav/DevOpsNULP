1. Done</br>
2. my_app/logs, install redis</br>
3. 8 STATES := app tests - is a variable with dynamically assigned values.</br>
 REPO := docker repo name</br>
..PHONY - is used to create a virtual target of makefile because STATE isn't a physical file.</br>
 $(STATES): - use of app or tests variables.</br>
 docker build - creates new docker container.</br>
 $(@) - variables from STATE(app, tests).</br>
 run - execute commands.</br>
 docker-prune - remove all the previous dockers.</br>
![1](./img/1.png)</br>
![2](./img/2.png)</br>
![3](./img/3.png)</br>
![4](./img/4.png)</br>
![5](./img/5.png)</br>
![6](./img/6.png)</br>
![7](./img/7.png)</br>
![8](./img/8.png)</br>
![9](./img/9.png)</br>
4. Done</br>
![10](./img/10.png)</br>
5. Makefile is better in this situation because of small amount of operations.</br>
Link to dockerhub: https://hub.docker.com/repository/docker/rostik37/lab5 </br>
6. Done, yml file in lab4</br>
![11](./img/11.png)
