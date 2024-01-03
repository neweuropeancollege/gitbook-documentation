# Finding Records in Lookup Fields

This is a lookup field


Sometimes we need to find the right record and select it in a lookup field. But if there are many records with the same name, it can be frustratingly difficult to select the correct record. This can happen in cases where common names make it difficult to select the correct account (e.g., multiple accounts named "Singh Administrative Account").

Here are two ways to work around this issue, of which the **first method is strongly recommended**.

## Making the record recently viewed

1. **Navigate to the Target Record**
    - The target record is the record you're trying to select in the lookup field.
    - You can navigate to the record by
        - searching with the global search feature at the top of the screen, utilizing unique identifiers such as the first name or email address of the student.
        - navigating to the record by another way you know you can use to access it, e.g. they are in your list of tasks or opportunities.

2. **Opening the Record**
   - Once you have located the correct record, open the record. This action is critical as it marks the record as a recently viewed item in Salesforce.

That's it! Once the record is marked as recently viewed, **it will appear as the first option in a lookup field**.

3. **Navigating Back**
   - Go back to your lookup field and select the first option. Rest assured it will be the correct one.

{% hint style="info" %}
Please note! The recently viewed record will only really be the one you recently viewed as long as you did not 'view' that record while a lookup field was already in 'edit mode'.
{% endhint %}

## Temporarily altering the record's name

1. **Navigate to the Target Record**
    - The target record is the record you're trying to select in the lookup field.
    - You can navigate to the record by
        - searching with the global search feature at the top of the screen, utilizing unique identifiers such as the first name or email address of the student.
        - navigating to the record by another way you know you can use to access it, e.g. they are in your list of tasks or opportunities.

2. **Opening the Record and Editing its Name**
    - Once you have located the correct record, open and edit its name to something distinct, taking note of the initial name.

3. **Navigating Back**
    - Go back to your lookup field and search for the corresponding record's new, temporary name.

4. **Change the Record's Name Back**
    - Edit the record's name back to what it was before.

{% hint style="info" %}
As you can see, this method is cumbersome as it requires an additional step. Use it if you feel comfortable with it.
{% endhint %}