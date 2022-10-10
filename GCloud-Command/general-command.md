to login first;

```
--> gcloud auth login
```
it directs you google page and take the token from the browser then give the value of token so you can run the scp command..

if you swicth the different account;


You can run:
```
--> gcloud config set account `ACCOUNT`
```

to switch accounts if necessary.

you can see the account details;

```
--> gcloud auth list
```
```
                  Credentialed Accounts
ACTIVE  ACCOUNT
*       xxxxxxxxxxxx-compute@developer.gserviceaccount.com
```

To set the active account, run:
```
--> gcloud config set account `ACCOUNT`
```


* ssh key sending;

```
--> gcloud compute os-login ssh-keys add --key-file=<path-of-.pub-keyfile> --project=<name-of-project-on-GCP>
```

* to send folder;

```
--> gcloud compute scp --recurse np-mcit-instance:~/<path of folder on remote>  <path of folder on local> --zone=us-central1-a
```

