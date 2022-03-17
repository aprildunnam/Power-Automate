## Outlook Integrated Busy Light Automation
If you have housemates, it can prove to be difficult to keep them out of your home office when you're in a meeting

This Power Automate Flow demonstrates how to kick off an automation when an event is starting on your Outlook Calendar which can integrate with the home automation service, IFTTT to toggle a smart light on and off.  That way your house mates know you're in a meeting.

## Hardware used
* On Air Sign: [https://www.amazon.com/dp/B098D9S5RQ/ref=cm_sw_r_tw_dp_Y0H8WZKZFWVPWABP15QF ](https://www.amazon.com/dp/B098D9S5RQ/ref=cm_sw_r_tw_dp_Y0H8WZKZFWVPWABP15QF )
* Kasa Smart Plug: [https://www.amazon.com/dp/B07B8W2KHZ/ref=cm_sw_r_tw_dp_dl_C6W5WWX96ETST8KVJZ2N?_encoding=UTF8&psc=1 ](https://www.amazon.com/dp/B07B8W2KHZ/ref=cm_sw_r_tw_dp_dl_C6W5WWX96ETST8KVJZ2N?_encoding=UTF8&psc=1 )

The setup was simple. I mounted the sign at the top of the doorframe and used some cable management tools to feed the cable along the frame. I then plugged it into a nearby outlook which I connected the Kasa smart plug to.

## Create the IFTTT Applet

You'll need to create two new Applets in IFTTT to turn your Kasa smart plug on and off. You'll use the Webhook trigger for each. Create one with an event name called on_air and a Kasa Action to toggle your plug on and another with an event name called off_air with a Kasa Action to toggle for plug off.

## Using the Flow for Outlook Integration

Once you have the IFTTT Applets created, download the zip file in this repo which includes the Power Automate flow.  This flow has everything you need in it to trigger an automation when an event is starting and call your IFTTT Applet to toggle your light on and off.

To import this flow do the following:
* Download the zip file
* Go to flow.microsoft.com
* Select "My Flows" in the left hand side
* Select "Import"
* Select "Upload" and browse to the downloaded zip
* Select "Import"
* If promoted, create a new connection to the Outlook connector
* Once flow is imported, click "Edit" to open in edit mode
* Expand the "Post to IFTTT to Set Busy Signal" action
* Replace the "youreventname" text with the event name of your IFTTT toggle on applet
* Replace the "your IFTTTKey" with your IFTTT key (I show how to get this in the corresponding video tutorial)
* Expand the Post to IFTTT to Set Free Signal action
* Replace the "youreventname" text with the event name of your IFTTT toggle off applet
* Replace the "your IFTTTKey" with your IFTTT key (I show how to get this in the corresponding video tutorial)
* Click Save to save your changes
* Click the back button to go to the flow settings page
* In the ribbon at the top, if it says "Turn on" make sure you click that to ensure the flow is on

## Video Walkthrough
I created this turtorial video that walks through how to set up the solution:
[Video tutorial](https://youtu.be/pv650wWRBm8)