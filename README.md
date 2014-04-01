photohunt-server
================

A server application for Photohunt. Restful API for uploading pictures and 
stuff.

##Pages##
###/upload###
Make a POST request here to upload a picture.
####Parameters####
key: the api key for a team
hash: a sha256 hash of the binary data of the image, encoded in base64url
fileextension: The file extension of the image. Probably png or jpg
####Post Body####
A base64 encoded image file, to be submitted

###/times###
Make a GET request here to get the times Photohunt is happening
####Parameters####
key: the api key for a team
####Returns####
A time period formatted as:
>Mar 31, 2013 at 07:13 until Mar 31, 2013 at 21:33

###/numpics###
Make a GET request here to get the number of pictures a team has uploaded, out
of the total number of the pictures they can upload.
####Parameters####
key: the api key for a team
####Returns####
Two numbers formatted as:
>0 / 20
