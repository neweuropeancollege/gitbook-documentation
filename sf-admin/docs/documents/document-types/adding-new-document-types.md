# Adding new document types

# How to Add New Application Document Types

## Step 1: Navigate to Setup
1. Log in to Salesforce.
2. Click on the gear icon in the upper right corner and select `Setup`.

## Step 2: Access the Object Manager
1. In the Setup menu, go to `Object Manager`.
2. Select the `Application Document` object.

## Step 3: Modify the Type Field
1. In the `Application Document` object, go to `Fields & Relationships`.
2. Click on the `Type` field.
3. Note that the `Type` field is a picklist controlled by a global value set. Click on `View Value Set` to open the global value set.

## Step 4: Add a New Picklist Value
1. In the global value set, click `New` to add a new type.
2. Enter the exact name of the new type in the text box.
3. Check the option to reorder alphabetically if available, then click `Save`.
4. If the reorder option is not available, click `Reorder` and select `Sort Alphabetically`. Click `Save`.

## Step 5: Update Record Types in Application Document Object
1. Return to the `Application Document` object in the `Object Manager`.
2. Navigate to `Record Types`.
3. Open the record type corresponding to the type of document you are adding (e.g., `Identification`, `Language Proficiency`).
4. Go to the `Picklists Available for Editing` section.
5. Click `Edit` next to the `Type` field.
6. Move the new type from the left box to the right box, then click `Save`.

## Step 6: Configure Field Dependencies in Required Application Document Object
1. In the `Object Manager`, select the `Required Application Document` object.
2. Go to `Fields & Relationships`.
3. Click on `Field Dependencies` in the top right corner.
4. Select the `Type` and `Specific Type` fields to manage dependent picklist values.
5. Include the new type under the appropriate columns according to the record type specified earlier.
6. Save your changes.

## Conclusion
After completing the steps above, you will have successfully added a new application document type. Ensure all configurations align with the new type, and verify functionality through testing.
