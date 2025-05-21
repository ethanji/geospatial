ReadMe: ‘DataGov_API_GeoMD_Tool_v1.R’Script

Andrew Beggs (General Engineer), Department of Commerce - Office of Inspector General
(Shared by) Ethan Iczkovitz on behalf of Andrew.

Purpose, Source, Scope, Conclusion

Purpose:

This software script intends to assist the user(s) quickly and easily:
1.
read in data across about a number of geospatial metadata records via the Data.gov Application Programming Interface (API)
2.
parse (i.e., process) the information sent from the Data.gov API
3.
perform the selected series of reliability and quality tests on the metadata present, including:
3.1 determine if data exists (reliability)
3.2 determine if data allowed/disallowed values and/or stored in proper format(s) (quality)
3.3 determine and test other attributes (e.g., data reliability, date validation, keyword formatting) (quality)
4.
aggregate results across all data records read in via the Data.gov API (
see step (1)
)
5.
automatically write results for further analysis and review
This notebook documents the key parts of the script’s code that are most impactful to meeting these objectives. All code will bereproduced, in full, at the end of this file.
Source:
This resource was developed in response to the administrative and technical challenges associated with both retrieving and thenreviewing any reasonable number of geospatial metadata files, consistent with effective Office of Inspector General oversight onto anagency’s geospatial data resources.
Without a resource like this, auditors can still locate, download, and open an individual records’ geospatial metadata (e.g., in a webbrowser). However, in order to determine the availability and relative quality of information present in the metadata file, auditors wouldneed to locate each valid data location within the file (a.k.a. searching for the correct “XPath”), copy or view that information, and thenoverlay best practices to determine suitability of the information supplied.
Whereas, computers are well-suited to this exact tedium of locating, downloading / obtaining, reviewing large amounts of data by using arobust-yet-adaptable series of logical checks, aggregating results, and reporting results.
Specifically, this script sources its data from the Data.gov
API (https://catalog.data.gov/)

variable detects of form: MM-DD-YYYY (or longer).
Date REGEX required and used in datevalidation():
To be updated (2-28-2025); we are not using the datevalidation() function any more. These two headings cover the two main groups(pattern-format and valid date digits).
End of ReadMe
