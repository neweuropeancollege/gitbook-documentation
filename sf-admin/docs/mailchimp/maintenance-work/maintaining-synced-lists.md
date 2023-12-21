# Maintaining Synced Lists

For example when someone is deleted on Salesforce, which can be as a result of
* a duplicate contact being merged
* a contact being deleted

then the contact will be archived on Mailchimp as well. This is because the MC2SF app only creates and updates contacts on Mailchimp when they meet the conditions we have defined, but does not archive them when they don't. It simply does not update them anymore.