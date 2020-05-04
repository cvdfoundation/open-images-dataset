# Open Images Dataset
Open Images is a dataset of ~9 million URLs to images that have been annotated with labels spanning over 6000 categories. This page aims to provide the download instructions and mirror sites for Open Images Dataset. Please visit the [project page](https://storage.googleapis.com/openimages/web/index.html) for more details on the dataset.

# Download Images

## Download Images With Bounding Boxes Annotations

CVDF hosts image files that have bounding boxes annotations in the Open Images Dataset V4/V5. These images contain the complete subsets of images for which instance segmentations and visual relations are annotated. The images are split into train (1,743,042), validation (41,620), and test (125,436) sets. The train set is also used in the Open Images Challenge 2018 and 2019.
The images are rescaled to have at most 1024 pixels on their longest side, while preserving their original aspect-ratio. The total size is 561GB. The images can be directly downloaded into a local directory from the CVDF AWS S3 cloud storage bucket:
```
s3://open-images-dataset
```
You can either download the images to a local directory or to your own AWS S3 cloud storage bucket with the following procedures:
1. install [awscli](https://aws.amazon.com/cli/)
2. download images for the train set, validation set, test set:
  * aws s3 --no-sign-request sync s3://open-images-dataset/train [target_dir/train] (513GB)  
  * aws s3 --no-sign-request sync s3://open-images-dataset/validation [target_dir/validation] (12GB)  
  * aws s3 --no-sign-request sync s3://open-images-dataset/test [target_dir/test] (36GB)
  
Alternatively, you can download the subsets in separate packed files (the subset train_x contains all images with ID starting with x):
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_0.tar.gz [target_dir] (46G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_1.tar.gz [target_dir] (34G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_2.tar.gz [target_dir] (33G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_3.tar.gz [target_dir] (32G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_4.tar.gz [target_dir] (31G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_5.tar.gz [target_dir] (31G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_6.tar.gz [target_dir] (32G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_7.tar.gz [target_dir] (31G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_8.tar.gz [target_dir] (31G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_9.tar.gz [target_dir] (31G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_a.tar.gz [target_dir] (31G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_b.tar.gz [target_dir] (31G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_c.tar.gz [target_dir] (31G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_d.tar.gz [target_dir] (31G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_e.tar.gz [target_dir] (28G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/train_f.tar.gz [target_dir] (28G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/validation.tar.gz [target_dir] (12G)
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/test.tar.gz [target_dir] (36G)



The target_dir can be a local directory or a AWS S3 cloud storage bucket.


## Download the Open Images Challenge 2018/2019 test set

CVDF also hosts the Open Images Challenge 2018/2019 test set, which is disjoint from the Open Images V4/V5 train, val, and test sets. The same AWS instructions above apply. Note that since the images from the 2019 challenge have not changed, the filenames only include the year 2018.

  * aws s3 --no-sign-request sync s3://open-images-dataset/challenge2018 [target_dir/test_challenge_2018] (10GB)

  We also provide the zipped file for challenge 2018/2019 set. You can download the zipped file using
  * aws s3 --no-sign-request cp s3://open-images-dataset/tar/challenge2018.tar.gz [target_dir] (9.7G)
  

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

