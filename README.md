# Open Images Dataset
Open Images is a dataset of ~9 million URLs to images that have been annotated with labels spanning over 6000 categories. This page aims to provide the download instructions and mirror sites for Open Images Dataset. Please visit the [project page](https://storage.googleapis.com/openimages/web/index.html) for more details on the dataset .

# Download Images

## Download Images With Bounding Boxes Annotations
**Prerequisite: Gmail or Gmail associated account**

CVDF hosts image files that have bounding boxes annotations in the Open Images Dataset V4. The images are split into train (1,743,042), validation (41,620), and test (125,436) sets. There is also a Open Images Challenge 2018 test set, which is completely disjoint from the other three sets. All images are rescaled to 1024x768 resolution with total size 561GB. The images can be directly downloaded into a local directory or a [Google Cloud storage bucket](https://cloud.google.com/storage/transfer/create-manage-transfer-console). Please sign up with your Gmail or Gmail associated account [here](http://www.cvdfoundation.org/datasets/open-images-dataset/signup.html) to request access. After you submit the request form, you can access the cloud storage bucket:
```
gs://open-images-dataset
```
You can either download the images to a storage bucket or a local directory with the following procedures:
1. install [gsutil](https://cloud.google.com/storage/docs/gsutil)
2. gcloud auth login [your_mail_account]
3. download images for the train set, validation set, test set, and the Challenge 2018 test set (please note that the images in the Challenge 2018 test set are completely disjoint from the images in the other sets):
  * gsutil -m rsync -r gs://open-images-dataset/train [target_dir/train] (513GB)  
  * gsutil -m rsync -r gs://open-images-dataset/validation [target_dir/validation] (12GB)  
  * gsutil -m rsync -r gs://open-images-dataset/test [target_dir/test] (36GB)
  * gsutil -m rsync -r gs://open-images-dataset/challenge2018 [target_dir/test_challenge_2018] (10GB)

The target_dir can be a local directory or a Google Cloud storage bucket.

## Download Full Dataset With Google Storage Transfer
**Prerequisite: Google Cloud Platform account**

In this section, we describe the procedures to download all images in the Open Images Dataset to a Google Cloud storage bucket. We recommend to use the user interface provided in the Google Cloud storage console for the task.

Google Storage provides a "storage transfer" function to transfer online files into a storage bucket. This function can be used to transfer images from original urls into user's storage bucket. CVDF prepares the tsv files that contain all image urls in Open Images Dataset for the transfer. The step-by-step instructions are described in [Creating and Managing Transfers with the Console](https://cloud.google.com/storage/transfer/create-manage-transfer-console). The size of the whole dataset is around 18TB. Please note that user needs to pay for hosting the dataset on Google Cloud storage after downloading it. The hosting price can be found on [Google Cloud Storage Pricing](https://cloud.google.com/storage/pricing).

The tsv files for the train set, in 10 partitions:  
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-train0.tsv<br>
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-train1.tsv<br>
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-train2.tsv<br>
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-train3.tsv<br>
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-train4.tsv<br>
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-train5.tsv<br>
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-train6.tsv<br>
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-train7.tsv<br>
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-train8.tsv<br>
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-train9.tsv<br>

The tsv file for the validation set:  
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-validation.tsv

The tsv file for the test set:  
https://storage.googleapis.com/cvdf-datasets/oid/open-images-dataset-test.tsv

The tsv file for the Challenge 2018 test set will be available before the 6th of June.
