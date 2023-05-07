Download Link: https://assignmentchef.com/product/solved-kit206-assignment2-c-application-test-report
<br>
Your small development team of (ideally) three people has been asked to implement and test the Researcher Assessment Program desktop application. Your software product will be a databasebacked desktop application with a Windows Presentation Foundation (WPF) graphical front end, implemented in C#. As part of your development efforts you will prepare and apply a small collection of test cases to verify that the completed application meets some of the key requirements agreed with the client.

<h1>Submission</h1>

By <strong>1500 (3pm) Friday October 20<sup>th</sup> </strong>submit <u>deliverables 1 and 2</u> to the <em>Assignment 2 – C# Application &amp; Test Report</em> assignment folder on the unit’s MyLO site. Separately, your team must complete (and all members must sign) the <u>Group Assignment cover sheet</u>; this may be scanned and submitted to the MyLO dropbox if you wish.

Your teammates should be selected from other students in your tutorial group. To register who is in your team, go to the Groups page on the unit’s MyLO site and select a group from the list. As in Assignment 1, group names incorporate the tutorial time. Include your group name (and your own names, too) in your application sources.

Your progress will be assessed, and feedback given, during your Week 11 tutorial. Additional details of this checkpoint will be provided after the mid‐semester break.

<h2>Deliverables</h2>

There are three deliverables in this assignment:

<ol>

 <li>a zipped VisualStudio project that contains the WPF‐based application that <em>must be submitted to the assignment folder</em>, accompanied by</li>

 <li>a <u>completed test report</u> in PDF, which must also <em>be submitted to the assignment folder</em>.</li>

 <li>The Visual Studio project and any precursor console application projects must be available <em>in your group’s SVN repository</em>.</li>

</ol>

<h1>The    starting       point for      developing the     application</h1>

A standard OO model for the system (some scenarios, all class diagrams and some sequence diagrams) will be released after the Assignment 1 due date, along with details of the database schema. You may then use your group members’ joint experience of developing their own OO models to determine the rest of your design. You may also deviate from the standard design as you see fit. This will give different development teams some freedom in their implementation choices.

<h2>OO      Model            versus           WPF</h2>

In the OO model each view is a separate class, which in WPF corresponds to defining a UserControl for each major view. Because this may complicate some of the event handling code, it is acceptable in the assignment to place separate views directly within the main window. Note, however, that the HD level of the <em>Use of WPF </em>assessment criterion requires that at least one user control be defined, and that defining your own controls will actually make each individual source file easier to manage.<strong>         </strong>

<strong>           </strong>

<h1>Development       approach</h1>

Because the final application requires knowledge of the C# language, how to communicate with a database using C# (and LINQ) and how to design and construct GUIs using WPF, and because these topics are to be covered over a period of some weeks, we recommend that you take a prototyping approach to the development of this application. This will allow you and your team to make useful progress on parts of the system even before you have obtained the skills required to implement the whole system. (Note that this will likely entail <em>some</em> manual copying of source files between projects as you migrate from a console application to a WPF application.) We suggest the following implementation stages (you may of course adopt a different development path if you find it suits your team better):

<table width="607">

 <tbody>

  <tr>

   <td width="48"><strong>Stage </strong></td>

   <td width="88"><strong>Timeframe </strong><strong>(semester week) </strong></td>

   <td width="235"><strong>Application type &amp; functionality </strong></td>

   <td width="237"><strong>Notes </strong></td>

  </tr>

  <tr>

   <td width="48"><strong>1 </strong></td>

   <td width="88">8–9</td>

   <td width="235">Console application with entity (data) classes, partially‐implemented control classes and at least one database adapter class.One or more driver classes containing Main() that can test features such as filtering of the staff or unit lists.</td>

   <td width="237">1.                   <em>May</em> have a GUI, but this should be no more than necessary to exercise/test implemented functionality (should be able to throw this GUI away later).2.                   Database adapter will need to return artificial data.</td>

  </tr>

  <tr>

   <td width="48"><strong>2 </strong></td>

   <td width="88">9–10</td>

   <td width="235">As above but using live data, which will substantially ease the burden on you to create artificial test data.Draft test cases that are complete in all details apart from test methods (which will likely still be high‐level until the GUI is built).</td>

   <td width="237">(1) as above</td>

  </tr>

  <tr>

   <td width="48"><strong>3 </strong></td>

   <td width="88">11–13</td>

   <td width="235">WPF application with custom controls for different views. Control classes updated to know about GUI components and event handlers connected.Test cases completed and applied to your application.</td>

   <td width="237">Transition will be easiest by creating a new WPF Application project andimporting the pre‐existing class files into it.</td>

  </tr>

 </tbody>

</table>

<h2>Use     of        SVN    source           control</h2>

You are required to use Subversion (SVN) source control for this project. We will create repositories for groups periodically based on the memberships shown on MyLO and notify you so you can check the list of teams with extant repositories. Commit information will be used to adjust your individual grade for this assignment.

We recommend that your repository (hence, your working directory) be a folder that contains one or more Visual Studio projects related to the assignment, one of which will be your final WPF‐based application. In this way you can use the repository to manage any early prototype console application projects as well, and we can see that team members have committed changes to those. If you need assistance with this please ask.

<strong>           </strong>

<h2>OO      Packages      and     C#       Namespaces</h2>

As C# applications have a top‐level namespace, which was not part of the OO Design, we recommend that each package in the OO Design becomes a nested namespace within your application’s top‐level namespace (which should be RAP). Note that the namespace and project name do not have to be the same, even though Visual Studio will initially make them the same.<strong>    </strong>

<h2>The     School           Database      (aka   RAP    Database)</h2>

The case study MySQL database is available via the following settings:

<strong>Database:</strong> kit206

<strong>User Id:</strong> kit206

<strong>Password:</strong> kit206

<strong>Data Source:</strong> alacritas.cis.utas.edu.au

You can also browse the data via <em>phpMyAdmin</em> (append that to the end of the server name). As the database is shared it will not appear in your own list of databases on alacritas if you log in under your own user name. An EER Diagram for the database plus some details on enumerated value columns accompanies this document.

<h3>Data     quality</h3>

The database is currently live and contains fictitious data. The data are consistent in that foreign key relationships are all valid, although initially there will not be much information in the database. More entries, or more realistic entries, may be added later in semester, but this is not guaranteed.

<h1>The    Testing        Report</h1>

Concurrently with development of the application you will create a test plan containing four test cases to verify the following subset of requirements in the RAP RTM:

<ul>

 <li>SWC 1</li>

 <li>UC8_User_views_ResearcherList</li>

 <li>UC16_User_selects_Researcher</li>

 <li>UC34_User_views_Publications</li>

</ul>

Each test case will be based on the <strong>Test Report Template</strong>, which is available on MyLO. Each test case that is based on a use case should include at least two <em>methods</em> by which the requirement will be tested. NTH features of use cases should also be tested and so will provide additional methods, even if they were not implemented; the quality of the test case will be assessed, not the one line outcome of whether it passes or not. The test cases for the SWC will likely need only one, brief method in order to be tested.

Ensure that all instructional entries (<em>Repeat the following box…</em>, <em>&lt;Extract the text…</em>, <em>Repeat Method and Outcome…</em>) and unused method–outcome rows are removed from your submitted test plan. The document should include a title and your team name on the first page; the first test case can start immediately below that.

When the application is complete, apply the test plan to it and record the outcome for each method. Remember that if the outcome is ‘fail’ then an explanation of when (which step) or how must also be recorded.

<strong>           </strong>

<h2>Sources         of        information             for      compiling     the      testing           plan</h2>

Follow the procedures described in <em>Module 5 Use case‐Based Testing</em> to derive the test cases for the indicated SWC and SW entries. The RTM will be your primary resource for identifying the criteria for each test case. The original requirements document may also provide some useful information. The structured scenarios you prepared during Assignment 1, in conjunction with the specific application being tested, will provide the basic structure of the testing methods in each test case, since they describe the user’s actions in each use case.

<h1>Assessment</h1>

The assessment criteria for the final submission are available in an accompanying document, in Excel and PDF formats.

Your progress will also be assessed during your week 11 tutorial, which will contribute up to 5% to your final grade in the unit. The assessment criteria for this check will be released after the midsemester break.

<h2>Peer   assessment</h2>

Peer assessment will be completed as part of the tutorial in week 13. You will have the opportunity to provide both qualitative and quantitative feedback on your teammates’ performance.

<h1>Revision     history</h1>

2017‐09‐12             Initial release

2017‐09‐15             Corrected Test Case requirements





