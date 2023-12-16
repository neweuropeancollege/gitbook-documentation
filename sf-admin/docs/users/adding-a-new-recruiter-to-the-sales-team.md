# Adding a New Recruiter to the Sales Team

The steps in adding a new person to the recruitment team involves configuration within WordPress, Microsoft Azure Portal, Salesforce, and Microsoft Exchange Admin, in that order. These involve the configuration of their Microsoft account, Salesforce account, email redirecting, and files access, respectively.

## WordPress | Upload photo

- First, log onto WordPress as an administrator or an account with the privileges to add files
- Uploading their photo:
  - Navigate to [Media Library](https://www.new-european-college.com/cms/wp-admin/upload.php)
  - Add photo
  - Locate URL pointing directly to photo and save it for later

## Azure Configuration | Create new user

- First, log onto Microsoft as administrator or an account with the privileges to create users
- Create user account in the Azure Portal
  - Navigate to [Users page](https://portal.azure.com/#view/Microsoft_AAD_UsersAndTenants/UserManagementMenuBlade/~/AllUsers)
  - Select `New user` and `Create new user`
  - Enter all relevant information
  - Create

## Salesforce Configuration | Create and set up new user

- First, log onto Salesforce as administrator
- Add to `Users` picklist value set
  - Adding the value
    - Navigate to [Picklist Value Sets](https://nec.lightning.force.com/lightning/setup/Picklists/home)
    - Find the `Users` set and open it
    - Under the `Values` section, click `New`
    - Enter the full name
    - Check `Add the new picklist values to all Record Types that use this Global Value Set`
    - Save
  - Reordering the value set
    - Under the `Values` section, click `Reorder`
    - Check `Display values alphabetically, not in the order entered`
    - Save
  - Assigning a chart color
    - Click `Edit` on picklist value of new user
    - Click on the color input element next to `Chart Color` and pick a color
  - Fix Task SF Bug
    - Navigate to [Task Object](https://nec.lightning.force.com/lightning/setup/ObjectManager/Task/Details/view)
    - Click `Record Types` on the left pane
    - For every record type,
    - Open and click `Edit` next to `User` field
    - Move the name from left to right pane
    - Save
  - Create new user
    - Navigate to [Users page](https://nec.lightning.force.com/lightning/setup/ManageUsers/home)
    - Click `New User`
    - Data entry
      - Name information
      - `Email` email from **step 1** in _Azure Configuration_
      - `Title` Admission Consultant
      - `Company` New European College
      - `Department` Recruitment and Admissions
      - `User` License: Salesforce
      - `Role` Sales Team
      - `Profile` NEC Recruiter
      - `Profile` Picture: URL from step 1 of WordPress Configuration
      - `Label` what you put in step 1.1.4.
      - `Label` Name: same as previous step
    - Save
    - The user receives an email to set password
  - Assign permissions
    - Navigate to the user page of the user you just created in Setup
    - Find `Permission Set Assignments`
    - Click `Edit Assignments`
    - Assign Can See Recruiter Dashboards, Can Deactivate Requirements, Trailhead User, Mailchimp User, Cooby Read, Cooby Edit
    - Save
  - Add to public group
    - Navigate to [Public Groups](https://nec.lightning.force.com/lightning/setup/PublicGroups/home) and then Files access
    - Add new user by clicking `Edit`, next to `Search`, choose `Users`, find user and move to right pane
    - Save
  - Add user to dashboard filters
    - For all dashboards which are in use with a User filter: (at time of writing: [My Team's Student Quotas, Funnels, and Cleanliness](https://nec.lightning.force.com/lightning/r/Dashboard/01Z9J0000005FVrUAM/view) [Follow Ups Management](https://nec.lightning.force.com/lightning/r/Dashboard/01Z3W000000H9e9UAC/view) and [Tasks Management](https://nec.lightning.force.com/lightning/r/Dashboard/01Z3W000000HBXoUAO/view))
    - Open the dashboard
    - Click `Edit`
    - Click the pen icon on the User filter and click `Add Filter Value`
    - Add new User and Apply
    - Reorder
    - Update, Save, Done
  - Create Salesforce inbound email address
    - Navigate to [Email Services page](https://nec.lightning.force.com/lightning/setup/EmailToApexFunction/home)
    - Click `Inbound Email Handler` and `New Email Address`
    - Data entry
      - `Email Address Name` First name
      - `Email address` First name all lowercase
      - `Active` checked
      - `Context User` The user’s name
      - `Accept Email From` remove anything inside
      - Save
    - Locate the new generated email and keep for later
  - Create incoming email channel
    - Navigate to [Channels](https://nec.lightning.force.com/lightning/o/Channel__c/home)
    - Clone an existing email channel record – e.g. Sascha’s email address
    - Data entry
      - Channel Name: [First name]’s email address
      - Identifier: [User’s email address from **step 1** in _Azure Configuration_]
      - Save
    - Change record owner to new User

## Exchange Configuration | Add new user to group, create contact for redirect address, set up email redirect

- First, log onto Microsoft as administrator or an account with the privileges to create users
- Add new user to group
  - Navigate to [Groups page](https://admin.exchange.microsoft.com/#/contacts)
  - Open `Mail-enabled security`
  - Open `NEC Salesforce`
  - On right pane, click `Members` and `View all and manage members`
  - Click `Add members`
  - Add email from **step 1** of _Azure Configuration_
- Create contact for redirect address
  - Navigate to [Contacts page](https://admin.exchange.microsoft.com/#/contacts)
  - Select `Add a mail contact`
  - Data entry
    - `Display Name` [First name]’s Salesforce Redirect (e.g., Sascha’s Salesforce Redirect)
    - `Alias` [First name]
    - `External email address` generated email from **step 5.6** of Salesforce Configuration.
    - Next and Save
- Set up email redirect
  - Navigate to [Rules page](https://admin.exchange.microsoft.com/#/transportrules)
  - Duplicate existing enabled rule
  - Data entry
    - `Name` [First name]’s Mail Redirect to Salesforce Production
    - `Apply this rule if` The recipient is ‘[User’s email address from **step 1** in _Azure Configuration_]’
    - `Do the following` Set the message header ‘toSalesforceRedirectingInbox’ to the value ‘[User’s email address from **step 1** in _Azure Configuration_]’
    - `And` Redirect the message to ‘salesforcenec@new-european-college.com’ and ‘[User’s email address from **step 1** in _Azure Configuration_]’ and ‘[the email address created in **step 2** in _Exchange Configuration_]’
    - Click `Make copy`
    - Click `Refresh`
    - Enable the rule

**Setting up the signature is also part of this process. Have the new employee read the documentation on that subject and set up their signature accordingly by themselves.**
