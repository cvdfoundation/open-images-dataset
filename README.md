# Open Images Dataset
Open Images is a dataset of ~9 million URLs to images that have been annotated with labels spanning over 6000 categories. This page aims to provide the download instructions and mirror sites for Open Images Dataset. Please visit the [project page](https://github.com/openimages/dataset) for more details on the dataset .

# Download Images

## Download Images With Bounding Boxes Annotations
**Prerequisite: Gmail or Gmail associated account**

CVDF hosts 836k image files that have bounding boxes annotations in Open Images Dataset. The images are splited into train, valication, and test sets with 669,124, 41,620, 125,436	 images, respectively. The images are rescaled to 1024x768 resolution with total size 245GB. The images can be directly downloaded into a local directory or a [Google Cloud storage bucket](https://cloud.google.com/storage/transfer/create-manage-transfer-console). Please sign up with your Gmail or Gmail asscociated account [here](http://www.cvdfoundation.org/datasets/open-images-dataset/signup.html) to request access. After you submit the request form, we will grant READ access to your mail account for the storage bucket:
```
gs://open-images-dataset
```
You can either download the images to a storage bucket or a local directory with the following procedures:
1. install [gsutil](https://cloud.google.com/storage/docs/gsutil)
2. gcloud auth login [your_mail_account]
3. gsutil -m rsync -r gs://open-images-dataset [your_local_dir or your_google_storage_bucket]

## Download Full Dataset With Google Storage Transfer
**Prerequisite: Google Cloud Platform Account**

In this section, we describe the procedures to download all images in the Open Images Dataset to a Google Cloud storage bucket. We recommend to use the user interface provided in the Google Cloud Storage console for the task.

Google Storage provides a "storage transfer" function to transfer online files into a user's storage bucket. This function can be used to trasnfer images from original urls into user's storage bucket. CVDF prepares tsv files that contain all image urls for the transfer. The step-by-step instructions are described in [Creating and Managing Transfers with the Console](https://cloud.google.com/storage/transfer/create-manage-transfer-console). The size of whole dataset is around 18TB. please note that user needs to pay for hosting the dataset on Google Cloud Storage after downloading it. The hosting price can be found on [Google Cloud Storage Pricing](https://cloud.google.com/storage/pricing).

The tsv file for the train set (partitioned into 10 files):  
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-train[0-9].tsv

The tsv file for the validation set:  
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-validation.tsv

The tsv file for the test set:  
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-test.tsv

