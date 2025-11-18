# Microservice #4 : Notification Microservice
# Overview
This microservice allows you to send a notification alert to your site. 

# How to request
Data will be requested by a call using fetch call to the program 

request parameters: title, description
example call:

fetch(http://localhost:5004/notifications/send), {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: { 
          targetURL: "http:localhost:5173"
          "title": "New Update Made", 
          "description": "New functionality added for saving items" 
} 
};
  
# How to recieve data:
You will recieve back JSON bpdy that includes a status, message, id, and time

example call:
{ 
  "status": "success", 
  "message": "Notification sent!", 
  "id": 22, 
  "time": "2025-11-03T10:20:00Z" 
}
