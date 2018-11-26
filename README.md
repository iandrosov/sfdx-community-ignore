# sfdx-community-ignore
SalesforceDX for Salesforce Community to ignore common APEX classes and files that come standard with scratch org when working with DX CLI. This is especially usefull when Community is used to test or validate the code and NOT the main objective for DX project.

While working with Community and SalesforceDX in Scratch ORGs I found that many standard and sample components, classes and pages are added by default. 
Thsi can be handy to pull Community changes to source control but can also bring some sidefects and deployment errors such as these. 

```
──────────────────────────────────
sfdx-lex-knowledge-edit/main/default/approvalProcesses/KnowledgeArticle.KBWorkflow.approvalProcess-meta.xml                       The approval process requires at least one allowed submitter.
sfdx-lex-knowledge-edit/main/default/profiles/Test Knowledge Profile.profile-meta.xml                                             In field: userLicense - noUserLicense named Guest found
sfdx-lex-knowledge-edit/main/default/approvalProcesses/KnowledgeArticleVersion.KBTranslationSubWorkflow.approvalProcess-meta.xml  The approval process requires at least one allowed submitter.
```
We not always want all this default code in our repository. This `.forceignore` helper file try to define most of these metadata elements to avoid copy them during `force:source:pull` and `force:source:push` DX CLI operations.

## Exception to the rule
Ojne exception can be if our DX project has work on these files such as custom Self Registration code in teh components or APEX classes. In this case we need to remmove some or all of tehse items from this ignore file.
