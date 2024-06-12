# Deploy and Configure Velero

## Step 1 - Check if the OADP operator is installed in your namespace

If not check with trainer.

## Step 2 - Create the secret for the Velero integration with Azure

You should have received the information to create the secret

`oc create secret generic cloud-credentials-azure --from-file cloud=<insert file name> `

## Step 3 - Create the Dataprotection application

Fill in the `./dataprotectionapplication.yaml` and deploy. Do you understand the config?

Check if the backupStorageLocation has `phase: available`

You have now configured and deployed Velero.

## Step 4 - Create a backup Schedule that makes backups of the resources in your namespace

reference: https://docs.openshift.com/container-platform/4.14/backup_and_restore/application_backup_and_restore/backing_up_and_restoring/oadp-scheduling-backups-doc.html
