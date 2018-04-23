# How to create complex custom controls (XRTreeList and XRGrid) 


<p>This example demonstrates how to create custom data-aware controls that have a complex structure. The example consists of two projects

* <strong>DevExpress.XtraReports.CustomControls. </strong>Contains all classes and methods related to custom controls.
* <strong>CustomControlExample. </strong>This project is for testing the aforementioned custom controls. This project invokes End-User Report Designers and Print Previews for both controls.<br><br>Take special note of the following classes and methods when examining the <strong>CustomControls </strong>project:<br>1. <strong>XRTreeList </strong>and <strong>XRGrid. </strong>They are XRControl descendants and contain all required properties and methods related to their visual representation.<br>1.1. The <strong>XRControl.CreatePresenter </strong>method allows you to create different presenters for visualizing your control at runtime and design time.<br>1.2. The <strong>XRControl.WriteContentTo </strong>method generates the visual representation and passes it to the resulting document.<br>1.3. The <strong>XRControl.CollectAssociatedComponents </strong>method allows you to link external objects (data source information and other Component properties) to your control.<br>1.4. The <strong>XRControl.CopyDataProperties </strong>method is required to inform your control of how to clone data source related properties.<br>1.5. The <strong>XRControl.CreateCollectionItem </strong>method defines how to create new collection items in your control.<br>1.6. The <strong>XRControl.CreateStyles </strong>method is responsible for creating specific control styles.<br>1.7. The <strong>XRControl.CreateScripts </strong>method creates scripts specific for this control.<br><br>2. <strong>XRTreeListDesigner</strong> and<strong> XRGridDesigner. </strong>These classes describe the design-time behavior of corresponding controls.<br>2.1. The <strong>XRControlDesigner.GetFilteredProperties </strong>method determines what properties should be visible in the Property Grid.<br>2.2. The <strong>XRControlDesigner.RegisterActionLists </strong>method fills the XRControl smart tag with required actions.<br><br>3. <strong>XRTreeListRuntimePresenter </strong>and <strong>XRGridRuntimePresenter. </strong>These classes generate visual representation of your controls.<br>3.1. The <strong>XRControlPresenter.CreateBrick </strong>method creates a container brick for displaying the control content.<br>3.2. The <strong>XRControlPresenter.PutStateToBrick </strong>method generates inner content based on the current control state.</p>
<br><strong>Important note: </strong><em>the VB.NET solution is for VS 2012 or newer, because it uses new operators that do not exist in VS 2010.</em><br><br><strong>See also:<br><a href="https://documentation.devexpress.com/XtraReports/7546/Examples/Create-an-End-User-Reporting-Application/Windows-Forms/How-to-Register-a-Custom-Control-in-the-End-User-Designer-s-Toolbox">How to: Register a Custom Control in the End-User Designer's Toolbox</a> <br></strong><a href="https://documentation.devexpress.com/XtraReports/CustomDocument3307.aspx">How to: Create a Numeric Label</a> <br><a href="https://documentation.devexpress.com/XtraReports/CustomDocument1304.aspx">How to: Create a Progress Bar Control</a>

<br/>

