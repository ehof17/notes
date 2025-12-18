### Overall:
- find what are we looking to improve? Engagement, clicks, bids etc
- decide on rating system
- 



### Idea 1. Webhook tracking opens
Idea is whenever a user opens an email, we can see what items were reccomended to them. Only count the item being seen if the email has been open.

1. Webhook.
    Need to create webhook that is accesible by Iterable whenever a user opens the email6
    Need to ensure the content of the email will be accessible by the webhook
    > Why? Since recs change every day, it will be hard to determine which items they were shown, if they open the email after the daily re embed random
    If the content of the email isn't accesible, will need to find another route
    Doesn't look like the content of the email is accessible


2. Apply a subset of campaigns to use the webhook.

3. Run experiments
   > What do we experiment?


### Idea 2. Track a subset of items
To get around the limitations presented, could we store a subset of item ids that are most relavent to the user on a given day

Cons: 
A ton of storage. 298447 emails, 301548 crmids
Not sure if needed for everyone

Pros:
Can translate into testing trade pub sites easier


### Idea 3. Webhook tracking sends
Idea is whenever a user is sent an email, We store the items that were going to be on it

> How do we determine what was in the email?
- Need to determine what datafeed was used in the email
- Need to determine what templateID it was 
- Email blast send event will return
  - contentId, email, campaignId, templateid, messageId
  - channelId, messageTypeId, experimet

- Upon receiving messageType Id can parse out the siteName from Recsys Site filter.
- It will need the other parameters from the datafeed.
- OR! We could use 



#### Idea 3. Option 1: Try and re create the datafeed contents
##### Recsys Site Filter parser
- Dynamically grab the snippet from Iterable Api 
- Determine what siteName is given to a specific messageTypeId
> Might want to move away from recsys site filter 

###### Determining other data feed params
Problem: No immediate way to determine what data feed was used
Solution: Adding another param to the request, then parsing it out in the python api aby Looking at the logs
Add templateId

Determine which data feed the email used
Store a mapping from identifier to data feed identifier
Store the contents of the datafeed externally
Are all data feeds even being used?
Can we just assume everything we are testing will use similar data feeds for now

 RecSys - Activity - Auction/Retail - Paid Seller No Country Filter - 12 Listings
RecSys - Activity - Retail - Variable Site/TLD - 12 Listings



OR...
Look at the logs to the TPP/python recsys apis
See the items that were requested at the same time with the same crmid/email as the email was sent to




#### Idea 3. Option 2: Store the entire email content
Pros: Will require less parsers and logic

- Biggest unknown is how to see programatically how to get the datafeed and parameters
- ClientTemplateID?

Cons: More storage
- possibly different email parsers for every templateID
- Might be hard with templates that have recsys and non recsys items on the same page
- 

### Idea 4: Using viewInBrowser
> Doesn't work. Using viewInBrowser will call the API again, so the view we see isn't the view the customer saw
- Log the messageId for all requests coming in from recsys
- Then later down the line call /api/email/viewInBrowser 
  - Will only work if the data feed content is stored.
  - If iterable will re attempt to call the API, then it won't work

