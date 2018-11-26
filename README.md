# sfdx-community-ignore
SalesforceDX for Salesforce Community to ignore common APEX classes and files that come standard with scratch org when working with DX CLI

While working with Community in SalesforceDX and Scratch ORGs many standard and sample components, classes and pages are added. But we not always want all this defgault code in our repository. This `.forceignore` helper file try to define all these metadata elements to avoid copy them during `force:source:pull` and `force:source:push` DX CLI operations.

## Exception to the rule
Ojne exception can be if our DX project has work on these files such as custom Self Registration code in teh components or APEX classes. In this case we need to remmove some or all of tehse items from this ignore file.
