# Basic Example: Adobe Analytics v2.0 API

The goal of this example is to simply "pull a simple table of data." Because of the way the v2.0 API works, to keep it _simple_, this code is limited to a single dimension and a single metric.

This requires a different kind of API access than was required for the v1.4 API (which simply required the user to have Web services access, and then just used the client ID and secret from that). So, you will need to have -- or have the assistance of someone who has -- Adobe I/O Console admin access.

What's needed (each of these values are required for the code to run):

* `api_key` -- this is a key that is available once you create an Adobe I/O OAuth client in the Adobe I/O console. For details, see [Adobe's documentation](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/create-oauth-client.md) and/or [this video by Jen Lasser](https://helpx.adobe.com/analytics/kt/using/postman-analytics-api2-requests-technical-video-use.html).
* `company_id` -- you can get this from the [Swagger interface](https://adobedocs.github.io/analytics-2.0-apis/) for the Adobe Analytics API. Jen explains how to do that starting at the 1:37 mark in [the same video referenced above](https://helpx.adobe.com/analytics/kt/using/postman-analytics-api2-requests-technical-video-use.html).
* `aa_rsid` -- this is just the report suite ID. You can grab this from your website or the plain ol' Adobe Analytics Admin Console (no fancy Adobe I/O stuff needed for this).
* `aa_token` -- this comes from the Analysis Workspace debugger tool. Details on how to enable that are available in [Adobe's documentation](https://github.com/AdobeDocs/analytics-2.0-apis/blob/master/reporting-tricks.md). Follow steps 1 through 6 and then grab the *Authorization:* value from the *CURL REQUEST* section of any request you inspect with the little bug icon. This token will expire periodically and will have to be updated in the code. OR, if you've got the coding chops, you can [see Adobe's OAuth documentation](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/create-oauth-client.md) and code a more robust solution.

Once you've got those values, just plug them into the first code snippet in `aa-simple-ranked.Rmd` and you should be off to the races.
