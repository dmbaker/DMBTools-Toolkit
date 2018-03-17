Use ‘SetDMBToolsLicPathEnvironment.exe’ to set the environment variable ‘DMBTOOLSLICPATH’ to the path to ‘DMBToolsLicense.lic’ license file.  If the environment variable ‘DMBTOOLSLICPATH’ is not set, then the license file must be in the same directory for all licensed applications.  Setting the environment variable allows the license file to reside on a network share that accessible to licensed applications.

The path may be passed as a parameter to ‘SetDMBToolsLicPathEnvironment.exe’ or may be set in the ‘SetDMBToolsLicPathEnvironment.exe.config’ file in the ‘DMBToolsLicensePath’ tag.

Copy the zip file containing ‘SetDMBToolsLicPathEnvironment.exe’ to location where users can run the app.  Each user of a licensed application may run this application to set the ‘DMBTOOLSLICPATH’ environment variable.  Alternatively, the ‘DMBTOOLSLICPATH’ environment variable may be set manually.
