Use the link below to do grid convergence:

https://www.ngs.noaa.gov/NCAT/

The NCAT webpage allows you to convert coordinates and at the same time will calculate grid convergence as part of the output.

Both single and locations can be converted at a time.  The results can be exported as an Excel spreadsheet.  The grid convergence is in the column 'spcConvergence' and is in DMS format.  Insert a new column to the right of the 'spcConvergence' column and then copy the formulae below to convert the DMS to decimal degrees.

=VALUE(MID(Y5, 1, FIND(" ",Y5, 1)-1))+VALUE(MID(Y3, FIND(" ",Y3, 1)+1,2))/60+VALUE(MID(Y4, FIND(" ",Y4, 1)+3,16))/60
