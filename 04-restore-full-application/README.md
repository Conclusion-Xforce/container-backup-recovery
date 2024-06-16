# Restore full application

## Step 1 - Deploy the image tool & upload image​

Create the image tool deployment and upload an image (so we can check if is still there after restore)

`oc apply -f ./manifests.yaml`

## Step 2 - Wait until backup is scheduled again​ (or create one manually)

Check in the OADP backup view until the backup is made again including the newly deployed application.

## Step 3 - Delete the deployment and Persistent Volume Claim​

To simulate a failure we will accidentally throw away the the deployment, service, route and most importantly the persisten volume claim we just created.

## Step 4 - Restore

Restore the application including the Persistent volume claim.

## Step 5 - Check Image

Check if the image you uploaded is still there

## Resources

* [Create OADP Schedule| OpenShift Docs](https://docs.openshift.com/container-platform/4.14/backup_and_restore/application_backup_and_restore/backing_up_and_restoring/oadp-scheduling-backups-doc.html)
* [Create OADP Restore | OpenShift Docs](https://docs.openshift.com/container-platform/4.14/backup_and_restore/application_backup_and_restore/backing_up_and_restoring/restoring-applications.html)
