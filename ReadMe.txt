{\rtf1\ansi\ansicpg1252\cocoartf1343\cocoasubrtf160
{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\deftab720
\pard\pardeftab720

\f0\b\fs24 \cf0 \ul \ulc0 Issues
\b0 \ulnone \
\
1. When you run your app and rotate the device/emulator are the methods displayed in the\
TextView consistent with methods called in the log? If not what would you have to do to\
make them consistent?\
\
No. The methods displayed in the TextView are not consistent with the methods called in the log. When the screen is rotated, the activity is suspended which calls 
\b onSaveInstanceState() 
\b0 method. This gets logged but is not displayed on screen because the activity is suspended by the time it gets displayed.\
\
A possible solution would to display method name of onSaveInstanceState() from 
\b onCreate() 
\b0 method after checking if the state was actually saved. If the app is created newly, then it is not displayed.}