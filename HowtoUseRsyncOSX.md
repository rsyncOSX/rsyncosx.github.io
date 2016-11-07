<h3>How to use RsyncOSX</h3>

This page is how to use RsyncOSX. It starts with the main view and is a walkthrough of adding a configuration and how to use it.<br />
<br />
<b>This page is under construction. </b>It will be under construction for some time. All screens in RsyncOSX is shown below. Information about each screen is "work in progress".<br />
<br />
<h3>
Some notes about rsync and RsyncOSX</h3>
<br />
RsyncOSX is a GUI for the rsync command-line tool. The main uses are:<br />
<ul>
<li>backup (and restore) local files on Mac to remote servers connected to Internet or local network</li>
<ul>
<li>the above is why I wrote RsyncOSX to use myself</li>
</ul>
<li>backup (and restore) local files on Mac to local storage (attached disks)</li>
<ul>
<li>if this is&nbsp;<i>the only use</i>&nbsp;there might be&nbsp;<i>other tools</i>&nbsp;more useful than RsyncOSX</li>
</ul>
</ul>
<div>
<i>source</i> : the local volume to be copied&nbsp;</div>
<div>
<i>destination</i> : the remote location where source files and catalogs are copied</div>
<div>
<br /></div>
<div>
<b>Warning</b>: default parameters for rsync is to&nbsp;<b>synchronize</b>&nbsp;the <b>source</b> and <b>destination</b>. Doing a "restore" will&nbsp;<b>delete</b>&nbsp;all files in the source which are not in the destination. The main objective to RsyncOSX is to keep any&nbsp;<b>source</b>&nbsp;directory and&nbsp;<b>destination </b>(backup)&nbsp;directory&nbsp;<b>in sync</b>. When a source directory is backed up, the destination is 100% in sync with source in the moment the backup task is completed. There are&nbsp;<b>no revisions</b>&nbsp;of files in the backup in&nbsp;<b>default RsyncOSX</b>. Old files in the backup are either replaced with new ones or deleted if so is true in source.<br />
<br />
What about<b> revisions and deleted</b> files? In the "parameters to rsync" there is presented a solution to save changed and deleted files in a selected backup location.<br />
<br />
<br />
<h3>
Where do RsyncOSX save configuration files?</h3>
<div>
<br /></div>
<div>
<br /></div>
<div>
RsyncOSX configuration file, log file, scheduled tasks file and userconfiguration are plain XML-files (<a href="https://en.wikipedia.org/wiki/Property_list" target="_blank">property list files</a>). &nbsp;Configuration files (backup and restore task configurations and schedule data) are saved in:<br />
<br />
<div>
<ul>
<li><code>~/Documents/Rsync/</code><code>MacID</code><code>/configRsync.plist</code></li>
<ul>
<li><code><b>~/</b></code>&nbsp;is user home directory</li>
<li><code>MacID</code>&nbsp;is the Mac Serial Number and is automatically&nbsp;created by RsyncOSX</li>
</ul>
</ul>
<div>
When profiles are used:</div>
<ul>
<li><code>~/Documents/Rsync/</code><code>MacID</code><code>/profile/configRsync.plist</code></li>
<ul>
<li>if&nbsp;<code>profile</code>&nbsp;are used</li>
</ul>
</ul>
<div>
</div>
</div>
</div>
<br />
<h4>
</h4>
<h4>
</h4>
<h4>
</h4>
<h4>
</h4>
<h4>
</h4>
<h4>
</h4>
<h4>
</h4>
<h4>
</h4>
<h4>
Why use RsyncOSX?</h4>
</div>
<div>
<br /></div>
<div>
There is only one simple answer to that and the answer is&nbsp;<b><a href="https://en.wikipedia.org/wiki/Rsync" target="_blank">rsync</a></b>. Rsync is a rock solid, well proven, secure, fast, reliable and wide accessibility across platforms command line tool. RsyncOSX is just a GUI for executing &nbsp;rsync commands. Rsync is a command line tool with tons of parameters. Choosing the right parameter and to get the predicted result from rsync might be a challenge. RsyncOSX does the job for you. RsyncOSX also stores configurations in profiles and makes it easy to use many configurations.</div>
<div>
<br /></div>
<div>
The following features are implemented in RsyncOSX:<br />
<ul>
<li>execute&nbsp;<b>single</b>&nbsp;tasks</li>
<ul>
<li>estimation run is required before the real task is executed</li>
<li>by pressing the Execute button&nbsp;<b>after</b>&nbsp;the estimation progress indicator has stopped executes the real task</li>
<li>if another row (task) is selected after estimation is done a new estimation run is&nbsp;required</li>
</ul>
<li>execute&nbsp;<b>batch</b>&nbsp;tasks</li>
<ul>
<li>batch tasks are executed automatically until all completed</li>
<li>if you want tasks to be executed in one go mark them for batch</li>
</ul>
<li>adding&nbsp;<b>new tasks</b>&nbsp; either by drag and drop (for local volumes) or by GUI</li>
<li><b>user configuration</b>&nbsp;</li>
<ul>
<li>the user can select another version of rsync</li>
</ul>
<li><b>abort</b>&nbsp;single- and batch tasks</li>
<li><b>rsync parameters</b></li>
<ul>
<li>the user can&nbsp;add parameters to rsync</li>
</ul>
<li><b>enable</b>&nbsp;saving backups of changed or deleted files (in rsync parameters)</li>
<ul></ul>
<li><b>delete</b>&nbsp;and&nbsp;<b>edit</b>&nbsp;configurations</li>
<li>store configurations in <b>profiles</b></li>
<li><b>copy of single files or volumes</b>&nbsp;from remote storage</li>
<li><b>scheduling of tasks</b></li>
<li><b>detailed logging</b></li>
<ul>
<li>switch on/off</li>
</ul>
</ul>
<div>
<br /></div>
</div>
<div>
<h4>
</h4>
<h4>
</h4>
<h4>
</h4>
<h4>
</h4>
<h4>
</h4>
<h4>
</h4>
<h4>
</h4>
<h4>
RsyncOSX is not suitable to all users</h4>
<br />
The primary objective for me to write and use RsyncOSX is for storing backup of local volumes to&nbsp;<i>low cost remote server</i>&nbsp;and assist me to keep my&nbsp;<i>two Macbook desktops in sync</i>. The remote servers might be running either Linux, Solaris, OpenSolaris, FreeBSD or other BSD based server OS. To set up and use all the functionality of RsyncOSX require some computer skills as login to a remote server (from terminal) and set up private/public key based ssh password-less logins. Some basic understanding of the command-line tool rsync is also recommended.<br />
<br />
Any user just looking for an easy to use backup tool is advised to use other and probably more suitable tools than RsyncOSX. To fully understand and use RsyncOSX I recommend the following:<br />
<ul>
<li>you have some understanding of the command-line tool rsync</li>
<li>you have some knowledge about running either Linux, Solaris, OpenSolaris, FreeBSD or other BSD based server OS</li>
<li>you are able to&nbsp;<a href="https://rsyncosx.blogspot.no/2016/03/remote-servers-ssh-and-passwordless.html" target="_blank">setup a ssh password-less login</a>&nbsp;between the Macbook desktop and the remote server</li>
</ul>
<div>
<br /></div>
</div>
<h3>
</h3>
<h3>
</h3>
<h3>
</h3>
<h3>
</h3>
<h3>
</h3>
<h3>
</h3>
<h3>
</h3>
<h3>
</h3>
<h3>
</h3>
<h3>
The main opening view
</h3>
<div>
<br /></div>
<div>
The main opening screen is below. All configurations to execute are listed in table. From this screen are all actions regarding configurations performed. All actions are presented below. The documentation is presented in sequence of how to add new configurations into RsyncOSX.<br />
<br />
There are two labels on top of table : Profile and Double click: YES. Configurations can be saved in user selected profiles. The profile in use is shown in label. Double click:YES (or NO) either allow or dont allow executing single tasks by double click on row. Disable/enable in Configuration.<br />
<br />
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="https://3.bp.blogspot.com/-9e82zjXi_q4/WBQnQ425ysI/AAAAAAAAL7E/t--57C8ZzPMIgcRn02YTnrWx8jAv35oXgCLcB/s1600/Screen%2BShot%2B2016-10-29%2Bat%2B06.35.31.png" imageanchor="1" style="margin-left: auto; margin-right: auto;"><img border="0" height="336" src="https://3.bp.blogspot.com/-9e82zjXi_q4/WBQnQ425ysI/AAAAAAAAL7E/t--57C8ZzPMIgcRn02YTnrWx8jAv35oXgCLcB/s640/Screen%2BShot%2B2016-10-29%2Bat%2B06.35.31.png" width="640" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;">The main view of RsyncOSX</td></tr>
</tbody></table>
RsyncOSX uses profiles. If not used all configurations are saved in the default profile. Which profile in use is labeled on left top of table.<br />
<br />
<div class="separator" style="clear: both; text-align: center;">
</div>
In the profiles menu there are two options:<br />
<ul>
<li>new profile (name of new profile must be set in "New profile name:")</li>
<li>delete profile</li>
</ul>
Selecting the "Default" button selects the default profile. &nbsp;Double click on a profile name selects the profile.<br />
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="https://1.bp.blogspot.com/-ZI3Wb7tQd5o/WBQnQ-ibGHI/AAAAAAAAL7A/XG1Du4gcLi8Pi3dlZNzzSCJOEFoMiZ_KQCLcB/s1600/Screen%2BShot%2B2016-10-29%2Bat%2B06.35.46.png" imageanchor="1" style="margin-left: auto; margin-right: auto;"><img border="0" height="336" src="https://1.bp.blogspot.com/-ZI3Wb7tQd5o/WBQnQ-ibGHI/AAAAAAAAL7A/XG1Du4gcLi8Pi3dlZNzzSCJOEFoMiZ_KQCLcB/s640/Screen%2BShot%2B2016-10-29%2Bat%2B06.35.46.png" width="640" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;">Selecting profile</td></tr>
</tbody></table>
</div>
<br />
<div>
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
</div>
<h3>
Add configuration</h3>
<div>
<br />
Adding configurations is easy. One configuration require as minimum only "Local catalog" and "Remote catalog". And they cannot be equal. After entering information about a configuration selecting the Add button adds it to RsyncOSX. Continue adding new configurations until completed and configurations are saved to permanent store when choosing another tab (as Execute or other).&nbsp;</div>
<div>
<br /></div>
<div>
Select "Local catalog" either by "drag and drop", by enter text directly or by GUI (press the folder icon). &nbsp;For "Remote catalogs" only drag and drop or GUI for local volumes. For remote server catalogs enter by text only.<br />
<br />
If "Single file" is ticked on, RsyncOSX adds backup og single file only. No restore part is added, use Copy files for search and restore.</div>
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><img border="0" height="336" src="https://1.bp.blogspot.com/-0qO_rSeuBKA/WAmhh79NoVI/AAAAAAAAL5E/eIDabOVSaWUSDf7GnvcgB79fdNpNNksZwCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B08.52.01.png" style="margin-left: auto; margin-right: auto;" width="640" /></td></tr>
<tr><td class="tr-caption" style="text-align: center;">The Add view - selecting Folder icon presents a GUI for local catalogs</td></tr>
</tbody></table>
<div class="separator" style="clear: both; text-align: center;">
<a href="https://1.bp.blogspot.com/-0qO_rSeuBKA/WAmhh79NoVI/AAAAAAAAL5E/eIDabOVSaWUSDf7GnvcgB79fdNpNNksZwCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B08.52.01.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"></a><br /></div>
<a href="https://1.bp.blogspot.com/-0qO_rSeuBKA/WAmhh79NoVI/AAAAAAAAL5E/eIDabOVSaWUSDf7GnvcgB79fdNpNNksZwCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B08.52.01.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"></a><br />
<br />
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="https://3.bp.blogspot.com/-c2w2h5xX9ag/WAmhh0ImdxI/AAAAAAAAL5I/oMN2h-FxbQU6cQbQVj3O4VERrnnpfqeLgCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B08.52.31.png" imageanchor="1" style="margin-left: auto; margin-right: auto;"><img border="0" height="366" src="https://3.bp.blogspot.com/-c2w2h5xX9ag/WAmhh0ImdxI/AAAAAAAAL5I/oMN2h-FxbQU6cQbQVj3O4VERrnnpfqeLgCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B08.52.31.png" width="640" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;">Adding local catalogs by GUI</td></tr>
</tbody></table>
The screen below is all information about my configuration for a virtual FreeBSD instance running on my Macbook Pro.<br />
<br />
<ul>
<li><b>Local catalog</b>: - path for my RsyncOSX src (as an example)</li>
<li><b>Remote catalog</b>: - ~/src/RsyncOSX is the home catalog for user thomas (the ~ is expanded as the home catalog with full path by the remote operating system), the remote catalog might also be added by full path (/home/thomas/src/RsyncOSX)</li>
<li><b>Remote username</b>: - thomas</li>
<li><b>Remote server</b>: - either name or IP-adress, 127.0.0.1 is the IP-adress for the virtual FreeBSD instance</li>
<li><b>ssh port</b>: - if ssh communicates through other than standard port 22 it must be set here. In Virtualbox I have set up a port forwarding through port 3022 -&gt; Virtualbox port 22.</li>
<li><b>rsync daemon</b>: - setting this puts a double colon :: in address parameter to rsync. It forces rsync to use the rsync daemon remote which takes some more setup. I am not using it myself.</li>
</ul>
<br />
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="https://2.bp.blogspot.com/-gi2FYh-_LBY/WAmhiEf5ZrI/AAAAAAAAL5M/q592yuxR-QIxu9c2ES9RctnCHQClwlowgCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B09.16.23.png" imageanchor="1" style="margin-left: auto; margin-right: auto;"><img border="0" height="336" src="https://2.bp.blogspot.com/-gi2FYh-_LBY/WAmhiEf5ZrI/AAAAAAAAL5M/q592yuxR-QIxu9c2ES9RctnCHQClwlowgCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B09.16.23.png" width="640" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;">Information about configuration for a Virtual machine</td></tr>
</tbody></table>
Select the Add button when finish and configuration are added to RsyncOSX. Any changes to added configurations from the Execute screen.<br />
<br />
RsyncOSX adds the "/" character to both local and remote volume.<br />
<br />
Both the "backup" part and "restore" part is added when saving new configurations.<br />
<div class="separator" style="clear: both; text-align: center;">
<a href="https://4.bp.blogspot.com/-EeBIBxlJE0s/WAmhiWeeGDI/AAAAAAAAL5Q/__WJIgbs2bYVcqqLby79vgC4niFvkGy2gCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B09.16.46.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="336" src="https://4.bp.blogspot.com/-EeBIBxlJE0s/WAmhiWeeGDI/AAAAAAAAL5Q/__WJIgbs2bYVcqqLby79vgC4niFvkGy2gCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B09.16.46.png" width="640" /></a></div>
<h3>
Executing added configuration</h3>
<div>
<div>
<br />
In main view (which is the opening view) tasks can be executed as&nbsp;<b>single</b>- and/or&nbsp;<b>batch</b>&nbsp;tasks. Execute single tasks requires selecting the Execute button twice : one for estimation run and the second for executing the real task. For Batch execution, see below.</div>
<br />
There are three options for editing after selecting a task in row :<br />
<ul>
<li><b>Edit task</b></li>
<li><b>Parameters</b> (to rsync)</li>
<li><b>Delete task</b></li>
</ul>
<div>
For Parameters see below. After selecting a row choosing one of the above pops up a new view according to selection. Selecting Edit task for editing basic information about task. Selecting Delete task deletes the selected row (task).<br />
<br />
There are some status fields in the view :<br />
<ul>
<li><b>Estimate</b> - text is either "Estimate" or "Execute" - valid for single tasks only</li>
<ul>
<li>"Estimate" - selecting Execute does a --dry-run</li>
<li>"Execute" - selecting Execute does the real job (backup or restore)</li>
</ul>
<li><b>Scheduled job</b> - a progress bar shows when a scheduled job is executing</li>
<li><b>Information</b> - if checked a drop down view is presented after each run - valid for single tasks only</li>
<li><b>Estimating</b> - a progress bar shows when a --dry-run (or estimate) is executing&nbsp;</li>
</ul>
</div>
</div>
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="https://2.bp.blogspot.com/-PslDJNhqRdc/WAmhihscUDI/AAAAAAAAL5U/CXCxco5tfPQNYCWgZUQfp5odxVLGe_wpQCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B09.17.14.png" imageanchor="1" style="margin-left: auto; margin-right: auto;"><img border="0" height="336" src="https://2.bp.blogspot.com/-PslDJNhqRdc/WAmhihscUDI/AAAAAAAAL5U/CXCxco5tfPQNYCWgZUQfp5odxVLGe_wpQCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B09.17.14.png" width="640" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;">Selecting a configuration for actions&nbsp;</td></tr>
</tbody></table>
<h4>
<span style="font-weight: normal;">Both "backup" and "restore" path is set when saving configuration.</span><br />
</h4>
<div>
<span style="font-weight: normal;"><br /></span></div>
<h4>
</h4>
<h4>
Parameters to rsync</h4>
<div>
<br />
<a href="https://rsyncosx.blogspot.no/2016/04/rsync-parameters.html" target="_blank">Here</a>&nbsp;are details about parameters to rsync. The parameters in picture below instructs rsync to save changed files in catalog ../backup (relativ to destination catalog) and suffix the backup file with timestamps. The above is enabled or disabled by select or deselect the "backup" button. The user might change the backup catalog. Default is ../backup.</div>
<div>
<br /></div>
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="https://1.bp.blogspot.com/-mFUGksTyUAA/WAmhilxPsnI/AAAAAAAAL5Y/s9lXbqBNRnkCTS1WPyjHmafFJAyNYF8qACLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B09.17.32.png" imageanchor="1" style="margin-left: auto; margin-right: auto;"><img border="0" height="336" src="https://1.bp.blogspot.com/-mFUGksTyUAA/WAmhilxPsnI/AAAAAAAAL5Y/s9lXbqBNRnkCTS1WPyjHmafFJAyNYF8qACLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B09.17.32.png" width="640" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;">Either set preselected parameters or your own parameters</td></tr>
</tbody></table>
If the backup directory is not created rsync automatically creates it. The ../backup is a catalog relative to the destination catalog. The user can specify any catalog as backup catalog.<br />
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="https://1.bp.blogspot.com/-rAioO-XrAm4/WAmhjC1UD6I/AAAAAAAAL5c/hx8vydOMgTY1dppLCd2SCQyspBca7HgsgCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B09.18.09.png" imageanchor="1" style="margin-left: auto; margin-right: auto;"><img border="0" height="336" src="https://1.bp.blogspot.com/-rAioO-XrAm4/WAmhjC1UD6I/AAAAAAAAL5c/hx8vydOMgTY1dppLCd2SCQyspBca7HgsgCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B09.18.09.png" width="640" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;">After selecting the "backup" parameter three new parameters are added to rsync task</td></tr>
</tbody></table>
The screen below is a listing of some of files moved to the backup directory and renamed before new files are transferred from source to destination.<br />
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="https://2.bp.blogspot.com/-3PGnAGBlXlU/WAmhlm9ispI/AAAAAAAAL6Y/6tGAo1yevaM9uGCgMUGSCq3-J-0xyZqYACEw/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B10.29.41.png" imageanchor="1" style="margin-left: auto; margin-right: auto;"><img border="0" height="448" src="https://2.bp.blogspot.com/-3PGnAGBlXlU/WAmhlm9ispI/AAAAAAAAL6Y/6tGAo1yevaM9uGCgMUGSCq3-J-0xyZqYACEw/s640/Screen%2BShot%2B2016-10-20%2Bat%2B10.29.41.png" width="640" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;">Changed files are moved to backup catalog and renamed with date and time as suffix</td></tr>
</tbody></table>
<h3>
</h3>
<h3>
</h3>
<h3>
User configuration</h3>
<div>
<br />
There are only a few parameters to choose in user configuration. The two most important are :</div>
<div>
<ul>
<li>another version of rsync</li>
<li>detailed logging on or off</li>
<li>allow double click to execute single tasks</li>
</ul>
<div class="separator" style="clear: both; text-align: center;">
</div>
<div class="separator" style="clear: both; text-align: center;">
<a href="https://2.bp.blogspot.com/-h7b8RpZ9lc4/WBQqLxmCMyI/AAAAAAAAL7U/mhef5atFxcITHPg0Z1OnNmU7bmXuzfbigCLcB/s1600/Screen%2BShot%2B2016-10-29%2Bat%2B06.48.11.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="336" src="https://2.bp.blogspot.com/-h7b8RpZ9lc4/WBQqLxmCMyI/AAAAAAAAL7U/mhef5atFxcITHPg0Z1OnNmU7bmXuzfbigCLcB/s640/Screen%2BShot%2B2016-10-29%2Bat%2B06.48.11.png" width="640" /></a></div>
<div>
<br /></div>
</div>
<div class="separator" style="clear: both; text-align: center;">
</div>
<h3>
</h3>
<h3>
Execute single tasks</h3>
<div>
<br />
Execute single tasks is a <b>two step</b> operation, one for <b>estimation</b> (dry-run) and one for the <b>real task</b>. If the Information button is ticked on a popup view is automatically presented after both tasks.<br />
<br />
Single tasks can be executed either by selecting the Execute button or (if enabled) double click on the selected task. Both methods is a two step operation.<br />
<div class="separator" style="clear: both; text-align: center;">
</div>
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
<a href="https://2.bp.blogspot.com/-LTOFBw_xhOE/WAmhj5hGMVI/AAAAAAAAL6Y/xXWeO9_fF9QKvWEcTfntmIbYRS_ONI-bwCEw/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B09.22.32.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="336" src="https://2.bp.blogspot.com/-LTOFBw_xhOE/WAmhj5hGMVI/AAAAAAAAL6Y/xXWeO9_fF9QKvWEcTfntmIbYRS_ONI-bwCEw/s640/Screen%2BShot%2B2016-10-20%2Bat%2B09.22.32.png" width="640" /></a></div>
<div>
The process info is updated when either a estimation task is executing or if a scheduled task is executing. There are five numbers in bottom page. Only version 3.x counts the number of remote directories. The numbers are files to be transferred and remote numbers.&nbsp;</div>
<h4>
</h4>
<h4>
</h4>
<h4>
Estimating</h4>
<div>
<br />
The actual rsync command to be executed is shown below right corner in view. It is only the estimation command which is shown. You might copy the command and paste it into a terminal for execution. You have to delete the --dry-run parameter to execute the real task.</div>
<div>
<br /></div>
<div>
If you dont want to do a two step task chose Execute batch task (se below).</div>
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="https://3.bp.blogspot.com/-IpJOm7XOh5U/WAmhjNPsE2I/AAAAAAAAL5k/8-9ECrKp_hsopC-a1ToXQhhpGHS28QpIwCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B09.21.54.png" imageanchor="1" style="margin-left: auto; margin-right: auto;"><img border="0" height="336" src="https://3.bp.blogspot.com/-IpJOm7XOh5U/WAmhjNPsE2I/AAAAAAAAL5k/8-9ECrKp_hsopC-a1ToXQhhpGHS28QpIwCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B09.21.54.png" width="640" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;">Result of estimation run</td></tr>
</tbody></table>
Next task shows what the next task is. It shows three status : Estimate, Execute or Abort. If Abort is pressed any executing task is aborted.<br />
<h4>
</h4>
<h4>
</h4>
<h4>
Executing</h4>
<div>
<br />
After estimate run is completed and result is checked, a real run is executed by selecting the Execute button again. If you select another row after estimation a new estimation run must be completed.&nbsp;</div>
<div class="separator" style="clear: both; text-align: center;">
<a href="https://4.bp.blogspot.com/-UxuIHn1pinM/WAmhjiJG6vI/AAAAAAAAL5o/285zrZW9RW0G_5Pg8odaL6ekIiKLeavNQCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B09.22.14.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="336" src="https://4.bp.blogspot.com/-UxuIHn1pinM/WAmhjiJG6vI/AAAAAAAAL5o/285zrZW9RW0G_5Pg8odaL6ekIiKLeavNQCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B09.22.14.png" width="640" /></a></div>
<br />
<h3>
</h3>
<h3>
Execute batch tasks&nbsp;</h3>
<div>
<br />
Only backup tasks can be set for batch. All tasks marked for batch is presented in screen for batchtask. Choosing Execute executes all tasks in one go, both the estimation run and real run. The screen is updated as the process of execution is going forward.</div>
<div class="separator" style="clear: both; text-align: center;">
<a href="https://3.bp.blogspot.com/-BUlrOHueogY/WAmhjz0rQPI/AAAAAAAAL5w/yD21ybRDyGEoeY5ygEmV9f6H2etj5OqbwCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B09.22.39.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="336" src="https://3.bp.blogspot.com/-BUlrOHueogY/WAmhjz0rQPI/AAAAAAAAL5w/yD21ybRDyGEoeY5ygEmV9f6H2etj5OqbwCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B09.22.39.png" width="640" /></a></div>
<h3>
</h3>
<h3>
Schedule task</h3>
<div>
<div>
<br />
By selecting a row and choose schedule applies a scheduled backup to a task.</div>
<div class="separator" style="clear: both; text-align: center;">
</div>
<div>
<div class="separator" style="clear: both; text-align: center;">
</div>
There are four(three) choices for schedules :<br />
<ul>
<li><b>Once</b></li>
<ul>
<li>is executed once at date and time given</li>
</ul>
<li><b>Daily</b></li>
<ul>
<li>is executed every 24-hour and stops at given date and time</li>
<li>first backup in 24-hour</li>
</ul>
<li><b>Weekly</b></li>
<ul>
<li>as for daily, but every 7 days</li>
</ul>
<li><b>Details</b></li>
<ul>
<li>stop or delete scheduled tasks</li>
</ul>
</ul>
</div>
</div>
<div class="separator" style="clear: both; text-align: center;">
<a href="https://3.bp.blogspot.com/-pJYPTGFb4vY/WAmhkSC5fhI/AAAAAAAAL50/Wn0PKn2m2bsi2t0aKIiD_K8M0z92BPZrQCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B09.23.45.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="336" src="https://3.bp.blogspot.com/-pJYPTGFb4vY/WAmhkSC5fhI/AAAAAAAAL50/Wn0PKn2m2bsi2t0aKIiD_K8M0z92BPZrQCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B09.23.45.png" width="640" /></a></div>
<br />
<div class="separator" style="clear: both; text-align: center;">
<a href="https://4.bp.blogspot.com/-qPey9NI5Wnk/WAmhkX5ckcI/AAAAAAAAL54/kwZaACuWAgsNq6cuWOB7m8WTMaVO4-cRQCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B09.24.05.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="336" src="https://4.bp.blogspot.com/-qPey9NI5Wnk/WAmhkX5ckcI/AAAAAAAAL54/kwZaACuWAgsNq6cuWOB7m8WTMaVO4-cRQCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B09.24.05.png" width="640" /></a></div>
<br />
<div class="separator" style="clear: both; text-align: center;">
<a href="https://2.bp.blogspot.com/-3W2nahamOLs/WAmhkY4mz8I/AAAAAAAAL58/gx3onllf-2siECKAcKu4aXzCbHAZhhPSgCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B09.24.13.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="336" src="https://2.bp.blogspot.com/-3W2nahamOLs/WAmhkY4mz8I/AAAAAAAAL58/gx3onllf-2siECKAcKu4aXzCbHAZhhPSgCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B09.24.13.png" width="640" /></a></div>
<h4>
&nbsp;Stopping a scheduled task</h4>
<div class="separator" style="clear: both; text-align: center;">
<a href="https://2.bp.blogspot.com/-3CKoR1TM0Yg/WAmhkxhhCYI/AAAAAAAAL6A/PK3o5esw6Kkf8ChF2NXY6DeuyoMy3qaowCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B09.24.25.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="336" src="https://2.bp.blogspot.com/-3CKoR1TM0Yg/WAmhkxhhCYI/AAAAAAAAL6A/PK3o5esw6Kkf8ChF2NXY6DeuyoMy3qaowCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B09.24.25.png" width="640" /></a></div>
<h3>
</h3>
<h3>
Copy single files or catalogs</h3>
<div>
<br />
Copy file and volume enables the user to select single file or catalogs for restore to a given local storage. The source for copy is the selected row in Execute view. Pressing select starts the job to collect data about which files are stored on remote server.</div>
<div class="separator" style="clear: both; text-align: center;">
<a href="https://1.bp.blogspot.com/-MmuYXOeNzXI/WAmhlPLl-_I/AAAAAAAAL6I/ekY2PnOzXygOnt6d2RTA7vXaDF7s5QulgCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B10.17.44.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="336" src="https://1.bp.blogspot.com/-MmuYXOeNzXI/WAmhlPLl-_I/AAAAAAAAL6I/ekY2PnOzXygOnt6d2RTA7vXaDF7s5QulgCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B10.17.44.png" width="640" /></a></div>
<br />
<div class="separator" style="clear: both; text-align: center;">
<a href="https://4.bp.blogspot.com/-fa_pRhIrlm8/WAmhlBXviEI/AAAAAAAAL6E/LNDfv5YUhMEjjrKihppR38TrjBxy4OXmQCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B10.17.53.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="336" src="https://4.bp.blogspot.com/-fa_pRhIrlm8/WAmhlBXviEI/AAAAAAAAL6E/LNDfv5YUhMEjjrKihppR38TrjBxy4OXmQCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B10.17.53.png" width="640" /></a></div>
<br />
<div class="separator" style="clear: both; text-align: center;">
<a href="https://1.bp.blogspot.com/-ULO1IkYC_rc/WAmhlpXWq0I/AAAAAAAAL6Q/SjCXaRf_Io4YW_O_hl1LDK4Zvl99ZPBPgCLcB/s1600/Screen%2BShot%2B2016-10-20%2Bat%2B10.17.59.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="336" src="https://1.bp.blogspot.com/-ULO1IkYC_rc/WAmhlpXWq0I/AAAAAAAAL6Q/SjCXaRf_Io4YW_O_hl1LDK4Zvl99ZPBPgCLcB/s640/Screen%2BShot%2B2016-10-20%2Bat%2B10.17.59.png" width="640" /></a></div>
<br />
<div class="separator" style="clear: both; text-align: center;">
</div>
<br />
<style type="text/css">
p.p1 {margin: 0.0px 0.0px 0.0px 0.0px; font: 11.0px Menlo; color: #000000; background-color: #ffffff}
span.s1 {font-variant-ligatures: no-common-ligatures}
</style>