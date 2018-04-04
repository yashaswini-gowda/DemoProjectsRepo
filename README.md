# DemoProjectsRepo
Demo projects repository for learning purpose
## Fake MHS

If a consuming application wants to use MessageActions that the MHS Simulator does not know about, then that action needs to be added in ActionRequestResponseMapping.xml underneath Mhs.Tool.Simulator. This will ensure that the correct MessageAction response is generated for each inbound MessageAction request. For example few lines of ActionRequestResponseMapping.xml are outlined below which contains requests and responses for a MessageAction.

'<messageActions>
  <requestResults>
    <messageAction>
      <request>QUPC_IN000006GB01</request>
      <response>REPC_IN000007GB01</response>
      <isAsync>true</isAsync>
    </messageAction>
	        .
	        .
	        .
  <requestResults>
  <requestMappings>
    <requestMapping>
      <originatingAction>QUPC_IN000006GB01</originatingAction>
      <asyncReplyAction>REPC_IN000007GB01</asyncReplyAction>
      <service>urn:nhs:names:services:cpisquery</service>
    </requestMapping>
	        .
	        .
	        .
  <requestMappings>
</messageActions>'
