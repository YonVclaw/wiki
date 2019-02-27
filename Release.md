Here you can read on how cScripts is being deployed. 

# Release procedure
1. Draft a new github release with proper version number.
   - ****Note:*** On the draft Travis will automaticly create release builds and upload them with proper name.*
1. Write and add the changelog based on created commits and pull requests. There are two categories General and Loadout. Put the changes done in the correct category. <br>Format are as follows: <br>```* TOPIC: Change i made (#PR) (**NAME**)```
     - **Topic***: ADDED, CHANGED, FIXED<br>
     **#PR**: Pull request number exsample: `#652`<br>
     **NAME:** Person that made the changed.<br>
     **Exsample:**<br>
     ADDED: Check for rifles in the inventory (#10) **Tully.B**
1. Create patch release