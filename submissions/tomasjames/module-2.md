### Nature of the Incident
On 20th August 2017, a user began to merge open pull requests in to the the `open-training` repository. This user was not affiliated with GitHub beyond undertaking the Campus Expert training, and did not communicate their intended actions to the author of the pull requests either. This resulted in a number of incomplete exercises being merged to the `master` branch - in a few instances these merge events were destructive (i.e. removing content from exercise descriptions).

### Moderation Action
The moderators took 3 steps to rectify the incident:  

- Revert the merge  
    This resulted in the erroneous merge events being rolled back to a last stable state, a prime example of the importance of version control for document versioning. Crucially, GitHub staff reverted the images with an individual commit and then merged these commits using a rebase. The primary objective behind this methodlogy was so that users undertaking the training (i.e. users of the repo) would not have to resync their forks.  
  
  
- Changed the merge permissions  
    This meant that now only people affiliated with GitHub can review and merge pull requests to the `master` branch. Prior to this, any repo user would merge pull requests however this resulted in the aforementioned incident and therefore required amendment. This did, however, remove the ability (at least for now) for Campus Expert trainees to train themselves in reviewing and merging pull requests.  
    

- Removed the user responsible  
    In all likelihood the user's intentions were good, and the actions were the result of a misunderstanding. It did however highlight the capability that a misunderstanding has, and so further work was required to ensure that users cannot alter (for worse) the content of the repo.  

The moderators also updated the repo with a new issue outlining the event, and the steps they took to rectify the incident. This meant that all users of the repo were a) aware of what happened and what was done to fix it but also b) the importance of proper merge etiquette.

### Outcome
The outcome has been overwhelmingly positive, and the repo and community has been improved as a result. Users are now more aware of the power that a pull request, and subsequent merge, has.

### What could be different?
The nature of the incident happening in the first place implies that better protections could have been implemented from the beginning. However, this incident was the first of its type and was therefore difficult to pre-empt. The relevant restorative actions were taken to rectify it immediately, therefore reducing disruption. This aspect was handled perfectly.

It is important however to highlight the need for updated documentation on how, when and why a pull request should be merged. Conversely this documentation should outline when not to merge a pull request. However the moderators are aware of the need for this and have themselves stated that it is coming.

Furthermore the removal of the user that merged the pull requests is potentially a harsh. From a community member's standpoint it could imply that any mistakes of this nature are punishable by removal from the training programme. Whilst this is likely not the case, some further justification on exactly why the user was removed (and whether this measure is temporary or permanent) could have been added to the issue outlining the incident.