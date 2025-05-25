# **Title:** My Vacation Planner

The purpose of this application is to serve as a lightweight option to help you organize and plan your trips without worrying about forgetting important details.
With this application, you may:
- **Plan your vacations** by setting a title, hotel name, and start & end dates through a user-friendly interface.  
- **Add excursions** that automatically validate against your vacation dates so you never book things outside your travel window.
- **Stay on schedule** with exact alarms that notify you when each vacation or excursion is starting or ending.
- **Share your itinerary** in one tap via email, SMS, or any app, complete with a neatly formatted list of all related excursions.
- **Manage your plans** easily: edit or delete vacations and excursions, with safeguards to prevent accidentally losing important information.
- **NEW** Quickly search for trips by title or hotel using an intuitive search bar.
- **NEW** Delete excursions with a swipe gesture, complete with an Undo option for safety.

## APK & Android Version

- **Built with:** Android Studio 2024.3.1 Patch 2
- **compileSdkVersion:** 35
- **minSdkVersion:** 26
- **targetSdkVersion:** 35
- This application is deployed to Android API 26 and higher, so it requires Android versions 8.0+.

## Usage

1. **Launch the App**
    - On install or launch, you’ll land on the **Vacations** list.
    - The ActionBar title reads **My Vacations**, and the FAB at bottom-right is labeled **Add Vacation** (`+`).

2. **Add a New Vacation**
    1. Tap the **Add Vacation** FAB (`+`).
    2. In the **Add Vacation** screen:
        - **Title**: Enter your vacation name (e.g. “Beach Trip”).
        - **Hotel**: Enter accommodation name.
        - **Dates**: Tap the date fields to pop up a **DatePicker** and pick the start and end dates for the vacation.
        - **Enable Alerts**: This box is checked by default, but you may also disable it to not receive alerts.
    3. Tap **Save**.
        - **Format validation**: Dates use the picker so they’re always `MM/dd/yyyy`.
        - **Range check**: Picker ensures Start ≤ End.
    4. You’ll be returned to the Vacations list, where your new item appears.

3. **Edit a Vacation**
    1. Tap any vacation card to open **Vacation Details**.
    2. Buttons available: **Share Vacation**, **View Excursions**, **Edit Vacation**, **Delete Vacation**.
    3. **Edit Vacation**: Opens the same form as before, titled “Edit Vacation,” pre-populated with the selected vacation details. Tap **Save** to apply any changes.

4. **Manage Excursions**
    1. From **Vacation Details**, tap **View Excursions**.
    2. The **Excursions** list for that vacation appears. The FAB is labeled **Add Excursion**.
    3. **Add Excursion**: Tap the FAB, enter **Title** and pick **Date**. The date picker enforces the within-vacation range validation. Tap **Save**.
    4. **Edit/Delete Excursion**: Tap an item to open **Excursion Details**, then **Edit** or **Delete**.

5. **Share Vacation Details**
    1. In **Vacation Details**, tap **Share Vacation**.
    2. Android’s share sheet appears where you can choose Email, SMS, Clipboard, etc.
    3. The message body is auto-populated with:
       ```text
       Vacation: [Title]
       Hotel:    [Hotel]
       Dates:    [MM/dd/yyyy – MM/dd/yyyy]
       Excursions:
         1. [Excursion Title] on [MM/dd/yyyy]
         2. …
       ```

6. **Delete a Vacation**
   1. **Delete Vacation**:
       - If excursions exist, you’ll see:
      >    “Cannot delete this vacation – you must first delete all excursions.”
       - If no excursions remain, you’ll get a confirmation dialog before final deletion.

7. **Alerts & Notifications**
    - When saving with alerts enabled, two exact alarms are scheduled (start & end) for vacations, and one alarm for the scheduled date for each excursion.
    - At the scheduled time you’ll see a system notification:
        - “\<Title\> is starting today!”
        - “\<Title\> has ended today.”

8. **Navigation**
    - Every screen shows an Up-arrow in the ActionBar to navigate back.
    - Android’s Back button also steps you back through the flow.

9. **Filter Vacations**
    - In the My Vacations screen, tap the search icon in the action bar up top.
    - Begin typing to filter vacations by **title** or **hotel name**.
    - The list updates live, and search **is not** case-sensitive.
    - Tap the "X" icon to clear the search and view all vacations again.

10. **Swipe-to-Delete Excursions**
    - In any Excursion List, swipe left on an excursion card to delete it **instantly**.
    - A Snackbar will appear at the bottom with an **Undo** option.
        - Tap **Undo** within a few seconds to restore the deleted excursion.
        - If not undone, the deletion is **permanent**.