# Set Up Your Signature

### Overview

To set up the signature, we first need to make sure links to Facebook, LinkedIn, and Skype are mentioned on your profile as well as a link to your picture, so that they go onto your signature. Then we need to add the signature to your signature settings. You will also add your profile picture to your Salesforce profile now.

### Going to your profile to add the links

1. Click on your picture top right
2. Click on your name
3. Click on the circle on the left where your photo should be and upload your photo.
4. Click edit on the top right
5. Fill in Link to Schedule Calendly, Link to LinkedIn, and Invite to Skype
6. Fill in Link to Profile picture (take the link from the picture uploaded to our [www.new-european-college.com/admindashboard](https://www.new-european-college.com/) website - ask someone who has access to give you the link if admin hasn't sent it already)
7. Link should look something like this -> https://www.new-european-college.com/cms/wp-content/uploads/....

### Going to your personal settings to add the email signature HTML

Once that's done

1. Click on your picture on the top right again.
2. Click Settings
3. Click My Email Settings (under Email)
4. Copy the following text into the email signature box

{% code overflow="wrap" fullWidth="false" %}
```html
{{{Recipient.Informal_Greeting__c}}}<br/><br/><br/><br/>Best regards,<br/>{{{[Sender.Name](https://sender.name/)}}}<table style="border-spacing: 10px; border-collapse: separate;"><tbody><tr><td><table><tbody><tr><td><img style="width: 130px; border-radius: 50%;margin-right:20px" src="{{{Sender.Profile_Picture__c}}}"/></td><td style="color: [#7f7f7f](javascript:void(0););"><span style="font-size: 10pt; font-family: Arial, Sans-Serif;"><strong>{{{[Sender.Name](https://sender.name/)}}}</strong> | {{{Sender.Title}}}</span> <span style="font-size: 8pt; font-family: Arial, Sans-Serif;"> <br/>{{{Organization.Phone}}}<br/>{{{Sender.Email}}}<br/>[www.new-european-college.com](https://www.new-european-college.com/)<br/><a href="{{{Sender.Calendly_Link__c}}}">Schedule a call</a> | <a href="{{{Sender.IN_Link__c}}}">LinkedIn</a> | <a href="{{{Sender.SK_Invite__c}}}">Skype | <a href="https://instagram.com/neweurcollege">Instagram</a></span></td></tr></tbody></table></td></tr></tbody></table><p><img src="https://bit.ly/3pOc8tH" width="500px"/></p><p><span style="font-size: 8pt; font-family: Arial, Sans-Serif; color: [#7f7f7f](javascript:void(0););"> New European College GmbH | Wolfratshauser Str. 84, 81379 Munich Gesch&auml;ftsf&uuml;hrer: Sascha Liebhardt | Amtsgericht M&uuml;nchen - HRB 214 932 UStID DE298857192 </span></p>
```
{% endcode %}

5. Save and exit
6. Double check your signature by opening and email composer on Salesforce. (Click on the plus on the top right corner and then Email)
