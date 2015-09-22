**NOTE - You will need QVSource 1.5.6.3 or later to use this sample.**

This example QlikView load script illustrates how to use the FollowerIds and Post_FollowerIds_Info tables of the Twitter Connector (and Friend equivalents) in conjunction with the UserLookupById table to build up a collection of all the followers and friends of a particular account over a number of reloads (if required).

This is necessary because the Twitter API only allows enough API calls to retrieve 15x5000=75,000 follower IDs per 15 minute window.

This script uses a new feature in QVSource which is under development and explained in more detail here:
http://wiki.qvsource.com/Getting-Follow-Up-Information-Based-On-A-Previous-Tables-Response.ashx

Further work would be needed to allow this to capture *new* followers/friends. Perhaps a stamp could be used and all followers/friends could be completely re-captured every X days.

To use this sample you will also need to edit the vWorkingFolder and vUserName parameters on the Setup tab.

Change Log
==========
1.0.4 - 22/10/14
----------------
* IMPORTANT: You will now need QVSource version 1.5.6.3 or later to work with this application.
* Fixed bug with friemds code using incorrect cursor (from followers).			
* Created _ThisReload and _NextReload versions of vNextAllowed[Follower|Friend]IDsRequest, vNextCursor[Follower|Friend]IDs variables and all are now shown in UI.
* Changed required version check to 1.5.6.3.

1.0.3 - 12/05/14
----------------
* UserLookupById now uses a processParamsSync file (rather than concatenating all user ids into the URL which resulted in URLs too long to be processed).
* Now requires QVSource 1.5.3.3 or later.

1.0.2 - 21/02/14
----------------
* Now only loads distinct ids.
* Reviewed and tested against QVSource 1.4.9.6 (requires this version or later).
* Now includes following (friends) functionality also.
* Now includes User lookup.

1.0.1 - 04/12/13
----------------
* Added badge.

1.0.0 - 04/09/13
----------------
* Initial version.