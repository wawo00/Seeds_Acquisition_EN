Guides of Syncing the Seeds to Ad Media
=======================================

Now you can sync your High Ad-Value Audiences data (hereafter called
"Seeds") to the specified ad media for user-targeted promotion.
Currently, only Facebook ad accounts are supported as sync targets. The
Seeds can be synced to specified Facebook ad accounts as "Ad Audience".

Facebook Client OAuth
---------------------

First of all, you need to authorize "Client OAuth" of your developer
account to UPLTV. When using this feature at the first time, you will
find an "Authorize Facebook Account" button, just click the button to
start authorizing.

Step1 - Provide the **App ID** and **App Secret** of an App in your Facebook develoer account.
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Go to Facebook for Developers (https://developers.facebook.com/apps/),
select any App and click into its configuration page.

Click into the "Settings - Basics" page in the left menu, you can easily
find App ID and App Secret of this App in the top position.

.. figure:: ../img/en_1.png
   :scale: 70 %
   :alt: picture 3

Step2 - Set the link provided by UPLTV to **"Vaild OAuth Redirect URIs"**.
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Copy the callback link provided by UPLTV, then go back to the same page
on Facebook for Developers in the previous step. Click into the
"Facebook Login - Settings" page in the left menu, find the input box of
"Vaild OAuth Redirect URIs", just paste the link copied from UPLTV into
the box and save it.

.. figure:: ../img/en_2.png
   :scale: 70 %
   :alt: picture 3


Step3 - Click the "Jump to Facebook & Complete the authorization" button, complete the authorization by following the instructions on the landing page.
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

When the authorization is completed, UPLTV will automatically obtain the
Facebook Ad accounts that allowed to be accessed by the authorized
developer account, and UPLTV will update the Ad accounts list regularly.
Also, you can replace the authorized account with a new one, but please
be cautions that all existing sync rules will be removed immediately.
The authorized token may be invaild in some special circumstances. When
it happens, you will find an "Re-authenticate" button. Please follow the
guide to re-authorize.

Create and edit sync rules
--------------------------

Once you have completed account authorization process, you are ready to
create a custom sync rule. You can sync the Seeds from any of your
multiple Apps to any number of authorized Facebook Ad accounts.

Some notes about sync mechanism
-------------------------------

#. Synced Seeds data will be grouped into different "Facebook Ad
   audiences" by Apps, the rule of naming the "audiences" :
   **#pid\ data\ accountID**  pid : App ID in UPLTV  data : date of last
   sync as format "yyyymmdd"  accountID : Facebook Ad account ID
#. UPLTV will update the "audiences" every day by adding new Seeds &
   removing discared Seeds.
#. The sync program starts at 1 o'clock (PST) every day, and will finish
   in 30 minutes.