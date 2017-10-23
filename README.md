# tap-survey
Temporary Repo

`Requirements
1. Create a view with a text field that takes in an alphanumeric string (user identifier) and a submit button.
2. On submit, make a request to our “Get Survey Offer” API endpoint. 
   1. http://supply-docs.tapresearch.com/#get-survey-offer
      1. This endpoint accepts a “callback” parameter for usage in a JSONP request, to address cross domain issues
   1. API Token: 9a7fb35fb5e0daa7dadfaccd41bb7ad1
   2. Ignore the device identifier parameter
   3. User identifier: “tapresearch”
      1. Anything else will yield has_offer: false
1. Handle response based on the has_offer attribute. 
   1. has_offer: true
      1. Add a “Take Survey” link that points to the offer URL. 
      2. Show the min/max reward amount along with the currency name.
   1. has_offer: false
      1. Display “No survey available”.


Bonus
1. Open a new tab when a user clicks on the “Take Survey” link.
2. Handle timeout scenario. 
3. Validations
   1. Non-empty user identifier
   2. User identifier cannot exceed 32 characters in length
