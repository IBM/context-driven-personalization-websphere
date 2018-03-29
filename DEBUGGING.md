Troubleshooting
===============

WCS 
---

* Make sure that trace is enabled on ExtSearchDisplayCmdImpl, which is a new command that extends the out-of-box SearchDisplayCmd and also trace is enabled on ExtSearchBoostExpressionProvider, which boosts the search results based on soft parameters like color, material etc.
* Ensure that the entry in the CMDREG table for ExtSearchDisplayCmdImpl is present.
* Also enable a trace on SearchResultsDisplay.jsp, which contains the functionality to fetch personalized vs non-personalized search results. This should help identify which function is invoked.
* Ensure that the right parameters are passed to dataextract.cmd when WCS export/import is invoked. To help troubleshoot errors that are encountered, review the wc-dataextract.log file as the first step in determining the source of your error.This would be present within WCDE_InstallDir\logs.
* Ensure that the output directory where PCI places the files is the same directory from  which WCS import happens.
* Cross-verify that the attributes that are made searchable and facetable via the WCS Management Center show up on the Aurora storefront as facet attributes.
* Cross-check if the right attributes are selected as filters in the personalized search results, by checking in ATTR table for those rows with FIELD1=0.These attributes are the ones considered for search filtering.



