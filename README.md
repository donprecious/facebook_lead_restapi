# facebook_lead_restapi
this api connect to facebook in other to retive lead data filled by user
this api is hosted in https://www.facebookleads.wellnessanddiets.com as a sub domain for testing purpose 

Root Url https://facebookleads.wellnessanddiets.com/
1- GET api/fb/leads  - retrive default lead data by leadId using 1989755784405615 as the default Lead id

response 
{
  "data": [
    {
      "created_time": "2018-02-28T08:49:14+0000", 
      "id": "<LEAD_ID>", 
      "ad_id": "<AD_ID>",
      "form_id": "<FORM_ID>",
      "field_data": [
        {
          "name": "car_make",
          "values": [
            "Honda"
          ]
        }, 
        {
          "name": "full_name", 
          "values": [
            "Joe Example"
          ]
        }, 
        {
          "name": "email", 
          "values": [
            "joe@example.com"
          ]
        },
      ], 
      ...
    }
  ],
  "paging": {
    "cursors": {
      "before": "OTc2Nz3M8MTgyMzU1NDMy", 
      "after": "OTcxNjcyOTg8ANTI4NzE4"
    }
  }
}


2- GET api/fb/leads/{leadId} 
get leads data by lead id, pass leadId parameter with an actual value e.g 1989755784405615 

Response 
response is similar to the previous code in 1- GET api/fb/leads 

3- GET api/fb/ads/{adId}/leads 
Gets all lead data associated to a ads, pass adId by an actual value of an AdId or a adGroup id 
Response 
{
  "data": [
    {
      "created_time": "2018-02-28T08:49:14+0000", 
      "id": "<LEAD_ID>", 
      "ad_id": "<AD_ID>",
      "form_id": "<FORM_ID>",
      "field_data": [
        {
          "name": "car_make",
          "values": [
            "Honda"
          ]
        }, 
        {
          "name": "full_name", 
          "values": [
            "Joe Example"
          ]
        }, 
        {
          "name": "email", 
          "values": [
            "joe@example.com"
          ]
        },
        {
          "name": "selected_dealer", 
          "values": [
            "99213450"
          ]
        }
      ], 
      ...
    }
  ],
  "paging": {
    "cursors": {
      "before": "OTc2Nz3M8MTgyMzU1NDMy", 
      "after": "OTcxNjcyOTg8ANTI4NzE4"
    }
  }
}

4 - GET api/fb/Form/{formId}/leads 
Get lead data by its form Id 

