# acm-storage
This is a quick setup to use ACM to manage multisite applications using ceph mirrroring.

## Prerequisites 
This assumes that two clusters have been setup and there is connectivity on the host networks either via standard networking or through something such as VPC peering.

The ACM operator must also be installed.

## Defining the application within ACM
On the cluster in which ACM is installed issue the following command to define the application.
```
oc create -f application-configuration
```

This defines the application and can place it on spokes named east1 and east2.

To create the storage application which will launch the storage jobs run

```
oc create -f application-configuration/storage
```
