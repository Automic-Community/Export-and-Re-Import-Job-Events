*Export and Re-Import Job Events*
=============


Export/Import all Dollar Universe Job Event.
http://github.com/Automic-Community/Export-and-Re-Import-Job-Events

<!-- List of attached files -->
Contents of Solution Package:

						
								*Dollar_Universe-Events_Export_Import.zip
								
						


Documenation and Instructions
---

<div class="ipsType_textblock ipsPad_half description_content"><span><strong class="bbc">Description</strong></span><br />&nbsp;<br />This is a Perl script that can:
<ul class="bbc">
<li>Export all Dollar Universe Job Event to a file</li>
<li>Re-Import the job event from that file</li>
</ul>
&nbsp;<br /><span><strong class="bbc">Usage</strong></span>
<pre class="prettyprint lang-auto linenums:0 prettyprinted"><span class="typ">Expected</span><span class="pln"> arguments</span><span class="pun">:</span><span class="pln">

</span><span class="typ">To</span><span class="pln"> </span><span class="typ">Export</span><span class="pun">:</span><span class="pln">
&nbsp; &nbsp; &nbsp;</span><span class="pun">-</span><span class="kwd">export</span><span class="pln"> </span><span class="pun">&lt;</span><span class="pln">FILENAME</span><span class="pun">&gt;</span><span class="pln"> </span><span class="pun">&lt;</span><span class="pln">AREA</span><span class="pun">&gt;</span><span class="pln"> </span><span class="pun">&lt;</span><span class="pln">NODE</span><span class="pun">&gt;</span><span class="pln">

</span><span class="typ">To</span><span class="pln"> </span><span class="typ">Import</span><span class="pun">:</span><span class="pln">
&nbsp; &nbsp; </span><span class="pun">-</span><span class="kwd">import</span><span class="pln"> </span><span class="pun">&lt;</span><span class="pln">FILENAME</span><span class="pun">&gt;</span><span class="pln"> </span><span class="pun">&lt;</span><span class="pln">AREA</span><span class="pun">&gt;</span><span class="pln"> </span><span class="pun">&lt;</span><span class="pln">NODE</span><span class="pun">&gt;</span><span class="pln">

</span><span class="pun">&lt;</span><span class="pln">AREA</span><span class="pun">&gt;</span><span class="pln"> </span><span class="kwd">and</span><span class="pln"> </span><span class="pun">&lt;</span><span class="pln">NODENAME</span><span class="pun">&gt;</span><span class="pln"> are optional</span></pre>
&nbsp;<br /><strong class="bbc"><span>Goal</span></strong><br />&nbsp;<br />Such script can be used when the even file has to be reset. With this script, all events can be recreated after the uxrazfic.<br />&nbsp;<br />In that case the typical procedure would be:
<ul class="bbc">
<li>Export the event:&nbsp;</li>
</ul>
<pre class="prettyprint lang-auto linenums:0 prettyprinted"><span class="pln">perl&nbsp;du_events_export_import</span><span class="pun">.</span><span class="pln">pl </span><span class="pun">-</span><span class="kwd">export</span><span class="pln"> c</span><span class="pun">:</span><span class="pln">\event</span><span class="pun">.</span><span class="pln">txt</span></pre>
<ul class="bbc">
<li>Stop Dollar Univere</li>
<li>Backup the file data/exp/u_fmlp60.dta</li>
<li>Reset and do a reorganization of the event files</li>
</ul>
<pre class="prettyprint lang-auto linenums:0 prettyprinted"><span class="pln">uxrazfic u_fmlp60 X
unireorg</span></pre>
<ul class="bbc">
<li>Start Dollar Universe</li>
<li>Re-import the events</li>
</ul>
<pre class="prettyprint lang-auto linenums:0 prettyprinted"><span class="pln">perl&nbsp;du_events_export_import</span><span class="pun">.</span><span class="pln">pl </span><span class="pun">-</span><span class="kwd">import</span><span class="pln"> c</span><span class="pun">:</span><span class="pln">\event</span><span class="pun">.</span><span class="pln">txt<br /><br /></span></pre>
<p><strong class="title">Target environments:</strong> Windows, Unix, Linux</p>
<p><strong class="title">Prerequisites:</strong> Perl</p>
<pre class="prettyprint lang-auto linenums:0 prettyprinted"><span class="pln">&nbsp;</span></pre>
</div>

Copyright and License
---

Broadcom does not support, maintain or warrant Solutions, Templates, Actions and any other content published on the Community and is subject to Broadcom Community [Terms and Conditions](https://community.broadcom.com/termsandconditions)


Questions or Need Help? 
---
Join the [Automic Community Integrations](https://community.broadcom.com/communities/community-home?CommunityKey=83e49dd4-b93e-464a-a343-2bb1e51c13ec) to discuss this integration.
