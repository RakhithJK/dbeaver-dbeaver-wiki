## Execution Plan

### Simple plan view

If a database driver supports the visualization of the execution plan, you can see the execution plan of the current query (under cursor) by pressing <kbd>Ctrl+Shift+E</kbd> or clicking **Explain execution plan** on the context menu or in the main toolbar: ![](images/ug/Exec-plan.png)
The execution plan command generates a tree of query execution as one of the result tabs and is convenient in estimating if the query/script is quick/optimal enough: 

![](images/ug/Execution_plan.png)

You can click the rows of the execution plan to see their details (statistics) in the panels below and to the right of the plan.  
To reevaluate the plan, click the **Reevaluate** button (![](images/ug/Refresh-projects-icon.png)).
To see the source script on which the plan is based, click the **View Source** button (![](images/ug/View-Source-button.png)).

### Advanced plan view <img src="images/commercial_big.png" align="top" vspace="2" height="24">

In DBeaver [Lite](Lite-Edition), [Enterprise](Enterprise-Edition), and [Ultimate](Ultimate-Edition) editions you can use an advanced (graph) visualization of the execution plan.  
This visualization shows the most expensive (cost-based) plan nodes. You can hide all irrelevant nodes (see node details), use horizontal or vertical plan layouts, export it to an image or save it as JSON to send to a colleague.

![](images/ug/Exec-plan-graph.png)
