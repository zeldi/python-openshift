# Creating and Deploying Python Apps on Openshift

## Scope
I wanted to create a demo python app to work on k8s, and OpenShift.


### Running in local docker environment

```
# docker-compose build
# docker-compose up 
Creating network "simple-python-deployment_default" with the default driver
Creating python ... done
Attaching to python
python    |  * Serving Flask app "server.py"
python    |  * Environment: production
python    |    WARNING: This is a development server. Do not use it in a production deployment.
python    |    Use a production WSGI server instead.
python    |  * Debug mode: off
python    |  * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
python    | 172.18.0.1 - - [05/Jul/2020 06:11:26] "GET / HTTP/1.1" 200 -
python    | 172.18.0.1 - - [05/Jul/2020 06:11:27] "GET /favicon.ico HTTP/1.1" 404 -
```


### Deploy the app to Openshift

```text
$ oc new-app https://github.com/zeldi/python-openshift.git --name simple-python
```
