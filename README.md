# Unlocking the Power of Data Visualization: A Step-by-Step Guide to Using Amazon S3 and QuickSight 

## Overview

1. Get UEFA data from my ***[GitHub repository] (https://github.com/GivenCingco/AmazonS3-with-Amazon-Quicksight-to-visualise-UEFA-stats)***
2. Store dataset into an Amazon S3 bucket.
3. Connect the S3 bucket with QuickSight and create visualizations.

## Download files from GitHub

1. Download the dataset of UEFA results 2019-2020 CSV file.
   - Click on the `key_stats.csv` file.
   - Press the download button.
   - Click `raw`
   - Press `ctrl + s` to save into your downloads folder.
2. Download the `manifest.json` file. We will use this file later for Quicksight to access the Amazon S3 bucket.
   

## Set up S3 bucket

1. Go to the AWS management console.
2. Search for S3.
3. Click on "Create bucket".
   - Give it a name.
   - Keep the rest of setting as default and select "Create".
4. Click on the bucket you just created and upload your CSV file.
5. Open up the `manifest.json` file on your IDE of choice.
![Screenshot 2023-05-08 at 17 35 44](https://user-images.githubusercontent.com/50238769/236867065-781e4149-86e6-46d8-84a2-6f10d8f769eb.png)

   - Under URIs, change and put your bucket name.
6. Upload the manifest file after saving your changes.

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
