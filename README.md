EEG
===

Measurement of EEG signal and sending them to server and having a csv copy on the device


###HelloEEGActivity
===============

This class is the proprietory class of NeyroSky API and example class given with the bundle. 
```
                tv.append("Got XXX: " + msg.arg1 + "\n");
```
Is the line that actually prints the required signal on the mobile device screen. The XXX denotes
the multiple cases that correspond to the message received from the device: Raw Data, Heart Rate, 
Attention, Meditation,Eye Blinks. <br>

```
                int att = msg.arg1;
            		ATT = String.valueOf(att);
            		
            		WriteToCSVFile csvWrite = new WriteToCSVFile();
					      csvWrite.generateCsvFile(Attention, ATT);
```
This section of the code is from the Attention case and shows us the way to write the data in a csv file.

```
                public static String SERVER_URL = "http://192.168.0.105:8081";
```
In case of your use, change this line to suit as per necessity.

###WriteToCSVFile
==============

This class is mainly to write the data from the Attention and Meditation case to a csv file with a time stamp.

###ServerPost
==============
This class has been integrated into the project to send incoming data from the BCI device to the local server for further analysis of the work. 
