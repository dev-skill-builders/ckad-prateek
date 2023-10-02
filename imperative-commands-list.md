## LIST OF RUNNING IMPERATIVE COMMANDS

|COMMANDS|
|---|
|kubectl explain <resource-name>|
|kubectl explain pod.spec|
|kubectl run pod my-pod --image=nginx:latest --restartPolicy=Never --port=80 -n my-namespace|
|kubectl delete pod my-pod-hashnum|
|kubectl edit pod my-pod-hash|
|kubectl exec -it my-pod -- /bin/bash |
|kubectl run busy1 --image=busybox --rm -it --restart=Never -n my-ns -- /bin/sh # Run a temporary pod and immediately delete after exiting the pod.|
|kubectl run job my-job --image=busybox:latest|
|kubectl create cronjob my-cj --schedule="* * * * *" --image busybox -- /bin/sh -c 'echo "Current Date is $date"'|
