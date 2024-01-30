Daily Notes : Day 74 
Denial of Service - Part 1

1. Cookie bomb
https://<domain>.com/index.php?param1=xxxxxxxxxxxxxx

2. Try input a very long payload to form. For example using very long password or using very long email
username=victim&password=aaaaaaaaaaaaaaa

3. Sometimes in website we found a parameter that can adjust the size of the image, for example
https://<domain>.com/img/vulnerable.jpg?width=99999999999&height=99999999999
4. Pixel flood, using image with a huge pixels

5. Frame flood, using GIF with a huge frame

6. Sometimes in website we found a parameter that can adjust the size of the image, for example

7. Sometimes if you try bug "No rate limit", after a long try it. The server will go down because there is so much requests