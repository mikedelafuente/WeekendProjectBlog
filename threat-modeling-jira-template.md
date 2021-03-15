# Threat Modelling Jira Template

**All Epics MUST have a threat model OR a note with the rationale for not needing
one** in order to meet our compliance audit requirements. Use this template to
guide deciding when a threat model is relevant and to document the required
information, which helps satisfy PCI and GDPR audit requirements.

The template is formatted for Jira.

```
h2. Threat Modeling Jira Worksheet

Security/Senior or higher Engineer:
Software Engineer of any level: 
Quality Engineer: 

Do I need threat modeling checklist:
{noformat}
[ ] Storing/Displaying user input*
[ ] Display PII (Personally Identifying Information)
[ ] Storing PII
[ ] Transmitting PII
[ ] New Third Party resources are being introduced (Libraries, page redirects, etc)
[ ] Uploading files
[ ] Stealth Access
[ ] Proxies
{noformat}

*Is any of the following information stored, viewed, or transmitted?*
{noformat}
[ ] Name
[ ] Address
[ ] Email Address
[ ] Phone Number
[ ] Bank Information (routing, account number, etc)
[ ] Credit Card Information
[ ] Signatures (images of signatures, documents with signatures)
[ ] Tax identifiers such as SSN
[ ] Date of birth
[ ] Login information (username or password)
[ ] IP address
[ ] External account information
    [ ] Policy number
    [ ] Group number
    [ ] PIN numbers
    [ ] Login information
    [ ] API Keys and passwords
{noformat}

*If none of the items are checked please explain in one or more sentences why threat modeling is not needed. This is a PCI and GDPR requirement. The reason cannot be because "nothing is checked" as the checklist was development in house.*

Skip the remaining steps if threat modeling is not needed.

*If no security measures are in place list the possible threats. Who would likely attack our products?*
    _Example:_
    _Employees with stealth access_
    _Partners with admin rights_
{noformat}
{noformat}

*List how can these threats be enabled (vulnerabilities). What are the vulnerabilities in the feature?*
    _Example:_
    _Transmission of data can be intercepted_
    _Sensitive data exposure_
{noformat}
{noformat}

*List the possible motivations of an attacker. Why would the attacker use these vulnerabilities?.*
    _Examples:_
    _Identity theft_
    _Financial harm_
{noformat}
{noformat}

*Map each attacker to the applicable vulnerabilities and rank the likelihood and impact of each vulnerabilities 1-5 where 1 is the lowest and 5 is the highest for determining order of importance.*
*When ranking likelihood ask yourself what are the chances of this happening?*
*When ranking impact ask yourself what would be the consequences to Infusionsoft be if this happened (financially and reputationally)?*
    _Example:_
    _Employee with stealth access steal exposed sensitive data 1 Impact 5_
{noformat}
{noformat}

*What are the countermeasures for each vulnerability (one sentence for each)?*
    _Example:_
    _Permission level access to prevent IS employee or partner from accessing specific information_
{noformat}
{noformat}
```
