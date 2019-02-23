How do we do this? 

Helpful links. 


From our good friend Google: 
https://cloud.google.com/dataproc/docs/guides/create-cluster for creating a cluster
https://cloud.google.com/dataproc/docs/guides/manage-cluster for managing said cluster

I think these are the instructions on how to launch an HTCondor instance. 

https://cloud.google.com/solutions/high-throughput-computing-htcondor

Maybe should be working with the Github repo?

https://github.com/GoogleCloudPlatform/deploymentmanager-samples/tree/master/examples/v2/htcondor


# Will have to ssh in to a VM

https://cloud.google.com/compute/docs/quickstart-linux

Make sure you follow this closely. If it works, you have a window that pops up thatI think
is already ssh'ed into the instance. 

***IMPORTANT!*** Select **Allow all access to Cloud APIs**


Might want to look at [this](https://cloud.google.com/compute/docs/instances/transfer-files) to see how to transfer
files into the instance. 

# Install the test files

Following this

https://cloud.google.com/solutions/high-throughput-computing-htcondor

## Need to install git first. 

```
sudo apt-get update
sudo apt-get install git
```
Select *[Y]* when the option comes up. 

## Deploy

Note that after you've run the ```gcloud deployment-manager...``` command, you can see the nodes on 
your Google Dashboard. 

When you run the 

```
gcloud compute ssh condor-submit
``` 

command, don't enter a passphrase and select *n* for no when it asks

```
Did you mean zone [us-east1-b] for instance: [condor-submit] (Y/n)? 
```



# ISSUES

Doesn't seem to actually run the jobs. That is, there is no output files as per the example???

Try the above again, but launch a centos VM and edit the startup condor file to reflect
the timezone and centos version and the condor version. 

Want to try this again, but editing the condor.jinja to import the shell scripts, a la

https://github.com/GoogleCloudPlatform/deploymentmanager-samples/blob/master/examples/v2/htcondor/condor.jinja.schema



Should we look at the genomics API?

https://cloud.google.com/genomics/docs/quickstart


-------------------------------

# Trying slurm

https://cloud.google.com/blog/products/gcp/easy-hpc-clusters-on-gcp-with-slurm

https://github.com/SchedMD/slurm/tree/slurm-17.11/contribs/gcp

When I try this, slurm never seems to get installed. 





