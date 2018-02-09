# Daemon Set to append a new string to search path 

This daemon set when deployed to the default namespace will append the required search string to resolv.conf

It will also update the kubelet service to point to the new resolv.conf and schedule for a reboot

In order for the pods to pick up the changes, nodes require a reboot, which is automatic

# Create Cluster Role Binding for the default namespace to give the service account proper priveleges to annotate the node for reboot. The file is also included
