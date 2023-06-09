# Unlocking the Power of Data Visualization: A Step-by-Step Guide to Using Amazon S3 and QuickSight 

## Overview

- Get UEFA data from my GitHub repository.
- Store dataset into an Amazon S3 bucket.
- Connect the S3 bucket with QuickSight and create visualizations.

## Download files from GitHub
1. Navigate to my ***[GitHub repository](https://github.com/GivenCingco/AmazonS3-with-Amazon-Quicksight-to-visualise-UEFA-stats)***. Dataset originally taken from this website ***[https://www.kaggle.com/datasets/azminetoushikwasi/ucl-202122-uefa-champions-league](https://www.kaggle.com/datasets/azminetoushikwasi/ucl-202122-uefa-champions-league)***

2. Click on the `key_stats.csv` file.



   ![Unlocking the Power of Data Visualization_ A Step-by-Step Guide to Using Amazon S3 and QuickSight  - Step 2](https://github.com/GivenCingco/AmazonS3-with-Amazon-Quicksight-to-visualise-UEFA-stats/assets/50238769/48208b19-69d7-441f-91b7-e19c839f600a)

   - Press the download button.
   - Click `raw`

![Unlocking the Power of Data Visualization_ A Step-by-Step Guide to Using Amazon S3 and QuickSight  - Step 3](https://github.com/GivenCingco/AmazonS3-with-Amazon-Quicksight-to-visualise-UEFA-stats/assets/50238769/85239d7c-5409-4d1f-b53e-b3b15cca96e5)


   - Press `ctrl + s` to save into your downloads folder.
3. Download the `manifest.json` file. We will use this file later for Quicksight to access the Amazon S3 bucket. To download the file click `manifest.json` file and follow the same guidelines you used to download the `key_stats.csv`.
   

## Set up S3 bucket

4. Go to the AWS management console and search for Amazon S3, then select it.

![Unlocking the Power of Data Visualization_ A Step-by-Step Guide to Using Amazon S3 and QuickSight  - Step 7](https://github.com/GivenCingco/AmazonS3-with-Amazon-Quicksight-to-visualise-UEFA-stats/assets/50238769/d1297b35-f1f4-457a-a919-266cd92c4d41)


5. Click on the orange button with the text "Create bucket".
   - Give it a name.
   - Click the "Bucket name" field and give it a globally unique name.
   - Keep the rest of setting as default and select "Create".
6. Click on the bucket you just created.



![Unlocking the Power of Data Visualization_ A Step-by-Step Guide to Using Amazon S3 and QuickSight  - Step 10](https://github.com/GivenCingco/AmazonS3-with-Amazon-Quicksight-to-visualise-UEFA-stats/assets/50238769/3101a699-f541-4aa2-a72b-e23b7ee7a83a)


7. Open up the `manifest.json` file on your IDE of choice.



![Screenshot 2023-05-08 at 17 35 44](https://user-images.githubusercontent.com/50238769/236867065-781e4149-86e6-46d8-84a2-6f10d8f769eb.png)



   - Under URIs, change and put your bucket name.
8. Upload the `manifest file` after saving your changes. Also upload the `key_stats.csv` file in the same bucket.


![Unlocking the Power of Data Visualization_ A Step-by-Step Guide to Using Amazon S3 and QuickSight  - Step 11](https://github.com/GivenCingco/AmazonS3-with-Amazon-Quicksight-to-visualise-UEFA-stats/assets/50238769/40a0f921-a924-445b-9131-4fbfc258f085)



## Amazon QuickSight

1. Duplicate your console page and type QuickSight.
2. If you don't have a QuickSight account yet create one by clicking on "sign up for QuickSight".
3. Start the free trial of Amazon QuickSight enterprise edition. Cancel your subscription before 30 days to avoid charges.
4. Enter your name under "Account info".
5. Enter email address under "Notification email address".
6. Under "IAM Role", select Amazon S3 and select the bucket you want to link to QuickSight. Click the bucket checkbox and click "Finish".
7. Keep the rest of the settings as default and click "Finish".
8. Wait a few minutes for your QuickSight account to be created before moving to the next step.
9. Click on "Go to Amazon QuickSight" button.
10. You'll be taken to the Amazon QuickSight page.
11. Click on "Datasets" -> "New dataset" -> "S3".
   - Go to your S3 bucket, click on the manifest file, then copy "S3 URL".
   - Back to the QuickSight tab and paste the URI into the URI text box. This provides QuickSight with the necessary instructions to import the CSV from the S3 bucket.
   - Write any name under the "Data source name" input box and click "Connect".
   - Click "Visualize".
   - Select the interactive sheet option and click "Create". Wait for your data to be imported.
   - Rename the sheet with an appropriate name.
   - Mention the goal of this visual.
     - Drag the player name field to the graph. To sort click on brand -> Sort options -> Sort by the player name and make the sort order DESC and press apply. The graph will be sorted by the players with most goals to the least goals.
     - Drag the goals into the graph.
     - Play around and create your own visualizations.
