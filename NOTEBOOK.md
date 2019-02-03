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
