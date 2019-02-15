# 2/15/2019

*Next challenges!*

* Take the code we worked on where we download a file and keep all that code there, but.....set up a new section
in the notebook (or a new notebook) were we 
** Get the list of files in a bucket
** Download them one at a time
** Process them after we've downloaded them
** Delete them after we've processed them
** Display the plots of what we've processed. For example, get the muon momenta for all events? Or construct
some invariant mass of the two muons for all events. 

* Get the zeroth order cluster examples running
** Let's get an HTCondor cluster launched! 
** https://cloud.google.com/solutions/high-throughput-computing-htcondor

  


# 1/29/2019

To-do
* Colab notebook example accessing files by *mounting* the bucket, not copying it over. 
* Start looking over [how to launch an HTCondor instance](https://cloud.google.com/solutions/high-throughput-computing-htcondor) and let's try to write an example and documentation to do something with 8 or 16 cores. 

# Questions/Concerns (1/30/2019):
* 1) The stackoverflow document you sent me demonstrates how to mount files on Google Drive
* 1a) Maybe upload a small bit of data from BaBar to Drive to see if it works?
* 2) Also, it gave me an error -> 'GoogleDrive' object has no attribute 'mount'. Maybe I missed something?

#Updates (2/3/2019):
* I was checking the web to see if I could adapt the code for mounting data from google drive to mounting data from google cloud by using gsutil commands, and after scouring stackexchange as well as Pydrive's API, I feel like I'm onto something, but I'm too focused at the moment to find it (cf losing something important and then finding it in plain sight sometime later)
* I shared the colab notebook chronicling my preliminary efforts to try mounting data from google cloud



# Updates (2/5/2019)
* I tried running the updated code (still with copying the data, not mounting it just yet), but it gave an error when it got to
```
client = storage.Client('My First Project')
```
Saying that there was "No module named 'google.cloud.iam'"
But, upon scouring (and trying to make some sense of) Google-Python APIs, I found [this](https://pypi.org/project/google-cloud-storage/), which is what you probably used to try copying the data over for this most current run. I tried running the code more akin to how it is listed in the link, to see if I could get the bucket, and then the blob, but I got an error there as well.
