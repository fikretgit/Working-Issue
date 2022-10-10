The Official Page;

```
https://github.com/opencv/cvat
```
and installation guide page;

```
https://github.com/opencv/cvat/tree/develop/helm-chart
```

to install cvat;

```
--> git clone https://github.com/opencv/cvat
--> cd cvat
--> docker-compose up -d
```
the output;

```
```
Status: Downloaded newer image for cvat/ui:dev
Creating cvat_db    ... done
Creating cvat_redis ... done
Creating cvat_opa   ... done
Creating traefik              ... done
Creating cvat_server          ... done
Creating cvat_worker_low      ... done
Creating cvat_utils           ... done
Creating cvat_worker_webhooks ... done
Creating cvat_worker_default  ... done
Creating cvat_ui              ... done
```

then we must create a "superuser" so;

```
docker exec -it cvat_server bash -ic 'python3 ~/manage.py createsuperuser'
```
add the values;

```
user name; <name of superuser>
email: 
password : xxxxxxx
```

superuser created..!!

Google Chrome is the only browser which is supported by CVAT. You need to install it as well. Type commands below in a terminal window:

```
curl https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
sudo apt-get update
sudo apt-get --no-install-recommends install -y google-chrome-stable

```

then localhost:8080 to see the pages.. but this is locally..

For K8s purpose we can use Helm.. but Cvat team says they are not supported Helm Chart..
so we must chnage "docker-compose.yaml" for Redis, Postgre etc.. which source we created manually on our cluster and attached with resources that will be created by docker-compose, so it will run appropriately..


