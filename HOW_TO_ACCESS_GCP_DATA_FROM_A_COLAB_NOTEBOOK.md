How do we do this? 

Helpful links?

The following code was the first cell in Google_Cloud_File_Test.ipynb (I believe it is shared with you)
It installs Pydrive onto a Colab notebook and asks the user for authentification

```
!pip install -U -q Pydrive
import os
from pydrive.auth import GoogleAuth
from pydrive.drive import GoogleDrive
from google.colab import auth
from oauth2client.client import GoogleCredentials

auth.authenticate_user()
gauth = GoogleAuth()
gauth.credentials = GoogleCredentials.get_application_default()
drive = GoogleDrive(gauth)
```

This code builds a drive API client, which allows you to use functions (differentiating between functions and methods is going to be a pain because I'm taking Data Structures, and working on this at the same time) from the Google Drive API


This line uses the drive command gsutil to list all the files within the bucket we stored in Google Cloud, called babar_data_test
```
!gsutil ls gs://babar_data_test
```
This line copies the data from babar_data_test so the user can use it in a Colab notebook

```
!gsutil cp -r gs://babar_data_test .
```

The rest of the code that wasn't listing out files was the same importing h5hep and the pps_tools like the activities for PPP

Helpful link: https://colab.research.google.com/notebooks/io.ipynb#scrollTo=eDLm7MHQEr2U

# Example of accessing and running over data on Google Cloud Storage from Colab

[Relevant Colab notebook](https://colab.research.google.com/drive/12Hk9fa4zS8qT75G0ciiDFfn0LLdpGIzW)


# Accessing GCP files without downloaded them to the Colab environment. 

Is [this](https://stackoverflow.com/questions/49021464/interface-between-google-colaboratory-and-google-cloud) a way to do it? 


# Google Drive
This is not Google Cloud storage, but still relevant. 

https://stackoverflow.com/questions/46986398/import-data-into-google-colaboratory

Not sure if we're mounting the whole drive right now, or just a folder. 


