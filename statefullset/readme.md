stateful applications --> DB

Deployment --> stateless applications not for stateful applications
Statefulset --> stateful applications.

Deployment vs Statefulset
==========================
1. Deployment is for stateless applications, Statefulset is stateful applications
2. PV and PVC is not mandatory for Deployment, but mandatory for stateful applications
3. Statefulset need headless service... i.e no cluster IP
4. Pods create in orderly manner in statefulset, Once first pod comes to running, then only other pod will create. While deletion reverse order follows
5. Pod identities are preserved in statefulset, because if any pod crashes, statefulset create another pod with same name, so that communication is easy between pods..

nslookup nginx-svc --> Cluster IP

1. DB node is responsible to findout all the worker nodes and inform them about data changes

headless service, it is a service without cluster IP
nslookup nginx-headless-svc --> all the endpoint IP