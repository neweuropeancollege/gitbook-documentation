# Naming Structure

In using the Exclusive Campaign Tracker model, we must select and adhere to a strict naming structure of the automations themselves in order to enable maintainability, flexibility, and upgradeability. This article outlines this naming structure and should be kept up-to-date as the structure evolves.

{% hint style="info" %}
Keep in mind, altering the naming structure should be done with caution, as it may have unintended outcomes with existing campaign recipients that are already in queue.
{% endhint %}

The structure is constructed of the following elements

* Marketing stage
* Source
* Sales stage
* Institution destination

... and formatted as so

`Marketing stage` - `Source` `Sales stage` `Instituion destination`

### Elements Descriptions

#### Marketing stage

<table><thead><tr><th width="135">Options</th><th>Significance</th></tr></thead><tbody><tr><td>Lead</td><td>a student inquirer that isn't a qualified applicant yet<br>a prospective partner that hasn't signed yet</td></tr><tr><td>Applicant</td><td>a student inquirer that has earned a qualified status</td></tr><tr><td>Partner</td><td>an educational agency that has signed a partnership contract with our organization</td></tr></tbody></table>

Applied => Lead - Direct Applicant NEC

App - Eval Docs + App - Interviewing => Qualified Lead - Direct Applicant NEC (3 weeks)

App - Requesting WUAS Decision - Closed Won => Applicant - Direct Applicant/Principal NEC (open)
