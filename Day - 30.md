Daily notes : Day 30 
File Upload Bypasses
1: Change the ContentType
2: Try to change the extension when send the request, for example in here you cant upload file with ext php but you can upload jpg file
4: Upload the payload, but start with GIF89a; and dont forget to change the content-type to image/gif
5: Using null byte in filename (Payload.php%00.gif)
6: Using double extensions for the uploaded file (file.jpg.php)
7: Uploading an unpopular file extensions 
8: Mix the tips 
*And many more…… 
*mention your favourite ones in comments!!