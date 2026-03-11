# How to monitor Skupper sites from a remote Prometheus

## 1. Create one PodMonitor for the Skupper Router and one PodMonitor for the Network Observer
~~~
oc apply -f podmonitorrouter.yaml
oc apply -f podmonitorobserver.yaml
~~~

## 2. Forward `oc -n openshift-user-workload-monitoring port-forward svc/prometheus-operated 9091:9090`
## 3. Go to: `http://127.0.0.1:9091/targets`


