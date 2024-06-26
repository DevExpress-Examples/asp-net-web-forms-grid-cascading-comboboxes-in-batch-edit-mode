<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128534653/14.1.4%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T124512)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
[![](https://img.shields.io/badge/💬_Leave_Feedback-feecdd?style=flat-square)](#does-this-example-address-your-development-requirementsobjectives)
<!-- default badges end -->
<!-- default file list -->
*Files to look at*:

* [DataProvider.cs](./CS/App_Code/DataProvider.cs) (VB: [DataProvider.vb](./VB/App_Code/DataProvider.vb))
* [BatchEditScript.js](./CS/BatchEditScript.js) (VB: [BatchEditScript.js](./VB/BatchEditScript.js))
* **[Default.aspx](./CS/Default.aspx) (VB: [Default.aspx](./VB/Default.aspx))**
* [Default.aspx.cs](./CS/Default.aspx.cs) (VB: [Default.aspx.vb](./VB/Default.aspx.vb))
<!-- default file list end -->
# ASPxGridView - How to implement cascading comboboxes in Batch Edit mode


<p>In this example, the combo box in the City column (the City combo box) is populated dynamically with city names via callbacks, based on the value selected in the combo box in the Country column (the Country combo box).  <br>You can find detailed steps by clicking below the "Show Implementation Details" link .<br><br><strong>MVC:</strong><br><a href="https://www.devexpress.com/Support/Center/p/T155879">GridView - A simple implementation of cascading comboboxes in Batch Edit mode</a><br><br></p>
<p><strong>See also: </strong><br><a href="https://www.devexpress.com/Support/Center/p/T356740">ASPxGridView - How to implement cascading combo boxes in Batch Edit mode by using WebMethods</a></p>


<h3>Description</h3>

The concept of cascading combo boxes requires sending a callback to the server to get data for the second editor based on the first editor's selected value.&nbsp;<br>In the meantime, it's impossible to send callbacks for built-in editors and it's necessary to use the EditItemTemplate (see&nbsp;<a href="https://www.devexpress.com/Support/Center/Question/Details/S173460">ASPxGridView - Batch Edit - Support a scenario when GridViewComboBoxColumn is used in callback mode</a>).<br>A basic scenario of this approach requires the following steps:<br>1) Use the client-side&nbsp;<a href="https://documentation.devexpress.com/AspNet/DevExpressWebASPxGridViewScriptsASPxClientGridView_BatchEditStartEditingtopic.aspx">ASPxClientGridView.BatchEditStartEditing</a>&nbsp; and&nbsp;<a href="https://documentation.devexpress.com/AspNet/DevExpressWebASPxGridViewScriptsASPxClientGridView_BatchEditEndEditingtopic.aspx">ASPxClientGridView.BatchEditEndEditing</a>&nbsp; events &nbsp;to provide the template combo box&nbsp;with values.<br>2) Handle the&nbsp;<a href="https://documentation.devexpress.com/AspNet/DevExpressWebASPxEditorsScriptsASPxClientComboBox_SelectedIndexChangedtopic.aspx">SelectedIndexChanged</a>&nbsp;event to send callbacks if it's required.<br>3) Handle the&nbsp;<a href="https://documentation.devexpress.com/AspNet/DevExpressWebASPxEditorsScriptsASPxClientComboBox_EndCallbacktopic.aspx">ASPxClientComboBox.EndCallback</a>&nbsp;event for the second editor to apply the selected item after a callback.<br>4) Handle the&nbsp;<a href="https://documentation.devexpress.com/#AspNet/DevExpressWebASPxClassesScriptsASPxClientControl_Inittopic">ASPxClientGridView.Init</a>&nbsp; and&nbsp;<a href="https://documentation.devexpress.com/AspNet/DevExpressWebASPxGridViewScriptsASPxClientGridView_EndCallbacktopic.aspx">ASPxClientGridView.EndCallback</a>&nbsp;events&nbsp; to initialize and reset global variables responsible for data providing logic&nbsp;after the grid was refreshed.&nbsp;

<br/>


<!-- feedback -->
## Does this example address your development requirements/objectives?

[<img src="https://www.devexpress.com/support/examples/i/yes-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=asp-net-web-forms-grid-cascading-comboboxes-in-batch-edit-mode&~~~was_helpful=yes) [<img src="https://www.devexpress.com/support/examples/i/no-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=asp-net-web-forms-grid-cascading-comboboxes-in-batch-edit-mode&~~~was_helpful=no)

(you will be redirected to DevExpress.com to submit your response)
<!-- feedback end -->
