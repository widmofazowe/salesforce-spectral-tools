# salesforce-spectral-tools

# Installation
production - `https://login.salesforce.com/packaging/installPackage.apexp?p0=04t1t000003PisI`

sandbox - `https://test.salesforce.com/packaging/installPackage.apexp?p0=04t1t000003PisI`

# Callouts
You can enqueue callout to external servie which is trackable by following command:
```spectral.CalloutService.enqueue(relatedObjectId, endpoint, payload);```

relatedObjectId - for tracking purposes, can be null

endpoint - endpoint to external service. It must be added to Remote Site Settings. eg. https://example.com/api/state/closed

payload - strigified payload passed to external service, eg. `JSON.serialize(new Map<String, Object>{'key' => 'value'})`
This method makes a POST request with payload as a json body.

Such a callout can be later displayed at a Callout tab.

Cleanup job - there is a cleanup job scheduled for cleaning successfull callouts older than 2 days

# AOs


# Utils


# Maintenance Tasks

