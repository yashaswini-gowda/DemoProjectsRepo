# DemoProjectsRepo
Demo projects repository for learning purpose
## Fake MHS

If a consuming application wants to use MessageActions that the MHS Simulator does not know about, then that action needs to be added in ActionRequestResponseMapping.xml underneath Mhs.Tool.Simulator. This will ensure that the correct MessageAction response is generated for each inbound MessageAction request. For example few lines of ActionRequestResponseMapping.xml are outlined below which contains requests and responses for a MessageAction.

&lt;messageActions&gt; 
 &lt;requestResults&gt;
  &lt;messageAction&gt;
   &lt;request&gt;QUPC_IN000006GB01&lt;/request&gt;
   &lt;response>REPC_IN000007GB01&lt;/response&gt;
   &lt;isAsync>true&lt;/isAsync&gt;
  &lt;/messageAction&gt;
 &lt;/requestResults&gt;
&lt;/messageActions&gt;
