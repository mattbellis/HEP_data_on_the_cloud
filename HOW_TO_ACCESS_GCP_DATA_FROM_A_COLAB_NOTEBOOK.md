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
!gsutil ls gs://babar_data_test

This line copies the data from babar_data_test so the user can use it in a Colab notebook
!gsutil cp -r gs://babar_data_test .

The rest of the code that wasn't listing out files was the same importing h5hep and the pps_tools like the activities for PPP

Helpful link: https://colab.research.google.com/notebooks/io.ipynb#scrollTo=eDLm7MHQEr2U
