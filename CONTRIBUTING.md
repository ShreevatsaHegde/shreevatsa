
<!DOCTYPE html>
<html><head>
<meta charset="UTF-8"/>
<meta id="schoolViewport" name="viewport" content="width=device-width, initial-scale=0.5, maximum-scale=1.0, minimum-scale=0.5"/><title>Zoho Creator&nbsp;-&nbsp;Schooling</title>
<link id="schoolRelShortcut" rel="SHORTCUT ICON" href="https://css.zohostatic.in/creator/11657/images/database_fav_small.ico" />

<style media="screen">
.school-body-init{
overflow: hidden;
} 
.school_loader_container
{
background: #f5f5f5;
position: fixed;
width: 100%;
height: 100%;
top: 0;
bottom: 0px;
right: 0;
left: 0;
z-index:99999;
}
.school_preview_loader
{
background: #ffffff;
}
.school_initial_loader
{
width: 100%;
position: absolute;
top:50%;
left:50%;
margin-top: -30px;
text-align: center;
-moz-transform: translate(-50%,-50%);
-ms-transform: translate(-50%,-50%);
-webkit-transform: translate(-50%,-50%);
transform: translate(-50%,-50%);
}
.school_initial_loader span
{
font-size: 22px;
font-family: arial;
letter-spacing: 1px;
display: block;
padding: 0 20px;
text-transform: uppercase;
color: #000;
line-height: 30px;
}
.school_initial_loader .school_initial_progess
{
width: 350px;
height: 2px;
border-radius: 2px;
margin-top: 30px;
background: #e0e0e0;
left:50%;
-moz-transform: translatex(-50%);
-ms-transform: translatex(-50%);
-webkit-transform: translatex(-50%);
transform: translatex(-50%);
position: relative;
}
.school_initial_loader .school_initial_progess .school_on_loading
{
content: '';
position: absolute;
width: 0%;
background: #5e6163;
height: 100%;
left:0;
-webkit-animation: progress 200ms forwards linear , progress_forward 300ms 200ms forwards linear;
-moz-animation: progress 200ms forwards linear , progress_forward 300ms 200ms forwards linear;
-ms-animation: progress 200ms forwards linear , progress_forward 300ms 200ms forwards linear;
animation: progress 200ms forwards linear, progress_forward 300ms 200ms forwards linear;
}
@-webkit-keyframes progress_forward {
0%
{
width: 50%;
}
100%
{
width: 95%;
}
}
@-moz-keyframes progress_forward {
0%
{
width: 50%;
}
100%
{
width: 95%;
}
}
@-ms-keyframes progress progress_forward {
0%
{
width: 50%;
}
100%
{
width: 95%;
}
}
@keyframes progress_forward {
0%
{
width: 50%;
}
100%
{
width: 95%;
}
}
@-webkit-keyframes progress {
0%
{
width: 0%;
}
100%
{
width: 50%;
}
}
@-moz-keyframes progress {
0%
{
width: 0%;
}
100%
{
width: 50%;
}
}
@-ms-keyframes progress {
0%
{
width: 0%;
}
100%
{
width: 50%;
}
}
@keyframes progress {
0%
{
width: 0%;
}
100%
{
width: 50%;
}
}
.school_initial_loader .school_initial_progess + .school_initial_progess
{
display: none;
margin-top: -2px;
z-index: 1;
}
.school_initial_loader.complete .school_initial_progess + .school_initial_progess
{
display: block;
}
.school_initial_loader.complete .school_initial_progess + .school_initial_progess .school_on_loading
{
-webkit-animation: progress_complete 0ms forwards linear;
-moz-animation: progress_complete 0ms forwards linear;
-ms-animation: progress_complete 0ms forwards linear;
animation: progress_complete 0ms forwards linear;
}
@-webkit-keyframes progress_complete {
0%
{
width: 80%;
}
100%
{
width: 100%;
}
}
@-moz-keyframes progress_complete {
0%
{
width: 80%;
}
100%
{
width: 100%;
}
}
@-ms-keyframes progress_complete {
0%
{
width: 80%;
}
100%
{
width: 100%;
}
}
@keyframes progress_complete {
0%
{
width: 80%;
}
100%
{
width: 100%;
}
}
</style> 
<script>function setCookie(keyName,value,expiryTime,domain,path)
{
var expdate=new Date();
if(expiryTime)
{
expdate.setTime(expdate.getTime()+(expiryTime*24*3600*1000));
}
else
{
expdate.setTime(expdate.getTime()+(365*24*3600*1000));
}
var cookieStr = keyName+ "=" +escape(value)+ ";expires="+expdate.toGMTString()+";";//No I18N
if(domain)
{
cookieStr = cookieStr + "domain="+escape(domain)+";";//No I18N
}
if(path)
{
cookieStr = cookieStr + "path="+escape(path)+";";//No I18N
}
document.cookie=cookieStr;
}
function loadCSS(url){
var css = document.createElement("link");
css.type = 'text/css';
css.rel = 'stylesheet';
css.href = url;
document.getElementsByTagName("head")[0].appendChild(css);
}
function getCookie(keyName){
if (document.cookie.length>0){
cookieBegin=document.cookie.indexOf(keyName + "="); //No I18N
if (cookieBegin!=-1){
cookieBegin=cookieBegin + keyName.length+1;
cookieEnd=document.cookie.indexOf(";",cookieBegin); //No I18N
if (cookieEnd==-1){ 
cookieEnd=document.cookie.length;
}
return unescape(document.cookie.substring(cookieBegin,cookieEnd));
}
}
return ""; //No I18N
}
function isNull(value){
if(!value || value == "undefined" || typeof(value) == "undefined" || value == "NULL" || value == "null" || value.length == 0 || value == ""){
return true;
}
return false;
}
function loadFiles(itemsToLoad) { //don't remove this method from this file
var promises = itemsToLoad.map(function(url) {
return loadFile(url);
});
return Promise.all(promises);    
}
function loadFile(url, defer){ //don't remove this method from this file
return new Promise(function(resolve, reject) {
if(typeof(getConfig) != "undefined" && !getConfig().useCompression && !defer){
return resolve();
}
var tag, type;
var match = url.match(/\.([^.]+)$/);
if (match) {
type = match[1];
}
if (!type) {
type = "js";  //No I18N
}
var filename = url.split("/");
filename = filename[filename.length - 1];
var fileid = filename.split(".")[0];
if (type === 'css'){
tag = document.createElement("link");
tag.type = 'text/css';
tag.rel = 'stylesheet';
tag.href = url;
tag.id = fileid+"_"+type;
}
else if (type === "js")
{
tag = document.createElement("script");
tag.type = 'text/javascript';
tag.defer = true;
tag.src = url;
tag.id = fileid+"_"+type;
}
if (tag) {
tag.onload = function() {resolve(url)};
tag.onerror = function() {reject(url)};
document.getElementsByTagName("head")[0].appendChild(tag);
}		
});
}
/****
* Temporary workaround. When 'catch' and 'delete' (which are js keywords) are included in js files, an parse error will be thrown by current compressor while minifying the script.
* This workaround can be removed once a new compressor is updated.
*/
function catchPromiseChain(promise, handler){
if(handler === undefined){
handler = function(e){
Console.log(e);
}
}
return promise.catch(handler);
}
function deleteCache_CacheStorage(cache,key){
return cache.delete(key);
}
function deleteCachePool_CacheStorage(poolName){
return caches.delete(poolName);
}
function deleteObject_IndexedDB(objStore, key){
return objStore.delete(key);
}</script>
<script type="text/javascript">var schoolNewLivePublicDomain = "creatorl.zohopublic.in";
/**this method is used to get csrf cookie since getCookie will not be loaded at this point**/
function getCSRF(){
var cookies = document.cookie.split(";");
var csrfName = "schoolcpn"; 
for(var i = 0; i<cookies.length; ++i){
cookie = cookies[i].trim();
if(cookie.indexOf(csrfName + '=') === 0){
return cookie.substring(csrfName.length+1);
}
}
}
var clouddocurl = "https://gadgets.zoho.in/CloudPicker?attachLimit=1&sources=gdrive,zohodocs,skydrive,dropbox,box&originUrl=https://" + location.hostname + "&zservice=schoolreator&check=true&frameorigin=https\x3A\x2F\x2Fapp.zohocreator.in";	
var fileCloudUrl = "https://gadgets.zoho.in/CloudPicker?school_PARAMS=&attachLimit=1&frameorigin=https\x3A\x2F\x2Fapp.zohocreator.in&serURL=https://" + location.hostname + "/shreegh44/schooling/gadgetcallback";	
var fileCloudUrlFormperma = "https://gadgets.zoho.in/CloudPicker?school_PARAMS=&attachLimit=1&frameorigin=https\x3A\x2F\x2Fapp.zohocreator.in&serURL=https://" + location.hostname + "/shreegh44/schooling/gadgetcallback/null";
;	
var schoolGlobal = new function(){

this.contextName = "app"; 
this.csrfTokenName = "schoolcpn";	
this.csrfToken = getCSRF();

this.scopeName = "shreegh44";
this.scopeZuid = "60000893504";	
this.scopeEmail = "";	

this.loginName = "shreegh44";
this.loginEmail = "shreegh44@gmail.com";	
this.loginZuid = "60000893605";
this.loginUserId = "12595000000002001";

this.appLinkName = "schooling";
this.appDisplayName = "Schooling";
this.applicationId = "12595000000003003";	
this.uiDateFormate = "DD-MMM-YYYY";  	
this.serverPrefix = window.location.protocol + "//" + window.location.host;
this.oldliveserver = "creator.zoho.in";	
this.appurl = this.serverPrefix + "/" +  this.scopeName + "/" + this.appLinkName + "/";

this.buildSetup = "in";

this.appbuilderserverprefix = "https://creator.zoho.in"

this.isPreviewAction = false;	
this.previewAppurl = this.serverPrefix + "/preview/" +  this.scopeName + "/" + this.appLinkName + "/";	
this.servicename = "zoho";
this.sheet2AppDomain = "https://sheet2app.zoho.in"; 
this.useSheet2App = false;

this.schoolChatEnabled 			= false; 	
this.schoolPreSalesEnabled		= false;  
this.isChatRestrictionEnabled = false;	
this.isNewExport = false;	
this.isMobileLayout	= false;	
this.schoolUpgradeChatEnabled = false; 	
this.appDirectionMeta = {
isRTL			 : false ,
sliderDirection  : false ? "left" : "right" , // No I18N
scrollerPosition : false ? "left" : "right" ,  // No I18N
tooltipPosition  : false ? "left" : "auto"	// No I18N
}
}</script>
<script type="text/javascript">var i18n =
{

"pleasewait":"Please wait", 
"ok" : "Okay", 
"yes" : "Yes", 
"no" : "No", 
"chatsupportweekends": "Our Chat Support is only available Monday-Friday. You can leave us an email to support&#x40;zohocreator.com and we will get back to you soon.", 
"chatsupportrestrictionmsg" : "All our reps are busy. You can leave us an email to support&#x40;zohocreator.com and we will get back to you soon.", 
"replace":"Replace", 
"submit":"Submit", 
"cancel":"Cancel", 
"loading":"Loading", 
"done":"Done", 
"openbuilder":"Open Builder",
"underconstruction":"Under Construction",
"back": "Back", 
"emailmessage": "Enter email id", 
"choice1": "Choice 1", 
"choice2": "Choice 2", 
"choice3": "Choice 3", 
"singlelinemessage": "Enter single line value", 
"nummessage": "Enter value", 
"selectmessage": "Select value", 
"linkname": "Link Name", 
"taptoselect": "Tap to Select", 
"uploadgallery": "Upload from gallery", 
"takepicture": "Take a picture", 
"subformmessage": "Tap to add Records", 
"taptosign": "Tap to Sign", 
/* Geo Location keys */
"geoheaderform" : "You're required to share your location to use this form.", 
"geoheaderduplicate" : "You're required to share your location to duplicate this record.", 
"geoheaderbulkedit" : "You're required to share your location to edit these records.", 
"geoheaderimportdata" : "You''re required to share your location to import data.", 
"geoheaderfailure" : "You''re required to share your location to continue.", 
"geodesc" : "If you click Allow, your location will be shared with this application''s owner when you submit this form.", 
"geodescfailure" : "You have blocked your location from Zoho Creator. Please allow to continue. Learn more.", 
"alreadyfileuploaded" : "You have already uploaded a file.", 
"errormsg":"Error occurred. Please refresh the page and try again later.",
"unconfirmeduserpublish": "The email address of the application owner is not yet verified. Please verify the email address to publish this component.", 
"publicaccessupgrademsg1":"Trial and Free edition users are not allowed to publish.", 
"publicaccessupgrademsg2":"Please contact &lt;a href&#x3d;&#x27;mailto&#x3a;support&#x40;zohocreator.com&#x27;&gt;support&#x40;zohocreator.com&lt;&#x2f;a&gt;", 
"publishmaxlimitreachedmsg1":"Maximum number of components allowed to publish for your account has been exceeded. ", 
"publishmaxlimitreachedmsg2":"Please contact &lt;a href&#x3d;&#x27;mailto&#x3a;support&#x40;zohocreator.com&#x27;&gt;support&#x40;zohocreator.com&lt;&#x2f;a&gt;", 
"publishmaxplanmaxlimitreached":"Maximum number of components allowed to publish for your account has been exceeded.", 
"selectOption":"Select",
"lookupaddrestriction":"Sorry, this form cannot be accessed from this portal. Please contact your administrator for further assistance.",
"redirectopaypal":"Redirecting to payment gateway...",
"paypaypaymentcancel":"Payment has been cancelled...",
"paypaypaymentsuccess":"Your payment has been processed successfully",
"invalidentriesfound":"Invalid entries found",
"correctandsubmit":"Please correct and submit again.",
"redirectopaypal":"Redirecting to payment gateway...",
"formlooksactive":"Form looks active",
"fileuploadinprogress":"File upload is in progress, try to submit once all uploads are done.",
"subformrowlimitreachedmsg":"You have reached maximum number of rows. You cannot add further.",
"formlooksactive":"Form looks active",
"nogeolocation":"Geolocation is not supported in this browser.",
"formgeolocationerror":"Geo location is enabled for this form. ",
"formgeolocationdesc":"Allow location access for this page to proceed.",
"geolocbrowsererror":"Try with a different browser   ",
"phonenovalidationerror":"Enter a valid phone number",
"validEmailMsg":"Enter a valid email address for <strong> {0} </strong>",
"validNumberMsg":"Enter a valid number for <strong> {0} </strong>",
"roundDecimalMsg":"Round off the <strong> {0}</strong> field value to {1} decimal places",
"validDateFormat":"Enter a valid date format for <strong> {0} </strong>", 
"mincharacter":"Please enter min. 2 characters", 
"nomatchfound":"No matches found", 
"integrationnomatchfound":"No matches found.", 
"selectplaceholder":"-Select-",
"prefixplaceholder":"None",
"addresssearchmsg":"Search for an address",
"noresultfound":"No results found",
"deleterecord":"Do you really want to delete this record &#x3f;", 
"delfailmsg":"Record&#x28;s&#x29; could not be deleted, since delete validate action failed.", 
"delsuccmsg":"Record&#x28;s&#x29; deleted successfully.", 
"nofldtomatch":"Please select the field(s) to match with existing record(s)",
"plzpastedata":"Please provide input for file content",
"importerror":"Error occurred while uploading the file. Kindly report this problem to support@zohocreator.com",
"nofiletoimport":"Please select a file with data.",
"unsupportedfile":"File format not supported. Please use a .CSV, .TSV, .XLS, .XLSX or .TXT file.",
"emptyfiletoimport":"Please provide a file with data",
"largefiletoimport":"Please provide a file of size less than 5MB",
"uploadmore":"To upload more, contact support@zohocreator.com", 
"importingmsg":"Importing Data ...", 
"selcols4imp":"Please select columns to import", 
"showimperrors":"Show Errors", 
"hideimperrors":"Hide Errors", 
"disperrormsg":"Please choose a Display Field.", 
"dateerrormsg":"Please choose a Start Date.", 
"grperrormsg":"Please choose a field to group report with.", 
"maperrormsg":"Please choose a field to mapping field", 
"unabletodelete1000recs":"Unable to delete more than 1000 records", 
"unabletodup1000recs":"Unable to duplicate more than 1000 records", 
"custActionExecMaxLimit":"Unable to execute this action for more than 1,000 records",    
"duplicaterecords":"Duplicating Records", 
"deleterecords":"Deleting Records", 
"selectrectodup":"Please select at least one record to be duplicated", 
"selectrectodelete":"Please select at least one record to be deleted", 
"showing":"Showing", 
"showsummary":"Show Summary", 
"hidesummary":"Hide Summary", 
"detailsummary":"Summary", 
"of":"of", 
"sum":"Total", 
"max":"Maximum", 
"min":"Minimum", 
"avg":"Average", 
"kanbanothercategory":"You cannot drop here as it is unlisted", 
"kanbannegativeCategory":"You cannot drop here as it is no longer exist", 
"kanbanemptymandatory":"You cannot drop here as this field is mandatory", 
"kanbandefaultlistedcategory":"Drop here to move to {0}", 
"deleteselrecsconf":"Do you really want to delete the selected &#x7b;0&#x7d; records &#x3f;", 
"deleteselrecconf":"Do you really want to delete the selected &#x7b;0&#x7d; record &#x3f;", 
"dupselrecsconf":"Do you really want to duplicate the selected &#x7b;0&#x7d; records &#x3f;", 
"dupselrecconf":"Do you really want to duplicate the selected &#x7b;0&#x7d; record &#x3f;", 
"selectatleastonerectoprintsummary":"You should select atleast one record to print the record summary.", 
"viewinvalidentriesmessage":"Invalid entries found. Please correct and save again.", 
"showatleastacolumn":"Select at least one column to display", 
"listreporthidecolumn":"At least one column needs to be displayed", 
"selectatleastacolumntoimport":"Select at least one column to import", 
"reportregensuccess":"Regeneration has been initiated for this report. This may take a few minutes based on the volume of data.", 
"reportregenfail":"Sorry. We are unable to regenerate the report.", 
"spreadsheetcnfm":"Do you really want to leave this page&#x3f; Unsaved changes will be lost.", 
"custactinfo":"Select at least one record that matches the criteria defined for this custom action", 
"customactionexecution":"Do you want to execute &#x5b;0&#x5d; action for this record&#x3f;", 
"onclickcustomactionmismatch":"The selected record does not match the criteria defined for this custom action", 
"unabletodeletereport":"Unable to delete the Report.", 
"fileuploadsizelimit":"File size must be lesser than 50MB", 
"imagesizelimit":"File size must be lesser than 10MB", 
"selectImageMsg":"Select Image", 
"selectfileMsg":"Select File", 
"localuploadHoverMsg":"Local Computer", 
"linkHoverMsg":"URL", 
"cameraHoverMsg":"Camera", 
"audioHoverMsg":"Microphone", 
"cloudUploadHoverMsg":"Cloud Storage", 
"restoreMsg":"Restore", 
"allowtoaccessmedia" : "Allow to access media&#x21;",
"nomediasupport" : "Your browser does not support media&#x21;",
"nosupportaudio" : "is not supported audio type",
"nosupportvideo" : "is not supported video type",
"uploadaudio": "You may only upload audio up to", 
"uploadvideo": "You may only upload video up to",
"shorteraudio": "long. Try uploading a shorter audio",
"shortervideo": "long. Try uploading a shorter video",
"uploadingvideo": "Uploading video...",
"uploadingaudio": "Uploading audio...",
"filesize": "Your file size exceeds 50MB ",
"filecorrupted" : "The file you're trying to upload is not readable",
"videopermissionline1" : "You're required to enable access to your microphone and camera before making a recording.",
"audiopermissionline1" : "You're required to enable access to your microphone before making a recording.",
"imagepermissionline1" : "You're required to enable access to your camera before capturing an image.",
"imagepermissionline2" : "Click Allow to enable capturing. You may change this setting at any time.",
"permissionline2" : "Click Allow to enable recording. You may change this setting at any time.",
"blockpermissionline1" : "You cannot make a recording from your browser since you have blocked media access for Zoho creator. ",
"blockpermissionline2" : "To continue, please change the permissions settings in your browser.",
"imgblockpermissionline1" : "You cannot capture an image from your browser since you have blocked media access for Zohocreator.   ",
"browsersupportline1" : "Sorry, but your browser doesn't support  media access. ",
"browsersupportline2" : "Please try accessing this application from another browser.",
"nofieldselect":"No fields selected&#x21;&#x21;", 
"updatenofield":"Update record for no fields doesn&#x27;t make sense", 
"norecordselect":"No records selected&#x21;&#x21;", 
"updatenorecord":"Update record for no records doesn&#x27;t make sense", 
"editcontinue":"Are you sure you want to continue&#x3f;", 
"updaterecords":"This will update &#x5b;0&#x5d; selected records", 
"updaterecord":"This will update &#x5b;0&#x5d; selected record", 
"updatevalue":"with the given value.", 
"updatevalues":"with the given values.", 
"vieweditinvalidmsg":"Invalid entries found. Please correct and save again.", 
"emptyreportname":"Report name cannot be empty.", 
"emptyfiltername":"Custom filter&#x27;s name cannot be empty.", 
"reportnameexceedchar":"Report name cannot exceed 50 characters. Provide a different name.", 
"filternameexceedchar":"Custom filter&#x27;s name cannot exceed 50 characters. Provide a different name.", 
"bulkeditselcolumn":"Select the column to edit", 
"either":"either", 
"or":"or", 
"month":"Month", 
"week":"Week", 
"day":"Day", 
"nextmonth":"Next Month",  
"nextweek":"Next Week",  
"nextday":"Next Day",  
"previousmonth":"Previous Month",  
"previousweek":"Previous Week",  
"previousday":"Previous Day", 
"searchlimit":"Field cannot have more than six values in search" , 
"correctvalueforn":"Please enter a valid number for N" , 
"correctvaluetosearch":"Please enter a valid number to search",  
"pdfdisablewarning":"Pdf export is currently not available for reports with multiple search values in a particular field",  
"dropdownselect":"-Select-", 
"otheroption":"Other", 
"delalert":"Alert Message", 
"delrecsuccess":"Deleted the following", 
"delrecord":"record", 
"delrecords":"records", 
"delrecfailure":"Delete validation failed for the following ", 
"delsuccessfully":"successfully.", 
"noreversegeocode":"No address found for this location", 
"rgeocodeservererror":"Internal error occurred. Try after some time.", 
"restrictsearch" : "Search based on this field is no longer supported, click the &#x27;X&#x27; to remove.",
"search" : "Search",
"school.dem.page.openbuilder":"Open Page Builder",
"deprecateBannerHeader" : "Looks like your browser is out of date.",
"deprecateBannerContent" : "To enjoy continued access to Zoho Creator in this browser, please update your browser to the latest version on or before October 31, 2018.",
"deprecateBannerLinkMsg" : "Know more.",
"deprecateBannerUserContent" : "To enjoy continued access to this application in this browser, please update your browser to the latest version on or before October 31, 2018. Contact your administrator for further information.",
"deprecateBannerMobileContent" : "Please update your browser to the latest version on or before October 31, 2018.",
"deprecateBannerMobileUserContent" : "Please update your browser to the latest version on or before October 31, 2018. Contact your administrator for further information.",
"revokingaccess":"Revoking access...", 
"grantingaccess":"Granting access...", 
"school.onboarding.wtlivemodeviewheading":"DATA REPORT", 
"school.onboarding.wtlivemodeviewdesc":"Click here to see all the records you have submitted in your form.", 
"school.onboarding.wtlivemodeaddheading":"WEB FORM", 
"school.onboarding.wtlivemodeadddesc":"Here is where you add data and submit it into your database.", 
"school.onboarding.wtlivemodeeditheading":"EDIT APPLICATION", 
"school.onboarding.wtlivemodeeditdesc":"Click on this icon to customize your application further, and share it with your team.", 
"school.onboarding.wtgotit":"Got it", 
"school.onboarding.stepof":"of", 
"school.onboarding.wtskip":"Skip Tutorial", 
"school.onboarding.wtnext":"Next", 
"school.onboarding.wtheadingapplication":"Here's your Application", 
"school.onboarding.wtdescapplication":"This is what people will see when they're using your application. In the final small section of the tutorial, we'll walk through how your pizza orders get stored. Go ahead and fill out your form a few times.", 
"school.onboarding.wtheadingreports":"Reports", 
"school.onboarding.wtdescreports":"Every time you build a form, Creator automatically makes a <b>Report</b> to view the info you enter in the form. This report is named after our form, but you can always change the name later. <br/><br/>Click on it to see what's inside.", 
"school.onboarding.wtheadingrecords":"Reports and Records", 
"school.onboarding.wtdescrecords":"This report lets workers know who ordered, which pizzas they want, and what table to deliver them to. Each entry in the report is called a <b>Record</b>.", 
"school.onboarding.wtheadingsearch":"Searching", 
"school.onboarding.wtdescsearch":"Reports let you search through and sort your information. You can click on the search icon and fill in details to find the records youre looking for.", 
"school.onboarding.wtheadingfinal":"And that's it!", 
"school.onboarding.wtdescfinal":"Congratulations! You're done.</br></br> If you want to keep working on your application, click on the 'Edit this application' link to return to the form builder screen.</br>For more help, you can always click on the 'Help' link to read our guides, watch our videos, chat with support, or go through this tutorial again.", 
"school.onboarding.wtheadingcreatorbasicsinfo":"Forms and Reports", 
"school.onboarding.wtdesccreatorbasicsinfo":"Now you know the basics of any Creator application. <b>Forms</b> let you collect information, and <b>reports</b> help you use it. In our application the form collects orders, and the report helps our workers serve pizzas.",
"school.live.notification.applysuccessmsg":"has been applied successfully to your account", 
"school.live.notification.successcontactmsg":"Contact <a href=mailto:support@zohocreator.com>support@zohocreator.com</a> for more clarifications",
"school.live.notification.rollbacksuccessmsg":"has been rolled back successfully",
"school.live.notification.rollbackcontactmsg":"If you are facing any issues contact <a href=mailto:support@zohocreator.com>support@zohocreator.com</a>",
"school.builder.accountsetup.enable" : "Enable", 	
"school.builder.accountsetup.disable" : "Disable", 
"school.common.builder.upgrade.validation.enabled" : "The upgraded security framework has been enabled for this application.", 
"school.common.builder.upgrade.validation.enabledmessage" : "Before clicking on <b>Enable for all users</b>, please check for any changes in HTML content in pages along with the reports corresponding to the forms fields listed in", 
"school.common.builder.upgrade.validation.enabledmessage.split" : "Application Validation.", 
"school.common.builder.upgrade.validation.testlater" : "I'll test later", 
"school.common.builder.upgrade.validation.enableforall" : "Enable for all users", 
"school.common.builder.upgrade.validation.enabledadmin" : "The upgraded security framework has been enabled for this application by the application owner.", 
"school.common.builder.upgrade.validation.enabledadminmsg" : "Contact the application owner if you find any changes in this application.", 
"school.common.builder.upgrade.validation.enablepopoup" : "Enabling the upgraded security framework to all users of this application cannot be undone. Are you sure you want to enable it?", 
"school.common.builder.upgrade.validation.enablepopupbutton" : "Enable", 
"school.common.builder.upgrade.validation.enablepopupcancel" : "Cancel", 
"school.common.builder.upgrade.validation.disablepopup" : "The upgraded security framework has been disabled and this application can be validated later from the Updates tab in the Account Setup.", 
"school.common.builder.upgrade.validation.disablepopupold" : "The upgraded security framework has been disabled and this application can be validated later from the Notification icon found at the top-right corner within an application.", 
}</script><script>var jsLocale = "en";	
var useCompression = true;	
var label 			= "11657";									
var staticLabel 	= "schools10549";								
function getConfig()
{
var confprop={"useCompression":true,"cssStaticServer":'css.zohostatic.in',"jsStaticServer":'js.zohostatic.in',"domainVal":'zoho.in',"production":'true',"devSetup":false};  	
return confprop;
}
var jsApacheServer 	= "https://js.zohostatic.in";		
var cssApacheServer = "https://css.zohostatic.in";	</script><script>
function schoolPath(config){
this.initComplete = false;
var _self = this;
this.basePath = { staticCss : config.cssServerPrefix+"/"+config.staticLabel+"/css/",
staticJs : config.jsServerPrefix+"/"+config.staticLabel+"/js/",
appJs : config.jsServerPrefix+"/"+config.buildLabel+"/app/js/",
appCss : config.cssServerPrefix+"/"+config.buildLabel+"/app/css/",
announcementJs : config.jsServerPrefix+"/"+config.buildLabel+"/announcement/js/",
announcementCss : config.cssServerPrefix+"/"+config.buildLabel+"/announcement/css/",
campaignCss : config.cssServerPrefix+"/"+config.buildLabel+"/campaigns/css/",
appbuilderJs : config.jsServerPrefix+"/"+config.buildLabel+"/appbuilder/js/",
appbuilderCss : config.cssServerPrefix+"/"+config.buildLabel+"/appbuilder/css/",
upgradeCss	:	config.cssServerPrefix+"/"+config.buildLabel+"/upgrade/css/",
appeditCss	:	config.cssServerPrefix+"/"+config.buildLabel+"/appedit/css/"
};
this.init = function(){
if(!_self.initComplete){
//1. Init common params
_self.initCommonParams();
//2. Init live specific params
_self.initLiveParams();
//3. Init app specific params 
for(var eachpath in _self.basePath){
var currBasePath = _self.basePath[eachpath];
for(var eachkey in schoolPath[eachpath].leafpaths){
var filename =  schoolPath[eachpath].leafpaths[eachkey];
schoolPath[eachpath][eachkey] = currBasePath + filename;
}
//delete schoolPath[eachpath].paths;
}
_self.initComplete = true;
}
}
this.initCommonParams = function(){
if(config.common){
schoolPath.wmsliteJs	=	config.common.wmsliteJsUrl;
schoolPath.wmsbarJs		=	config.common.wmsBarJsUrl;
schoolPath.wmsbarCss	=	config.common.wmsBarCssUrl;
schoolPath.storeJSUrl	=	config.common.storeJSUrl;
schoolPath.storeCssUrl	=	config.common.storeCssUrl;
}
}
this.initLiveParams	= function(){
if(config.live){
schoolPath.appCss.themeCss			= _self.basePath.appCss + config.live.defaultThemeFileCss;
schoolPath.appCss.themeFont			= _self.basePath.staticCss + config.live.defaultThemeFontCss;
schoolPath.appCss.rtlCss				= _self.basePath.appCss + config.live.rtlFileName;
}
}
}
schoolPath.upgradeCss = {
leafpaths : {
upgradeCss 		: "upgrade.css" 
}
};
schoolPath.appeditCss = {
leafpaths : {
walkthroughCss 		: "school_onboarding_walkthrough.css" 
}
};
schoolPath.appbuilderCss = {
leafpaths : {
libCss				:	"lib.css", 
creatorCss			:	"creator.css", 
creatorBgCss		:	"creator_bg.css", 
onboardCss			:	"onboard.css", 
sectionsCss			:	"sections.css", 
themesCss			:	"themes.css", 
quickshareCss		:	"quickshare.css", 
upgradePopupCss		:	"upgradepopup.css", 
pagebuilderCss		:	"pagebuilder.css", 
pageappearanceCss	:	"pageappearance.css", 
settingsCss			:	"settings.css", 
formbuilderCss		:	"formbuilder.css", 
workflowbuilderCss	:	"workflowbuilder.css", 
pagebuilderBgCss	:	"pagebuilder_bg.css", 
delugebuilderCss	:	"deluge_builder.css", 
templatebuilderCss	:	"templatebuilder.css", 
templateprintbuilderCss	:	"templateprintbuilder.css", 
templateprintbuilderBgCss	: "templateprintbuilder_bg.css", 
dbEmCommonCss 		: "db-em-common.css", 
livechatCss			: 'schoollivechat.css', 
fontDbEmCommonCss 	: "fonts-dbem-common.css" 
}
};
schoolPath.appbuilderJs = {
leafpaths :{
libJs 				:		'lib.js', 
creatorJs			:		'creator.js', 
campaignsJs			:		'campaigns_js.js', 
bootJs				:		'boot.js', 
upgradePopupJs		:		'upgradepopup.js', 
helpCardJs			:		'helpcard.js', 
securityJs			:		'school_common_security.js' 
}
}
schoolPath.staticCss = {
leafpaths : {
pbfonticonCss 		: 'school-pb-fonticons.css', 
fontsbootCss		: 'fonts-boot.css', 
tpbootCss 			: 'tp-boot.css', 
tpthemeCss			: 'tp-theme.css', 
fontpreviewCss		: 'font-preview.css', 
supportCss 			: 'support-Feedback.css', 
zbuttonCss			: 'tp-button.css', 
fontsDbEmCommonCss	: 'fonts-dbem-common.css', 
schoolAppBrand			: 'school-app-brand.css', 
fontsEmliveCommonCss :	'fonts-emlive-common.css', 
fontsC5BuilderCss	:	'fonts-c5builder.css', 
ptFonticonsCss		: 'school-pt-fonticons.css', 
tpLibCss			: 'tp-lib.css', 
tpColorPickerCss	: 'tp-colorpicker.css', 
micsNotificationCss : 'mics_css.css' 
}
};
schoolPath.staticJs = {
leafpaths : {
requireJs 			: 'require.js', 
tpEMliveJs			: 'tp-emlive.js', 
tpC5builderJs		: 'tp-c5Builder.js', 
jqueryJs			: 'jquery.js', 
tpLiveDepsJs 		: 'tp-live-deps.js', 
tpLiveLibJs			: 'tp-livelib.js', 
supportJs			: 'support-Feedback.js', 
micsNotificationJs 	: 'mics_js.js', 
schoolsSecurityJs		: 'security.js' 
}
};
schoolPath.appJs = {
leafpaths : {
bootJs 				: 'bootstrap.js', 
liveLibJs			: 'livelib.js', 
mobileLiveJs 		: 'livelib-mobile.js', 
mobileEventsJs		: 'mobileevents.js', 
campaignsJs			: 'campaigns_js.js', 
reachusJs	 		: 'reachUs.js', 
livechatJs			: 'schoollivechat.js', 
bannerJs	 		: 'school_banner.js' 
}
};
schoolPath.appCss = {
leafpaths : {
bootCss 			: 'boot.css', 
reachusCss 			: 'reachUs.css', 
pageCss				: 'page.css', 
pageOldCss 			: 'pageold.css', 
mobileCss			: 'mobilelive.css', 
customizedPortalTemplateCss	:	'customizedPortalTemplate.css', 
bannerCss	 		: 'school_banner.css', 
nlpCss				: 'school_nlp.css' 
}
};
schoolPath.announcementJs = {
leafpaths : {
betafeatureJs 		: 'school_betafeature.js' 
}
};
schoolPath.announcementCss = {
leafpaths : {
betafeatureCss 		: 'school_betafeature.css' 
}
};
schoolPath.campaignCss = {
leafpaths : {
assistbotCss 		: 'assistbot.css' 
}
};
new schoolPath({
cssServerPrefix : "https://css.zohostatic.in/creator", 
jsServerPrefix : "https://js.zohostatic.in/creator",
staticLabel : "schools10549",
buildLabel : "11657",
common : {
wmsliteJsUrl : "//js.zohostatic.in/ichat/v314_https/js/wmsliteapi.js",
storeJSUrl	 : "https://js.zohostatic.in/storehandler/v9/js/zswidget.min.js",
storeCssUrl	 : "https://css.zohostatic.in/storehandler/v9/css/zswidget.min.css",
wmsBarJsUrl	 : "//js.zohostatic.in/ichat/v314_https/js/wmsbar.js",
wmsBarCssUrl : "//css.zohostatic.in/ichat/v314_https/css/wmsbar.css"
},
live : {
defaultThemeFileCss : "theme3.1.css",
defaultThemeFontCss : "font-lato.css",
rtlFileName			: "rtl_theme3.1.css"
}
}).init();</script><link rel="dns-prefetch" href="//css.zohostatic.in"><link rel="dns-prefetch" href="//js.zohostatic.in">
<script>schoolGlobal.isAdmin = true;	
schoolGlobal.isEditSupport = false;	var c = getCookie('schoolNEWUIPUBLICPORTAL');if(c != null && c != undefined && c == 'false'){}</script><script>
var managerConfig = {};

var cssLoaded = false;
function hideWelcomeLoading(){
if(!cssLoaded || (typeof(loadingFlag) != "undefined" && loadingFlag)) {
setTimeout(hideWelcomeLoading,100);
return false;
}
var d = document.getElementById("school-init-loader-animation");
d.className += " complete";   	
var element = document.getElementById("school-welcome-loading");
element.className = element.className + " fadeOut";
setTimeout(function(){element.parentNode.removeChild(element);},200);
document.body.className = document.body.className.replace("school-body-init ","");
}
var wFlag 				= false;								
var appMeta 			= {"APPLINKNAME":"schooling","isPaymentCallback":false,"APPTHEMECOLOR":"1","APPVIEWOPTION":"1","CUSTOMTHEME":true,"APPPAGES":{"Timetable":{"PAGELINKNAME":"Timetable","PAGEISHIDDEN":false,"COMPONENTS":[{"COMPDISPLAYNAME":"Class Timing Sets","COMPLINKNAME":"Class_Timing_Sets"},{"COMPDISPLAYNAME":"Grade & Timing Set Mapping","COMPLINKNAME":"Grade_Timing_set_Mapping"},{"COMPDISPLAYNAME":"Set Timetable","COMPLINKNAME":"Set_Timetable"},{"COMPDISPLAYNAME":"All Grade Timetables","COMPLINKNAME":"All_Grade_Timetables"}],"PAGEDISPLAYNAME":"Timetable"},"Employee":{"PAGELINKNAME":"Employee","PAGEISHIDDEN":false,"COMPONENTS":[{"COMPDISPLAYNAME":"Employee Dashboard","COMPLINKNAME":"Employee_Dashboard"},{"COMPDISPLAYNAME":"Employee Attendance","COMPLINKNAME":"Employee_Attendance_Report"},{"COMPDISPLAYNAME":"Students Attendance","COMPLINKNAME":"Student_Attendance_View"}],"PAGEDISPLAYNAME":"Employee"},"Academics":{"PAGELINKNAME":"Academics","PAGEISHIDDEN":false,"COMPONENTS":[{"COMPDISPLAYNAME":"Add Grade","COMPLINKNAME":"Add_Grade"},{"COMPDISPLAYNAME":"Grades","COMPLINKNAME":"Grades"},{"COMPDISPLAYNAME":"Subjects and Faculties Allotment","COMPLINKNAME":"Subjects_and_Faculties_Allotment"},{"COMPDISPLAYNAME":"All Subjects","COMPLINKNAME":"All_Subjects"},{"COMPDISPLAYNAME":"Announcements","COMPLINKNAME":"Announcements"}],"PAGEDISPLAYNAME":"Academics"},"Parent":{"PAGELINKNAME":"Parent","PAGEISHIDDEN":false,"COMPONENTS":[{"COMPDISPLAYNAME":"Parent Dashboard","COMPLINKNAME":"Parent_Dashboard"}],"PAGEDISPLAYNAME":"Parent"},"Admin":{"PAGELINKNAME":"Admin","PAGEISHIDDEN":false,"COMPONENTS":[{"COMPDISPLAYNAME":"Admin Dashboard","COMPLINKNAME":"Admin_Dashboard"},{"COMPDISPLAYNAME":"Add Student","COMPLINKNAME":"Add_Student"},{"COMPDISPLAYNAME":"Add Employee","COMPLINKNAME":"Add_Employee"},{"COMPDISPLAYNAME":"Student Details","COMPLINKNAME":"Student_Details"},{"COMPDISPLAYNAME":"Employee Details","COMPLINKNAME":"Employee_Details"}],"PAGEDISPLAYNAME":"Admin"},"Student":{"PAGELINKNAME":"Student","PAGEISHIDDEN":false,"COMPONENTS":[{"COMPDISPLAYNAME":"Student Dashboard","COMPLINKNAME":"Student_Dashboard"}],"PAGEDISPLAYNAME":"Student"},"Settings":{"PAGELINKNAME":"Settings","PAGEISHIDDEN":false,"COMPONENTS":[{"COMPDISPLAYNAME":"Institute Details","COMPLINKNAME":"Institute_Details"},{"COMPDISPLAYNAME":"Current Academic Year","COMPLINKNAME":"Current_Academic_Year"},{"COMPDISPLAYNAME":"Departments","COMPLINKNAME":"Departments"},{"COMPDISPLAYNAME":"Designations","COMPLINKNAME":"Designations"},{"COMPDISPLAYNAME":"Student Categories","COMPLINKNAME":"Student_Categories"},{"COMPDISPLAYNAME":"Student Religions","COMPLINKNAME":"Student_Religions"}],"PAGEDISPLAYNAME":"Settings"}},"APPTHEME":3,"ISPREVIEWACTION":false,"APPDISPLAYNAME":"Schooling","FEATURES":{"showFirstTimeTutorial":true,"showSignupHelpCard":true},"PAGESLIST":["Admin_Dashboard","Employee_Dashboard","Parent_Dashboard","Student_Dashboard"]};
var sharedBy			= "null";
var contactSRC			= "https://contacts.zoho.in/file?fs=thumb&ID=60000893605";													
var isMarketingCampaign = false;
var isMICSNotificationEnabled = false;
var showBetaFeatures 			= "false";
var isBrowserDeprecated = false;
var showSecurityBannerInLive = false;
var isShowAdminBanner = true;			
var isDevAccount = false;
var bootConfig 			= {
setup			: "in",
useCompression	: true,
label			: "11657",
staticLabel		: "schools10549",
jsApacheServer	: jsApacheServer,
cssApacheServer	: cssApacheServer,
walkThrough		: wFlag, 
appMeta			: appMeta,
contactSRC		: contactSRC,
isPrviewAction	: false,
managerConfig	: managerConfig,
isBrowserDeprecated		: isBrowserDeprecated,
scopeId : "shreegh44",
appId : "12595000000003003",
isAppOwner : true,
showSecurityBannerInLive : showSecurityBannerInLive,
isMobile	: false,
showBetaFeatures : showBetaFeatures,
isShowAdminBanner : isShowAdminBanner,
isDevAccount : isDevAccount,
isC5 : true,
favIconUrl	: 'https://css.zohostatic.in/creator/11657/images/database_fav_small.ico',
};
var customThemeMeta 	= '[null,{"12595000000005771":"tech-2-l-add","12595000000009853":"ui-1-lock-circle","12595000000009855":"users-single-03","12595000000005653":"travel-church","12595000000009851":"holidays-dead-hand","12595000000003633":"education-pencil-47","12595000000003797":"education-hat","12595000000003631":"ui-1-calendar-check-62","12595000000003637":"business-chart-bar-32","12595000000009857":"users-circle-10","12595000000003955":"ui-1-settings-gear-64","12595000000003635":"business-chart-bar-32","12595000000005535":"design-shape-circle","12595000000009859":"users-parent","12595000000004723":"media-2-guitar","12595000000003959":"ui-1-calendar-check-62","12595000000003957":"education-school","12595000000004727":"media-1-brightness-47","12595000000005065":"users-2-contacts-44","12595000000009863":"ui-1-calendar-grid-61","12595000000006279":"sport-tactic","12595000000009865":"ui-1-settings-gear-63","12595000000009861":"files-book-08","12595000000003963":"design-2-layers","12595000000003643":"users-square-33","12595000000003367":"users-2-a-add","12595000000003961":"design-2-filter-organization","12595000000004455":"ui-1-calendar-grid-61","12595000000003967":"travel-church","12595000000003801":"ui-1-check-square-11","12595000000009867":"holidays-dead-hand","12595000000003965":"business-hierarchy-53","12595000000003805":"media-1-speaker","12595000000003803":"education-books-46","12595000000006685":"food-hob","12595000000006961":"users-2-b-love","12595000000004183":"users-2-focus","12595000000006445":"ui-1-calendar-60","12595000000006885":"holidays-glove","12595000000003651":"users-parent","12595000000005351":"education-pencil-47","12595000000005231":"business-progress","12595000000006527":"food-hob","12595000000009839":"users-single-03","12595000000003015":"ui-1-lock-circle","12595000000004863":"shopping-mobile-card","12595000000004587":"ui-1-calendar-grid-61","12595000000003615":"users-2-contacts-44","12595000000003659":"files-book-08","12595000000003813":"arrows-2-time","12595000000006007":"design-2-3d-29","12595000000003019":"users-add-27","12595000000003811":"ui-1-calendar-grid-58","12595000000006965":"users-2-b-love","12595000000009837":"ui-1-lock-circle","12595000000003975":"business-hierarchy-53","12595000000003619":"users-2-contacts-45","12595000000003817":"ui-3-calendar-add","12595000000003815":"files-time","12595000000009841":"files-user","12595000000004591":"design-2-3d-29","12595000000009843":"users-parent","12595000000003661":"files-add","12595000000006131":"shopping-delivery","12595000000005889":"tech-2-l-add","12595000000009849":"ui-1-settings-gear-64","12595000000009845":"files-book-08","12595000000005403":"media-1-button-previous","12595000000009847":"ui-1-calendar-grid-58","12595000000003947":"ui-1-calendar-grid-61","12595000000003627":"users-single-03"}]'; 
var walkthroughCSSFlag = false;
if(isMICSNotificationEnabled){
var micsConfig = {};
micsConfig.sharedBy="60000893504";	
micsConfig.tipengineURL="https://tipengine.zoho.in";	
micsConfig.micsServiceId="144"; 
micsConfig.isFlatDashboardEnabled = true; 
bootConfig.micsConfig = micsConfig;
}</script><script>bootConfig.jsVersion = "/es6";
window.onload = function(){
setTimeout(function(){
cssLoaded = false;
var _cssDependencyList = [schoolPath.staticCss.fontsbootCss, 
schoolPath.appCss.themeFont, 
schoolPath.staticCss.tpbootCss,
//schoolPath.staticCss.fontsDbEmCommonCss,
schoolPath.staticCss.schoolAppBrand,
schoolPath.appCss.bootCss,
schoolPath.staticCss.tpthemeCss,
schoolPath.appCss.themeCss];
if(schoolGlobal.appDirectionMeta.isRTL){
_cssDependencyList.push(schoolPath.appCss.rtlCss);
}
loadFiles(_cssDependencyList).then(function(){
cssLoaded = true;
});
var _bootList	= [schoolPath.staticJs.requireJs,schoolPath.appJs.bootJs];
loadFiles(_bootList).then(function(){
var booter = new schoolBoot(bootConfig);
booter.appInit({ 
isMarketingCampaign : isMarketingCampaign,
isMICSNotificationEnabled : isMICSNotificationEnabled,
loadBanner : (isBrowserDeprecated || showSecurityBannerInLive)
});
});
},0);
};</script></head><body class="school-body-init primary_theme primary_sidebar_theme school-design-switch  school_live_adminbar school-c5-live-walkthrough " >
<div id="school-welcome-loading" class="school_loader_container "><div id="school-init-loader-animation" class="school_initial_loader" style=""><span>Schooling</span> <div class="school_initial_progess"><div class="school_on_loading"></div></div><div class="school_initial_progess "><div class="school_on_loading"></div></div></div></div><div class="wrapper container-fixed school-full-height school-dem-container   ">

  

<div id="liveHeader"><ul class="liveHeader-breadcrump"><li><a class="school-dem-liveHeader-logo" href="https://creator.zoho.in"></a></li><li class="school-dem-liveHeader-separator"><i class="fa fa-angle-right"></i></li><li><a href="">Schooling
</a></li></ul><ul id="viewOption" class="liveHeader-center-menu"><li><a viewchoice="1" id="webView" href="javascript:;" class="school-live-deviceMenu liveHeader-menu-active"><i class="school-dem-laptop-icon"></i></a></li><li><a viewchoice="2" id="mobileView" href="javascript:;" class="school-live-deviceMenu"><i class="school-dem-mob-icon"></i></a></li><li><a viewchoice="3" id="tabletView" href="javascript:;" class="school-live-deviceMenu"><i class="school-dem-tab-icon"></i></a></li></ul><ul class="liveHeader-menus"><li><a href='javascript:void(0);' class="school-dem-upgrade" onclick="Upgrade.redirectToUpgradePage('shreegh44', 'Live_Header', true);">



Trial expires in
<span class="school-dem-trial-day">1</span> day



<span> Upgrade </span></a>

</li><li><a id="editAppEl" href="https://creator.zoho.in/appbuilder/shreegh44/schooling/edit" class="school-edit-icon">
<i class="school-dem-edit-icon"></i>
<span class="">Edit this application</span> </a></li><li><a href="javascript:;" class="school-admin-action school-admin-help-opt" id="school-more-help">
<i class="school-dem-help-icon"></i>
<span class="">Help</span> </a></li></ul></div>



<div id="loadingEl" class="school-dem-loader-container" style="display:none;"><div class="ball-pulse-container"><div></div><div></div><div></div><div></div></div></div>
<div id="appViewContainer" class="school-full-height">
<div class="school-header"><div class="brand"><a href="https://app.zohocreator.in" style="display:none;">

</a>
<a href="">

<span class="school-app-icon-details school-app-brand-appicon-hasicon" style="display: none"> <span class="school-app-brand-appicon-icon"> <span class='school-app-brand iconimages school-ab-finance6'></span> </span></span>

<span class="school-app-brand-appname"> Schooling </span></a>
</div><div class="brand hide" id="school-applicationHeaderDiv"><a href="javascript:void(0);" id="school-applicationHeaderBar">
</a>
<a href="javascript:void(0);" id="backToSection" class="school-dem-back-button school-dem-back-active">
<i class="school-li-outline arrows-1-minimal-left"></i>
</a></div>
<div id="school-header-top-bar-wrapper" class="header_top_bar" ><a href="javascript:void(0);" class="menutoggle" id="menuToggle"> <i class="fa fa-dedent fa-fw"></i> </a>

<div class="top_navbar">


<div id="school-account-settings" class="top_navbar_user school_navbar_noicons"><a href="javascript:;">
<img src="" class="pull_left user_image">			
<span class="navbar_user_name">shreevatsa hegde</span> 
</a></div><div class="clear"></div></div></div></div>
<div class="topbar_dropdown" id="school-account-dropdown" style="right:0.3%"><div class="Profile-info"><div class="user-image"><a href="javascript:;">
<img src="" class="pull_left user_image">			
</a></div><div class="user-info"><div class="user-name"><span class="navbar_user_name">shreevatsa hegde</span></div><div class="user-email-id"><a href="mailto:shreegh44&#x40;gmail.com"><span class="navbar_user_name">shreegh44&#x40;gmail.com</span></a> </div><div class="user-privacy">
<a href="https://accounts.zoho.in/u/h#profile/personal" target="_blank">My Account</a>



<a href="https://creator.zoho.in/logoutpage.jsp?sharedBy=shreegh44&appLinkName=schooling&appID=12595000000003003" class="dropdown_option">			
<i class="fa fa-sign-out"></i>
<span class="title">Sign out</span> </a>
</div></div></div><div class="Profile-option"><ul><li>
<a href="https://creator.zoho.in" class="dropdown_option">					
<i class="fa fa-home"></i>
<span class="title">Home</span> </a></li></ul></div></div>



<div class="inner">
<div id="school_inner_nav_menu" class="pane_nav school-dem-hide-pane full_pane_nav">
<div class="pane_nav_menu accordion_menu school-showAppIcons container-fixed 
 " id="pane_nav_menu">
<ul id="school_nav_menu">
<li class="school_nav_section"><a id="tab_Admin" href="#Admin" class="school_tab school_transition ">
<i elName="componentIcon" class="
school-li-solid tech-desktop" 
id="t12595000000003015"></i>

<div class="school-nav-title"><span class="title">Admin</span></div>

<span class="plus"> <i class="fa fa-angle-down"></i> </span>
</a>
<ul class="school_tab_comp pane_nav_submenu" >

<li class="school_nav_com ">
 
<a id="Admin_Dashboard" href='#Page:Admin_Dashboard'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003017"></i>

<div class="school-nav-title"><span class="title">Admin Dashboard</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Add_Student" href='#Form:Add_Student'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003019"></i>

<div class="school-nav-title"><span class="title">Add Student</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Add_Employee" href='#Form:Add_Employee'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003367"></i>

<div class="school-nav-title"><span class="title">Add Employee</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Student_Details" href='#Report:Student_Details'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003615"></i>

<div class="school-nav-title"><span class="title">Student Details</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Employee_Details" href='#Report:Employee_Details'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003619"></i>

<div class="school-nav-title"><span class="title">Employee Details</span></div>
</a></li></ul></li>
<li class="school_nav_section"><a id="tab_Employee" href="#Employee" class="school_tab school_transition ">
<i elName="componentIcon" class="
school-li-solid tech-desktop" 
id="t12595000000003627"></i>

<div class="school-nav-title"><span class="title">Employee</span></div>

<span class="plus"> <i class="fa fa-angle-down"></i> </span>
</a>
<ul class="school_tab_comp pane_nav_submenu" >

<li class="school_nav_com ">
 
<a id="Employee_Dashboard" href='#Page:Employee_Dashboard'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003629"></i>

<div class="school-nav-title"><span class="title">Employee Dashboard</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Employee_Attendance_Report" href='#Report:Employee_Attendance_Report'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003631"></i>

<div class="school-nav-title"><span class="title">Employee Attendance</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Student_Attendance_View" href='#Report:Student_Attendance_View'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003633"></i>

<div class="school-nav-title"><span class="title">Students Attendance</span></div>
</a></li></ul></li>
<li class="school_nav_section"><a id="tab_Student" href="#Student" class="school_tab school_transition no-comp-section">
<i elName="componentIcon" class="
school-li-solid tech-desktop" 
id="t12595000000003643"></i>

<div class="school-nav-title"><span class="title">Student</span></div>

</a>
<ul class="school_tab_comp pane_nav_submenu" style='display:none;'>

<li class="school_nav_com ">
 
<a id="Student_Dashboard" href='#Page:Student_Dashboard'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003645"></i>

<div class="school-nav-title"><span class="title">Student Dashboard</span></div>
</a></li></ul></li>
<li class="school_nav_section"><a id="tab_Parent" href="#Parent" class="school_tab school_transition no-comp-section">
<i elName="componentIcon" class="
school-li-solid tech-desktop" 
id="t12595000000003651"></i>

<div class="school-nav-title"><span class="title">Parent</span></div>

</a>
<ul class="school_tab_comp pane_nav_submenu" style='display:none;'>

<li class="school_nav_com ">
 
<a id="Parent_Dashboard" href='#Page:Parent_Dashboard'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003653"></i>

<div class="school-nav-title"><span class="title">Parent Dashboard</span></div>
</a></li></ul></li>
<li class="school_nav_section"><a id="tab_Academics" href="#Academics" class="school_tab school_transition ">
<i elName="componentIcon" class="
school-li-solid tech-desktop" 
id="t12595000000003659"></i>

<div class="school-nav-title"><span class="title">Academics</span></div>

<span class="plus"> <i class="fa fa-angle-down"></i> </span>
</a>
<ul class="school_tab_comp pane_nav_submenu" >

<li class="school_nav_com ">
 
<a id="Add_Grade" href='#Form:Add_Grade'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003661"></i>

<div class="school-nav-title"><span class="title">Add Grade</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Grades" href='#Report:Grades'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003797"></i>

<div class="school-nav-title"><span class="title">Grades</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Subjects_and_Faculties_Allotment" href='#Report:Subjects_and_Faculties_Allotment'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003801"></i>

<div class="school-nav-title"><span class="title">Subjects and Faculties Allotment</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="All_Subjects" href='#Report:All_Subjects'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003803"></i>

<div class="school-nav-title"><span class="title">All Subjects</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Announcements" href='#Report:Announcements'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003805"></i>

<div class="school-nav-title"><span class="title">Announcements</span></div>
</a></li></ul></li>
<li class="school_nav_section"><a id="tab_Timetable" href="#Timetable" class="school_tab school_transition ">
<i elName="componentIcon" class="
school-li-solid tech-desktop" 
id="t12595000000003811"></i>

<div class="school-nav-title"><span class="title">Timetable</span></div>

<span class="plus"> <i class="fa fa-angle-down"></i> </span>
</a>
<ul class="school_tab_comp pane_nav_submenu" >

<li class="school_nav_com ">
 
<a id="Class_Timing_Sets" href='#Report:Class_Timing_Sets'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003813"></i>

<div class="school-nav-title"><span class="title">Class Timing Sets</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Grade_Timing_set_Mapping" href='#Report:Grade_Timing_set_Mapping'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003815"></i>

<div class="school-nav-title"><span class="title">Grade &amp; Timing Set Mapping</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Set_Timetable" href='#Form:Set_Timetable'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003817"></i>

<div class="school-nav-title"><span class="title">Set Timetable</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="All_Grade_Timetables" href='#Report:All_Grade_Timetables'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003947"></i>

<div class="school-nav-title"><span class="title">All Grade Timetables</span></div>
</a></li></ul></li>
<li class="school_nav_section"><a id="tab_Settings" href="#Settings" class="school_tab school_transition ">
<i elName="componentIcon" class="
school-li-solid tech-desktop" 
id="t12595000000003955"></i>

<div class="school-nav-title"><span class="title">Settings</span></div>

<span class="plus"> <i class="fa fa-angle-down"></i> </span>
</a>
<ul class="school_tab_comp pane_nav_submenu" >

<li class="school_nav_com ">
 
<a id="Institute_Details" href='#Report:Institute_Details'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003957"></i>

<div class="school-nav-title"><span class="title">Institute Details</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Current_Academic_Year" href='#Report:Current_Academic_Year'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003959"></i>

<div class="school-nav-title"><span class="title">Current Academic Year</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Departments" href='#Report:Departments'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003961"></i>

<div class="school-nav-title"><span class="title">Departments</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Designations" href='#Report:Designations'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003963"></i>

<div class="school-nav-title"><span class="title">Designations</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Student_Categories" href='#Report:Student_Categories'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003965"></i>

<div class="school-nav-title"><span class="title">Student Categories</span></div>
</a></li>
<li class="school_nav_com ">
 
<a id="Student_Religions" href='#Report:Student_Religions'>
<i elName="componentIcon" class="school-li-solid ui-3-playlist" 
id="t12595000000003967"></i>

<div class="school-nav-title"><span class="title">Student Religions</span></div>
</a></li></ul></li>
</ul></div></div><!--Left Pane ends here--> 

<div id="school-component"  elname="school-component" class="page_content_wrapper container-fixed"></div></div></div>
<div id="preloader" class="loading-animation"><div class="line"><span class="break dot1"></span> <span class="break dot2"></span> <span class="break dot3"></span> <span class=""></span> <span class=""></span></div></div><div class="appFooter"><p>Â© 2018 ZOHO Corp. All rights reserved.</p> </div>	
<div><div class="school-app-freeze-layer" id="school-app-freeze-layer" style="display: none"></div><div class="school-panel" id="panel"><div class="admin-panel-wrapper hide" id="adminPanel"><div class="clear"></div><div id="adminPanelContainer"><div id="adminPanelContent">
<ul id="tabContainer" class="switch_user_tab"><li><a class="themePanel">Themes</a></li><li><a class="iconPanel">Icons</a></li>
<a href="javascript:;" id="adminpanel-close" class="tab_anchor"><i class="fa fa-times"></i></a></ul><div id="admin_accordion" class='school-overflow-hidden'><div class="theme_color_wrapper" style="display:none;"><div class="theme_color_options js-tooltip" style="margin-top:10px;">
<span class="selectThemes">Select Theme</span> <span id="1" class="theme_opt school_transition bg_blue"> <b class="theme_header theme_header_left"></b>
<b class="theme_header theme_header_right"></b>
<b class="theme_sidebar"></b>
<b class="theme_sidebar_menu"></b> </span><span id="2" class="theme_opt school_transition bg_green_tab"> <b class="theme_header"></b>
<b class="theme_topbar"></b>
<b class="theme_topbar_search"></b> </span><span id="3" class="theme_opt school_transition bg_red"> <b class="theme_header theme_header_left"></b>
<b class="theme_header theme_header_right"></b>
<b class="theme_sidebar"></b> </span><span id="4" class="theme_opt school_transition bg_blue_light"> <b class="theme_header theme_header_left"></b>
<b class="theme_header theme_header_right"></b>
<b class="theme_sidebar"></b> </span><span id="5" class="theme_opt school_transition bg_sky_blue"> <b class="theme_header theme_header_left"></b>
<b class="theme_header theme_header_right"></b>
<b class="theme_sidebar"></b>
<b class="theme_sidebar_menu"></b> </span><span id="6" class="theme_opt school_transition bg_black_tab"> <b class="theme_header"></b>
<b class="theme_topbar"></b> </span></div></div>
<div class="icons_wrapper">
<div class="use_icon_option clearfix"><div id="useIconSwitchDiv" class="school-dem-icon-choose"><label>Use Icons</label>
<div class="school-dem-switch-toggle"><input type="checkbox" id="useIconSwitch" name="useIconSwitch" switch="bool"><label for="useIconSwitch" data-on-label="Yes" data-off-label="No"></label></div></div><div id="toggleIconSwitchDiv" class="school-dem-icon-choose school-dem-icon-type"><label>Icon Type</label>
<div class="school-dem-switch-toggle"><input type="checkbox" id="toggleIconSwitch" name="toggleIconSwitch" switch="bool"><label for="toggleIconSwitch" data-on-label="Outline" data-off-label="Solid"></label></div></div><div class="iconBtnCntr hide"><input type="button" name="saveIcons" class="school-live-primary-btn" value='Save' />
<input type="button" name="resetIcons" class="school-live-secondary-btn" value='Reset' /></div></div>
<div class="icon_content_wrapper"><div class="icon_menu_wrapper"><ul><li class="school_nav_section" key="Admin" type="0" uid="12595000000003011">
<a href="javascript:void(0);" class="school_tab school_transition">
<i class=""></i>
<span class="title">Admin</span> </a>

<ul class="school_tab_comp pane_nav_submenu">
<li class="school_nav_com" key="Admin_Dashboard" type="1" uid="12595000000003017">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Admin Dashboard</span> </a></li>
<li class="school_nav_com" key="Add_Student" type="1" uid="12595000000003019">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Add Student</span> </a></li>
<li class="school_nav_com" key="Add_Employee" type="1" uid="12595000000003367">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Add Employee</span> </a></li>
<li class="school_nav_com" key="Student_Details" type="1" uid="12595000000003615">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Student Details</span> </a></li>
<li class="school_nav_com" key="Employee_Details" type="1" uid="12595000000003619">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Employee Details</span> </a></li></ul></li><li class="school_nav_section" key="Employee" type="0" uid="12595000000003623">
<a href="javascript:void(0);" class="school_tab school_transition">
<i class=""></i>
<span class="title">Employee</span> </a>

<ul class="school_tab_comp pane_nav_submenu">
<li class="school_nav_com" key="Employee_Dashboard" type="1" uid="12595000000003629">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Employee Dashboard</span> </a></li>
<li class="school_nav_com" key="Employee_Attendance_Report" type="1" uid="12595000000003631">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Employee Attendance</span> </a></li>
<li class="school_nav_com" key="Student_Attendance_View" type="1" uid="12595000000003633">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Students Attendance</span> </a></li></ul></li><li class="school_nav_section" key="Student" type="0" uid="12595000000003639">
<a href="javascript:void(0);" class="school_tab school_transition">
<i class=""></i>
<span class="title">Student</span> </a>
</li><li class="school_nav_section" key="Parent" type="0" uid="12595000000003647">
<a href="javascript:void(0);" class="school_tab school_transition">
<i class=""></i>
<span class="title">Parent</span> </a>
</li><li class="school_nav_section" key="Academics" type="0" uid="12595000000003655">
<a href="javascript:void(0);" class="school_tab school_transition">
<i class=""></i>
<span class="title">Academics</span> </a>

<ul class="school_tab_comp pane_nav_submenu">
<li class="school_nav_com" key="Add_Grade" type="1" uid="12595000000003661">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Add Grade</span> </a></li>
<li class="school_nav_com" key="Grades" type="1" uid="12595000000003797">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Grades</span> </a></li>
<li class="school_nav_com" key="Subjects_and_Faculties_Allotment" type="1" uid="12595000000003801">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Subjects and Faculties Allotment</span> </a></li>
<li class="school_nav_com" key="All_Subjects" type="1" uid="12595000000003803">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >All Subjects</span> </a></li>
<li class="school_nav_com" key="Announcements" type="1" uid="12595000000003805">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Announcements</span> </a></li></ul></li><li class="school_nav_section" key="Timetable" type="0" uid="12595000000003807">
<a href="javascript:void(0);" class="school_tab school_transition">
<i class=""></i>
<span class="title">Timetable</span> </a>

<ul class="school_tab_comp pane_nav_submenu">
<li class="school_nav_com" key="Class_Timing_Sets" type="1" uid="12595000000003813">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Class Timing Sets</span> </a></li>
<li class="school_nav_com" key="Grade_Timing_set_Mapping" type="1" uid="12595000000003815">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Grade &amp;amp; Timing Set Mapping</span> </a></li>
<li class="school_nav_com" key="Set_Timetable" type="1" uid="12595000000003817">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Set Timetable</span> </a></li>
<li class="school_nav_com" key="All_Grade_Timetables" type="1" uid="12595000000003947">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >All Grade Timetables</span> </a></li></ul></li><li class="school_nav_section" key="Settings" type="0" uid="12595000000003951">
<a href="javascript:void(0);" class="school_tab school_transition">
<i class=""></i>
<span class="title">Settings</span> </a>

<ul class="school_tab_comp pane_nav_submenu">
<li class="school_nav_com" key="Institute_Details" type="1" uid="12595000000003957">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Institute Details</span> </a></li>
<li class="school_nav_com" key="Current_Academic_Year" type="1" uid="12595000000003959">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Current Academic Year</span> </a></li>
<li class="school_nav_com" key="Departments" type="1" uid="12595000000003961">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Departments</span> </a></li>
<li class="school_nav_com" key="Designations" type="1" uid="12595000000003963">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Designations</span> </a></li>
<li class="school_nav_com" key="Student_Categories" type="1" uid="12595000000003965">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Student Categories</span> </a></li>
<li class="school_nav_com" key="Student_Religions" type="1" uid="12595000000003967">
<a href="javascript:void(0);">
<i class="" ></i>
<span class="title" >Student Religions</span> </a></li></ul></li></ul></div><div class="icon_tab_wrapper"><div id="icon_search_box" class="icon_search_container"><input type="text" name="iconSearchInput" class="icon_search_bar" placeholder="Search..." autocomplete="off">
<i class="school-li-solid ui-1-zoom cp"></i></div><div id="icons_container_wrapper" class="icons_search_wrapper"><div class="tableHeader recentsTable" style="display:none;">Recent</div><table name="recentsTable"><tbody></tbody></table><div class="tableHeader iconsTable" style="display:none;">Others</div><table name="iconsTable"><tbody></tbody></table><table name="iconsTableClone"><tbody></tbody></table></div><div class="icons_notused_wrapper"><div>Icons are currently not used in this application.</div></div></div></div><!----></div></div></div></div></div><div id="helpPanel" class="school-help-panel hide"><div class="school_more_help"><div class="school_help-panelheader"><span class="school_help-text">Help</span> <a href="javascript:;" id="school_helpPanel-close" class="tab_anchor"><i class="fa fa-times"></i></a></div><div class="school_help_container">
<div class="school-dem-clearfix"><div id="quickStart" class="school_help-webinar pull-left school-half-width"><a href="https://www.zoho.in/creator/newhelp/images/creator5-quick-start-guide.pdf" target="_blank">
<i class="fa fa-file-text"></i>
<span class="school_help-header">Quick Start Guide</span> <span class="school_help-subcontent">Get introduced to Zoho Creator application building and the interface. Build along a complete application from scratch.</span> </a></div><div id="userGuide" class="school_help-webinar pull-left school-half-width"><a href="https://www.zoho.in/creator/newhelp/user-guides.html" target="_blank">
<i class="fa fa-book"></i>
<span class="school_help-header">User Guide</span> <span class="school_help-subcontent">Learn to build, customize, and access custom apps across web, mobile, and tablet.</span> </a></div>
<div id="webinar" class="school_help-webinar school-half-width pull-left"><a href="https://www.zoho.in/creator/webinars.html?source=inproduct_homeHelp" target="_blank" >	
<i class="fa fa-users"></i>
<span class="school_help-header">Webinars</span> <span class="school_help-subcontent">Join our live webinars to learn how to build, customize, and access your apps on Zoho Creator. Chat with our experts in real-time and get all your questions answered.</span> </a></div>
<div id="forums" class="school_help-webinar pull-left school-half-width"><a href="https://forums.zoho.com/zoho-creator" target="_blank">
<i class="fa fa-comments"></i>
<span class="school_help-header">Forums</span> <span class="school_help-subcontent">Post a topic, discuss app development ideas, and tap into the knowledge shared among fellow Zoho Creator users, all in a single place.</span> </a></div><div id="support" class="school_help-support pull-left school-half-width"><a id="school-reachus-live-support" style="cursor: pointer;">
<i class="fa fa-envelope"></i>
<span class="school_help-header">Support</span> <span class="school_help-subcontent">One stop place to get all your questions answered and to connect with the Zoho Creator Team.</span> </a></div><div id="hireaexpert" class="school_help-hireAexpert school-half-width pull-left"><a href="http://www.zoho.in/creator/post-requirement.html" target="_blank" >
<i class="fa fa-user"></i> 
<span class="school_help-header">Hire a Certified Expert</span> <span class="school_help-subcontent">Experts who have earned the trust of our community by contributing ideas available here to help you.</span> </a></div></div></div></div></div></div><div class="school-fade-bg hide" id="shareBg"></div><div class="school-popup-container hide" id="sharePopup"><div class="school-popup-box"><div class="school-popup-box-outer"><div class="school-popup-box-header"><span>Revoke access for my users</span> <a class="school-popup-close"></a></div>
<div class="school-popup-box-content clearfix"><div class="clearfix school-pad-20">
<div class="pull-left share_to_users_img"></div><ul class="school-popup-box-content-ul pull-left">
<li><i class="school-check"></i><span>This setting applies to all your users, and to all the applications in your account.</span></li><li><i class="school-check"></i><span>Your users will access the old version by default.</span></li><li><i class="school-check"></i><span>Ensure that you have not used any new URLs in any of your websites. If so, change those to the old URLs before changing this setting.</span></li> </ul></div><div class="school-popup-footer clearfix school-pad-20"><a class="school-live-primary-btn pull-right school-bdr-rad-4 disabledButton hidden revertButton">Revoke access</a>
<div class="school-popup-footer-decision"><label for="school_I_agree_to_the_terms" class="agree-decision-box-label">I have read the above conditions.</label>
<label>
<span> <input id="school_I_agree_to_the_terms" class="customCheckbox" name="school_I_agree_to_the_terms" title="" value="Decision box" type="checkbox" autocomplete="off"><label for="school_I_agree_to_the_terms"></label> </span></label></div></div></div></div></div></div><div class="school-fade-bg hide" id="tutorialBg"></div><a href="javascript:;" class="school-dialogue-close" id="tutorialPopupClose" style="display: none;"></a>
<div class="school-popup-container hide" id="tutorialPopup"><div class="school-popup-box"><a class="school-slide-arrow school-arrow-left">	</a>
<a class="school-slide-arrow school-arrow-right">	</a>
<div class="school-popup-box-outer-feature"><div class="school-popup-box-content clearfix school-block"><div class="clearfix school-block"><div class="school-theme-slider clearfix school-block"><div class="bounceIn animated image-delay school-pa-img slide-1"><div class="school-image-wraper screen-1 fade-in"></div><div class="school-thumb-container"><ul class="school-thumbs"><li class="theme-1"></li><li class="theme-2"></li><li class="theme-3"></li><li class="theme-4"></li><li class="theme-5"></li></ul></div></div></div><div class="school-theme-fearture-slider"><h3 class="school-theme-fearture-h3">Introducing the New <b>zoho Creator ui</b></h3>
<ul class="school-theme-fearture-list"><li class="bounceInRight animated one"><div class="school-theme-fearture-badge"><span><i class="fa fa-check"></i> </span></div><div class="school-theme-fearture-detail"><b>New Themes</b><span>A fresh set of colorful themes.</span></div></li><li class="bounceInRight animated two"><div class="school-theme-fearture-badge"><span><i class="fa fa-check"></i> </span></div><div class="school-theme-fearture-detail"><b>Icons</b><span>Clear icons for each part of the application.</span></div></li><li class="bounceInRight animated three"><div class="school-theme-fearture-badge"><span><i class="fa fa-check"></i> </span></div><div class="school-theme-fearture-detail"><b>Font Styles</b><span>Modern flat new fonts.</span></div></li></ul></div></div></div></div></div></div><div class="forwardImageSwitch hide"><div class="bounceIn animated image-delay school-pa-img slide-1"><div class="school-image-wraper screen-1 fade-in"></div><div class="school-thumb-container"><ul class="school-thumbs"><li class="theme-1"></li><li class="theme-2"></li><li class="theme-3"></li><li class="theme-4"></li><li class="theme-5"></li></ul></div></div><div class="bounceIn animated image-delay school-pa-img slide-2"><div class="school-image-wraper fade-in"></div></div><div class="bounceIn animated image-delay school-pa-img slide-3"><div class="school-image-wraper fade-in"></div></div></div><div class="forwardListSwitch hide"><div><h3 class="school-theme-fearture-h3">Introducing the New <b>zoho Creator ui</b></h3> <ul class="school-theme-fearture-list"><li class="bounceInRight animated one"><div class="school-theme-fearture-badge"><span><i class="fa fa-check"></i> </span></div><div class="school-theme-fearture-detail"><b>New Themes</b><span>A fresh set of colorful themes.</span></div></li><li class="bounceInRight animated two"><div class="school-theme-fearture-badge"><span><i class="fa fa-check"></i> </span></div><div class="school-theme-fearture-detail"><b>Icons</b><span>Clear icons for each part of the application.</span></div></li><li class="bounceInRight animated three"><div class="school-theme-fearture-badge"><span><i class="fa fa-check"></i> </span></div><div class="school-theme-fearture-detail"><b>Font Styles</b><span>Modern flat new fonts.</span></div></li></ul></div><div><h3 class="school-theme-fearture-h3">Introducing the New <b>zoho Creator ui</b></h3> <ul class="school-theme-fearture-list"><li class="bounceInRight animated one"><div class="school-theme-fearture-badge"><span><i class="fa fa-check"></i> </span></div><div class="school-theme-fearture-detail"><b>Switching between versions</b><span>You can switch between the old and new UI.</span></div></li><li class="bounceInRight animated two"><div class="school-theme-fearture-badge"><span><i class="fa fa-check"></i> </span></div><div class="school-theme-fearture-detail"><b>Can I access the new UI on mobile ?</b><span>No, the new UI does not apply for the mobile web site.</span></div></li><li class="bounceInRight animated three"><div class="school-theme-fearture-badge"><span><i class="fa fa-check"></i> </span></div><div class="school-theme-fearture-detail"><b>Can my users access the new UI ?</b><span>No, the new UI is accessible only to the administrator.</span></div></li></ul></div><div><h3 class="school-theme-fearture-h3">Introducing the New <b>zoho Creator ui</b></h3> <ul class="school-theme-fearture-list"><li class="bounceInRight animated one"><div class="school-theme-fearture-badge"><span><i class="fa fa-check"></i> </span></div><div class="school-theme-fearture-detail"><b>How do I enable the new UI for my users ?</b><span>Click on "Grant access for my users" under your profile name.</span></div></li><li class="bounceInRight animated two"><div class="school-theme-fearture-badge"><span><i class="fa fa-check"></i> </span></div><div class="school-theme-fearture-detail"><b>Can my users still access the old UI ?</b><span>Once you enable the new UI for your users, they cant access the old UI.</span></div></li><li class="bounceInRight animated three"><div class="school-theme-fearture-badge"><span><i class="fa fa-check"></i> </span></div><div class="school-theme-fearture-detail"><b>How do I switch back to the old UI ?</b><span>Click on "Switch to old version" under your profile name.</span></div></li></ul></div></div></div>
<script type="text/javascript">var schoolChatEnabled 			= schoolGlobal.schoolChatEnabled;
var schoolPreSalesChatEnabled 	= schoolGlobal.schoolPreSalesEnabled;
if(typeof(i18n) == "undefined") {
var i18n = [];
}
i18n['school.reachus.successMsg'] 	= 'Your request has been sent successfully!'; 
i18n['school.general.erralert1msg'] = 'Error Occurred. We are sorry for the inconvenience.'; </script><div id="reachUs" class="school-dem-right-popup school-dem-box-sizing school-dem-freeze-content active school-dem-support-request school-support-popup-footer school-c5-support-request" style="display:none;overflow: scroll;"><div class="school-dem-right-title school-dem-box-sizing school-dem-clearfix"><span class="flt-left"> <i class="school-li-solid tech-2-headset"></i>
<span>Reach Us</span> </span><a id="reachUsExit" href="javascript:;" class="tab_anchor"><i class="school-li-outline ui-1-simple-remove"></i></a></div><div class="school-dem-tab school-dem-clearfix"><a id="school-reachus-feedback-tab" class="school-dem-tab-header school-dem-box-sizing selected">
<i class="ui-1-email-83 school-li-solid"></i>
<span>Email</span> </a>
<a id="school-reachus-editaccess-tab" class="school-dem-tab-header school-dem-box-sizing">
<i class="school-li-solid ui-1-settings-tool-66"></i>
<span>Edit Access</span> </a></div><div class="school-dem-right-content school-dem-box-sizing"><div id="school-reachus-feedback" class="school-reachus-tab-content school-c5-feedback-support"><div class="school-dem-clearfix school-dem-label-top"><label>From</label>
<div id="reqEmailId" class="school-dem-field-group"><input type="text" name="reqEmailId" class="school-dem-field school-dem-input school-dem-box-sizing" value="shreegh44&#x40;gmail.com" disabled></div></div><div id="feedBackMenu" class="school-dem-reachus-feedback"></div><div id="school-enable-appedit" class="school-dem-checkbox school-support-checkbox"><input class="school_checkbox" type="checkbox" name="editSupportPerm" id="editSupportPerm" checked><label class="school-li-solid choice-label-text" for="editSupportPerm" title=""><span>Please enable edit permission to help with troubleshooting.</span></label></div><div class="school-dem-btnactions"><input type="button" id="feedbackSupportSubmit" class="school-dem-primarybtn school-dem-btn school-dem-border-radius-2 school-dem-box-sizing" value="Submit Request"> <div class="reachus-dot-load-container"><div class="reachus-dot-load"></div><div class="reachus-dot-load"></div><div class="reachus-dot-load"></div></div></div></div><div class="school-reachus-tab-content" id="school-reachus-chat"><div class="school-dem-hdr-description"><label>
Type in your queries and start a live chat with our support team.
</label></div><textarea id="reachusChatDescription" class="school-dem-field school-dem-textarea school-dem-box-sizing school-dem-hdr-textarea"></textarea>
<div class="school-dem-btnactions"><input type="button" name="" id="reachUsStartChat" class="school-dem-primarybtn school-dem-btn school-dem-border-radius-2 school-dem-box-sizing" value="Start Chat"></div></div><div id="school-reachus-edit-access" class="school-reachus-tab-content hide"><div id="school-reachus-editaccess-enable" class="school-reachus-editaccess-enable hide"><p>To debug an issue reported, the support team may sometimes request you to enable edit access to your application. Click below to enable edit access.</p>
<input type="button" id="school-reachus-editaccess-enable-button" class="school-dem-primarybtn school-dem-btn school-dem-border-radius-2 school-dem-box-sizing" value="Enable edit access"></div><div id="school-reachus-editaccess-revoke" class="school-reachus-editaccess-revoke hide"><p>Edit access to support can be withdrawn anytime after the issue is resolved. Click here to cancel edit access to support, for your application.</p>
<input type="button" id="school-reachus-editaccess-revoke-button" class="school-dem-primarybtn school-dem-btn school-dem-border-radius-2 school-dem-box-sizing" value="Revoke edit access"></div></div></div></div>


</div>
<div id="active-DatePicker" ><div style="position:relative" id="active-DatePicker-Cont"></div></div><div class="school-scroll-mask" style="display: none;"></div>


<div class="live-chat new-live" id="schoolChat" style="display:none"><i class="live-chat-ico"></i>
<small class="circle-ripple"></small></div></body></html>
