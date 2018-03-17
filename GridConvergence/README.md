
Use the link below to do grid convergence:

https://www.ngs.noaa.gov/NCAT/

The NCAT webpage allows you to convert coordinates and at the same time will calculate grid convergence as part of the output.

To do multipoint conversion, select the 'Multipoint Conversion' tab. Then click the '+ Choose' button to select a file with a list of locations to convert. After the file is uploaded, a list of download formats will be presented.  A description of the upload file format for doing multipoint conversion is found here:

https://www.ngs.noaa.gov/NCAT/readme_upload.txt

Here is an example:

ID,lat,lon,eht,inDatum,outDatum,spcZone,utmZone  
ABCD,37.393300000,-92.459040000,0.0,NAD83(1986),NAD83(2011),2401,auto  
EFGH,37.393300000,-96.0,0.0,NAD83(1986),NAD83(2011),auto,15

The important columns are ‘spcZone’ and ‘utmZone.’  By putting ‘auto’ in either, the system will make its best guess at the target zone based on the ‘outDatum.’  To set the ‘spcZone’ directly, for example, the codes may be looked up in the COUNTYSPC.XLS in this repository.  The columns are ‘SPC27’ and ‘SPC83’ in the COUNTYSPC.XLS file.  The same may be done for the utm zones.  The codes are in the column ‘UTM.’

Both single and multiple locations can be converted at a time.  The results can be exported as an Excel spreadsheet.  The grid convergence is in the column 'spcConvergence' and is in DMS format.  Insert a new column to the right of the 'spcConvergence' column and then copy the formulae below to convert the DMS to decimal degrees.


=VALUE(MID(Y5, 1, FIND(" ",Y5, 1)-1))+VALUE(MID(Y3, FIND(" ",Y3, 1)+1,2))/60+VALUE(MID(Y4, FIND(" ",Y4, 1)+3,16))/60
