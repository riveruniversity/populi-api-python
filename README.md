# Populi

This module interacts with the populi api, handling pagination, and rate limiting using pycurl.
Most every command found [here](https://support.populiweb.com/hc/en-us/articles/223798747#getAcademicTerms), can be accessed via pythonic methods. I have attempted to keep the two in sync

## Example
```python
import populi

populi.initialize(
    endpoint='https://example_campus.populi.web.com/api/index.php',
    access_key='example access key',
    asXML=True
)

# returns transactions as xml
results = populi.get_transactions(start_date='2012-10-01', end_date='2012,10-02')
```
## Versions

### 0.0.10
+ Added method set_custom_field_options() to check multiple options via value or option_index parameter.

### 0.0.9
+ Added method get_leads() which has been added to the Populi API Reference List on April 9, 2021.
+ Added method delete_person().
+ Added method get_online_payment_url().

### 0.0.8
+ Forked from https://github.com/mikrjohn/populi-api-python

### 0.0.7
+ Enabled passing curl options via initialize(). The added option list is in the format of tuples: (pycurl.OPTION, value).

### 0.0.6
+ Updated Command list as of commands shown on populi on May 25th, 2020
+ Fixed downloadFile and downloadBackup to return bytes.
