# Big Picture

![big-picture.png](./static/big-picture.png) 


## Assumptions

|Role|FQDN|IP|OS|RAM|CPU|
|----|----|----|----|----|----|
|Master1|ct-kmaster1|10.99.0.101|CentOs 7.6|2G|2|
|Node1|ct-knode1|10.99.0.201|CentOs 7.6|1G|1|
|Node2|ct-knode2|10.99.0.202|CentOs 7.6|1G|1|


# Provision VM 

[CentOS 7.6 Link Download](https://sourceforge.net/projects/osboxes/files/v/vb/10-C-nt/7/7-18.10/181064.7z/download) 


# On both ct-kmaster1 , ct-knode1 and ct-knode2
## Pre-requisites 
Set network adapter all VM as image below


![](./static/adapter1.png) 

![](./static/adapter2.png) 

![](./static/adapter-2.png) 



#### Edit `/etc/hosts` file

```
# kube-master1 /etc/hostname
127.0.0.1 kubemaster1
```

```
# ct-knode1 /etc/hostname
127.0.0.1 ct-knode1
```

```
# ct-knode2 /etc/hostname
127.0.0.1 ct-knode2
```

#### Edit Hostname and  Static Ip for Adapter 2 ( POD network )
```
nmtui
```

![nmtui-config.png](./static/nmtui-config.png) 
