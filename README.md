Google Drive → YouTube & X Auto Poster

What it does:
When a new video is added to a Google Drive folder, this workflow uploads it to YouTube and posts a tweet on X with the same caption.​

Trigger:
Google Drive Trigger (file Created) – watches a specific folder and starts the workflow when a new file appears.

Steps:
Google Drive Download – downloads the new file as binary.
Set Caption + URL – creates a caption from the file name (e.g., “New video: <file name>”).
Upload a video (YouTube) – uploads the video using YouTube credentials and sets it to Public.
Create Tweet (X) – posts a tweet with {{ $json.caption }} using X OAuth credentials.​

How to test:
Configure credentials for Google Drive, YouTube, and X in n8n.
Run the workflow once manually from Set Caption + URL with a sample file to confirm upload + tweet.
Enable the Google Drive Trigger, then drop a test video in the watched folder and verify:
Video appears on YouTube.
Tweet is created on the X account with the caption.​
