# Restoring a simple web app

## Step 1 - Create a deployment, service and route for httpd

A bit of a recap of the previous weeks. 
Create a simple deployment, service and route based on the information below:
* Container Image: `image-registry.openshift-image-registry.svc:5000/openshift/httpd:latest`
* Container Port: `8080`
* TLS termination: `edge`

## Step 2 - Create a backup schedule in OADP

To make sure the backup is made frequently but does not impact the other tenants on the cluster use the following requirements:

* Schedule: `*/5 * * * *`
* includedNamespaces: `<INSERT NAMESPACE NAME>`
* defaultVolumesToFsBackup: `false`

## Step 3 - Delete the deployment

To simulate a failure we will accidentally throw away the the deployment we just created.

## Step 4 - Restore the deployment 

Restore the deploy and check if everything works again.

## Resources

* [Create OADP Schedule| OpenShift Docs](https://docs.openshift.com/container-platform/4.14/backup_and_restore/application_backup_and_restore/backing_up_and_restoring/oadp-scheduling-backups-doc.html)
* [Create OADP Restore | OpenShift Docs](https://docs.openshift.com/container-platform/4.14/backup_and_restore/application_backup_and_restore/backing_up_and_restoring/restoring-applications.html)
