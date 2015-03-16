# 0. Before you start #
  * Ensure you clear the datastore by starting the development server with option `--clear_datastore`.
  * Ensure you open a new browser instance.
  * Ensure that you have at least the following browsers available for testing:
    * Internet Explorer 8+
    * Firefox 3+
    * Google Crome 2+
    * Safari 7+
# 1. Home page #
Access http://localhost:8080

_Expected:_ Page with NoteSafe information is displayed. `Notes` button is displayed in right-top corner.
## 1.1. Authentication ##
Click `Notes` button.

_Expected:_ Developer sign in prompt is displayed.

Select `Logout`.

_Expected:_ Home page is displayed again.

Select `Notes`.

_Expected:_ Developer sign in prompt is displayed.

Select `Login`.

_Expected:_ Terms and Conditions are displayed.

## 1.2. Terms and Conditions ##
Select `Home`.

_Expected:_ Home page is displayed.

Select Notes

_Expected:_ Terms and Conditions are displayed.

Select Accept

_Expected:_ Notes page with no notes is displayed.

Select Home

_Expected:_ Home page

## 1.3 Notes ##
Select Notes

_Expected:_ Notes page with no notes is displayed.

## 1.4. Add new note ##
Click `Add`.

_Expected:_ New note page is displayed.<br>
<i>Expected:</i> The title of the page should be <code>New note</code>.<br>
<i>Expected:</i> The <code>Save</code> button should be underlined in red.<br>
<i>Expected:</i> The <code>Encrypted text</code> area should be empty.<br>
<br>
Click <code>Save</code>.<br>
<br>
<i>Expected:</i> General error message should be displayed indicating that there are multiple errors.<br>
<i>Expected:</i> Error message should be displayed for the name field indicating that the name is mandatory.<br>
<i>Expected:</i> Error message should be displayed for the password field indicating that the password is mandatory.<br>
<i>Expected:</i> Error message should be displayed for the confirm password field indicating that the confirm password is mandatory.<br>
<i>Expected:</i> Warning message should be displayed for the clear text field that the clear text is empty.<br>
<br>
Click on the cross of the general validation message.<br>
<br>
<i>Expected:</i> All validation messages should be cleared.<br>
<br>
Set the focus to the name field.<br>
<br>
<i>Expected:</i> Information message with maximum length should appear under the name field and stay there.<br>
<br>
Enter <code>TestTestTestTestTest1</code> as name and wait a few seconds.<br>
<i>Expected:</i> Error message should be displayed indicating that the name can't longer than 20 characters.<br>
<br>
Enter <code>Text 1</code> as name.<br>

<i>Expected:</i> Information message with maximum length should appear under the name field and stay there.<br>
<br>
Select Save<br>
<br>
<i>Expected:</i> No validation error or warning should be displayed for the name field but all other validation messages should be displayed as before.<br>
<br>
Click on the cross of the general validation message.<br>
<br>
<i>Expected:</i> All validation messages should be cleared.<br>
<br>
Enter <code>notsafe</code> as password and wait for a few seconds.<br>
<br>
<i>Expected:</i> Error message should be displayed indicating that the password is not safe.<br>
<br>
Enter <code>NotSafe!</code> and wait for a few seconds.<br>
<br>
<i>Expected:</i> Warning message should be displayed indicating that the password is not safe.<br>
<br>
Enter <code>NowWeAreTalking!!!</code> and wait for a few seconds.<br>
<br>
<i>Expected:</i> No validation message should be displayed.<br>
<br>
Focus on the confirmation password and wait for a few seconds.<br>
<br>
<i>Expected:</i> Error message should be displayed indicating that the confirmation password doesn't match the password.<br>
<br>
Enter <code>NotSafe!</code> and wait for a few seconds.<br>
<br>
<i>Expected:</i> Error message should be displayed indicating that the confirmation password doesn't match the password.<br>
<br>
Enter <code>NowWeAreTalking!!!</code> and wait for a few seconds.<br>
<br>
<i>Expected:</i> No validation messages should be displayed.<br />
<i>Expected:</i> The password fields should be hidden.<br />
<i>Expected:</i> The <code>Master password cached.</code> should appear.<br />
<i>Expected:</i> A warning message should appear at the top indicating that all unsaved data will be cleared in 30 seconds. Please note that the timeout is set to 30 seconds only in development. It is several minutes in the production environment.<br />
<i>Expected:</i> An Ajax message is sent to the server with the encrypted key (see <code>Technical information</code> section).<br>
<br>
Wait for 30 seconds.<br>
<br>
<i>Expected:</i> Warning message should be displayed that all unsaved sensitive data has been cleared.<br />
<i>Expected:</i> The bar stating that the master password is cached should disappear.<br />
<i>Expected:</i> The password field should appear.<br />
<i>Expected:</i> The <code>Clear text</code> field should be read-only and contain a message stating that it will update automatically once the correct password has been entered.<br>
<br>
Click <code>Save</code>.<br>
<br>
<i>Expected:</i> An error message should appear stating that the password can't be empty.<br>
<br>
Enter <code>NowWe</code> as password and wait several seconds.<br>
<br>
<i>Expected:</i> An error message should appear that the password is not correct.<br>
<br>
Click <code>Save</code>.<br>
<br>
<i>Expected:</i> An error message should appear that the password is not correct.<br>
<br>
Enter <code>NowWeAreTalking!!!</code> as password and wait for a few seconds.<br>
<br>
<i>Expected:</i> No validation messages should be displayed.<br />
<i>Expected:</i> The password fields should be hidden.<br />
<i>Expected:</i> The <code>Master password cached.</code> should appear.<br />
<i>Expected:</i> A warning message should appear at the top indicating that all unsaved data will be cleared in 30 seconds. Please note that the timeout is set to 30 seconds only in development.<br />
<i>Expected:</i> The <code>Clear text</code> field should be in edit mode, i.e. show the <code>Read</code> button and and a text area. The message should disappear from the text area and it should be editable.<br>
<br>
Click <code>Save</code>.<br>
<br>
<i>Expected:</i> A general warning message at the top should appear stating that there are warnings.<br />
<i>Expected:</i> A warning message should appear near <code>Clear text</code> stating that the text is empty.<br>
<br>
Click on the cross of the general warning message.<br>
<br>
<i>Expected:</i> The general warning message should disappear.<br>
<br>
Click <code>Save</code>.<br>
<br>
<i>Expected:</i> A general warning message at the top should appear stating that there are warnings.<br />
<i>Expected:</i> A warning message should appear near <code>Clear text</code> stating that the text is empty.<br>
<br>
Click <code>Save</code> again.<br>
<br>
<i>Expected:</i> An information message should appear that the note has been added.<br />
<i>Expected:</i> The <code>Encrypted text</code> should get updated.<br />
<i>Expected:</i> An Ajax message (see <code>Technical information</code> section) should be sent to the server with the encrypted text.<br />
<i>Expected:</i> The <code>Clear text</code> should in read mode, i.e. show the <code>Edit</code> button and no text area.<br />
<i>Expected:</i> The note title updates to <code>Test 1</code>.<br>
<br>
Click <code>Notes</code>.<br>
<br>
<i>Expected:</i> One note called <code>Test 1</code> should be listed.<br>
<br>
Click <code>Add</code> and enter <code>Test 2</code> as name.<br>
<br>
<i>Expected:</i> The <code>Clear text</code> area should be in edit mode and empty (assuming that the password is still cached).<br />
<i>Expected:</i> The <code>Encrypted text</code> area should show message indicating that it will be updated after clear text has been entered.<br>
<br>
Click into the <code>Clear text</code> area.<br>
<br>
<i>Expected:</i> An information message should appear that the clear text should be max. 10240 characters long.<br>
<br>
Enter <code>Test tex</code> as <code>Clear text</code> and wait a few seconds.<br>
<br>
<i>Expected:</i> A warning message should appear indicating that all unsaved sensitive data will be cleared in 30 seconds and a count down should begin.<br />
<i>Expected:</i> The <code>Encrypted text</code> area should show the encrypted text.<br>
<br>
Add a <code>t</code> to the clear text  and wait a few seconds.<br>
<br>
<i>Expected:</i> The count down should be reset.<br />
<i>Expected:</i> The <code>Encrypted text</code> area should update with the new encrypted text.<br />
<i>Expected:</i> The <code>Save</code> button should show no underline.<br>
<br>
Click <code>Save</code> and wait for 30 seconds.<br>
<br>
<i>Expected:</i> An information message should appear that the note has been added.<br />
<i>Expected:</i> The <code>Encrypted text</code> should get updated.<br />
<i>Expected:</i> An Ajax message (see <code>Technical information</code> section) should be sent to the server with the encrypted text.<br />
<i>Expected:</i> The <code>Clear text</code> should in read mode, i.e. show the <code>Edit</code> button and no text area.<br />
<i>Expected:</i> The <code>Clear text</code> should show a message indicating that it will update automatically once the correct password has been entered. It should not show <code>Test text</code>
<i>Expected:</i> The note title updates to <code>Test 2</code>.<br>
<br>
Enter <code>NowWeAreTalking!!!</code> as password and wait for a few seconds.<br>
<br>
<i>Expected:</i> The <code>Clear text</code> field should show <code>Test text</code>.<br />
<i>Expected:</i> The <code>Clear text</code> field should in read mode, i.e. show the <code>Edit</code> button and no text area.<br>
<br>
Click <code>Notes</code>.<br>
<br>
<i>Expected:</i> Two notes called <code>Test 1</code> and <code>Test 2</code> should be listed.<br>
<br>
Select <code>Test 1</code>.<br>
<br>
