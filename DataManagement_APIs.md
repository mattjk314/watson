## Functions

<dl>
<dt><a href="#registerMultipleDevices">registerMultipleDevices(arryOfDevicesToBeAdded)</a></dt>
<dd><p>Register multiple new devices, each request can contain a maximum of 512KB.
The response body will contain the generated authentication tokens for all devices.
The caller of the method must make sure to record these tokens when processing
the response. The IBM Watson IoT Platform will not be able to retrieve lost authentication tokens</p>
</dd>
<dt><a href="#deleteMultipleDevices">deleteMultipleDevices(arryOfDevicesToBeDeleted)</a></dt>
<dd><p>Delete multiple devices, each request can contain a maximum of 512Kb</p>
</dd>
<dt><a href="#getPhysicalInterfaces">getPhysicalInterfaces(Refer)</a></dt>
<dd><p>returns the list of all of the draft physical interfaces that have been defined
for the organization in the Watson IoT Platform. Various query parameters can be
used to filter, sort and page through the list of draft physical interfaces that are returned.</p>
</dd>
<dt><a href="#addPhysicalInterface">addPhysicalInterface(name, description)</a></dt>
<dd><p>Creates a new draft physical interface for the organization in the Watson IoT Platform.</p>
</dd>
<dt><a href="#deletePhysicalInterface">deletePhysicalInterface(physicalInterfaceId)</a></dt>
<dd><p>Deletes the draft physical interface with the specified id from the organization in the Watson IoT Platform.</p>
</dd>
<dt><a href="#getPhysicalInterface">getPhysicalInterface(physicalInterfaceId)</a></dt>
<dd><p>Retrieve the draft physical interface with the specified id.</p>
</dd>
<dt><a href="#updatePhysicalInterface">updatePhysicalInterface(physicalInterfaceId, name, description)</a></dt>
<dd><p>Updates the draft physical interface with the specified id. The following properties can be updated:</p>
</dd>
<dt><a href="#getPhysicalInterfaceEventMapping">getPhysicalInterfaceEventMapping(physicalInterfaceId)</a></dt>
<dd><p>Retrieve the list of event mappings for the draft physical interface.
Event mappings are keyed off of the event id specified in the MQTT topic
that the inbound events are published to.</p>
</dd>
<dt><a href="#addPhysicalInterfaceEventMapping">addPhysicalInterfaceEventMapping(physicalInterfaceId, eventId, eventTypeId)</a></dt>
<dd><p>Maps an event id to a specific event type for the draft specified physical interface.</p>
</dd>
<dt><a href="#removePhysicalInterfaceEventMapping">removePhysicalInterfaceEventMapping(physicalInterfaceId, eventId)</a></dt>
<dd><p>Maps an event id to a specific event type for the draft specified physical interface.</p>
</dd>
<dt><a href="#getActivePhysicalInterfaces">getActivePhysicalInterfaces(Refer)</a></dt>
<dd><p>returns the list of all of the active physical interfaces that
have been defined for the organization in the Watson IoT Platform</p>
</dd>
<dt><a href="#getActivePhysicalInterface">getActivePhysicalInterface(physicalInterfaceId)</a></dt>
<dd><p>Retrieve the active physical interface with the specified id.</p>
</dd>
<dt><a href="#getActivePhysicalInterfaceEventMapping">getActivePhysicalInterfaceEventMapping(Refer)</a></dt>
<dd><p>Retrieve the list of event mappings for the active physical interface.
Event mappings are keyed off of the event id specified in the MQTT topic
that the inbound events are published to.</p>
</dd>
<dt><a href="#getLogicalInterfaces">getLogicalInterfaces(Refer)</a></dt>
<dd><p>returns the list of all of the draft logical interfaces that have been defined
for the organization in the Watson IoT Platform</p>
</dd>
<dt><a href="#addLogicalInterface">addLogicalInterface(name, description, schemaId)</a></dt>
<dd><p>Creates a new draft logical interface for the organization in the Watson IoT Platform.
The logical interface must reference a schema definition that defines the structure of
the state that will be stored for the device or thing.</p>
</dd>
<dt><a href="#deleteLogicalInterface">deleteLogicalInterface(logicalInterfaceId)</a></dt>
<dd><p>Deletes the draft logical interface with the specified id from the organization in the Watson IoT Platform.</p>
</dd>
<dt><a href="#getLogicalInterface">getLogicalInterface(logicalInterfaceId)</a></dt>
<dd><p>Retrieve the draft logical interface with the specified id.</p>
</dd>
<dt><a href="#updateLogicalInterface">updateLogicalInterface(logicalInterfaceId, name, description, schemaId)</a></dt>
<dd><p>Updates the draft logical interface with the specified id.</p>
</dd>
<dt><a href="#performOperationOnLogicalInterface">performOperationOnLogicalInterface(logicalInterfaceId, operationName)</a></dt>
<dd><p>Performs the specified operation against the draft logical interface. The following values can be specified for the operation property:</p>
<pre><code>1. validate-configuration
2. activate-configuration
3. list-differences
</code></pre></dd>
<dt><a href="#getActiveLogicalInterfaces">getActiveLogicalInterfaces(Refer)</a></dt>
<dd><p>returns the list of all of the active logical interfaces that have been defined
for the organization in the Watson IoT Platform</p>
</dd>
<dt><a href="#getActiveLogicalInterface">getActiveLogicalInterface(logicalInterfaceId)</a></dt>
<dd><p>Retrieve the active logical interface with the specified id.</p>
</dd>
<dt><a href="#performOperationOnActiveLogicalInterface">performOperationOnActiveLogicalInterface(logicalInterfaceId, operationName)</a></dt>
<dd><p>Performs the specified operation against the logical interface. The following values can be specified for the operation property:</p>
<pre><code>deactivate-configuration
</code></pre></dd>
<dt><a href="#getDraftSchemas">getDraftSchemas(Refer)</a></dt>
<dd><p>returns the list of all of the draft schema for the organization
in the Watson IoT Platform</p>
</dd>
<dt><a href="#addDraftSchema">addDraftSchema(name, schemaFilePath, description)</a></dt>
<dd><p>Creates a new draft schema definition for the organization in the Watson IoT Platform.</p>
</dd>
<dt><a href="#deleteDraftSchema">deleteDraftSchema(schemaId)</a></dt>
<dd><p>Deletes the draft schema with the specified id from the organization in the Watson IoT Platform.</p>
</dd>
<dt><a href="#getDraftSchema">getDraftSchema(schemaId)</a></dt>
<dd><p>Retrieves the metadata for the draft schema definition with the specified id.</p>
</dd>
<dt><a href="#updateDraftSchema">updateDraftSchema(schemaId, name, description)</a></dt>
<dd><p>Updates the metadata for the draft schema definition with the specified id. The following properties can be updated:</p>
<ol>
<li>name</li>
<li>description
Note that if the description field is omitted from the body of the update, then any existing description will be removed from the schema definition.</li>
</ol>
</dd>
<dt><a href="#getDraftSchemaContent">getDraftSchemaContent(schemaId)</a></dt>
<dd><p>Retrieves the content of the draft schema definition file with the specified id.</p>
</dd>
<dt><a href="#updateDraftSchemaContent">updateDraftSchemaContent(schemaId, schemaFilePath)</a></dt>
<dd><p>Updates the content of a draft schema definition file with the specified id.</p>
</dd>
<dt><a href="#getSchemas">getSchemas(Refer)</a></dt>
<dd><p>returns the list of all of the active schema definitions for the organization in the Watson IoT Platform
in the Watson IoT Platform</p>
</dd>
<dt><a href="#getSchema">getSchema(schemaId)</a></dt>
<dd><p>Retrieves the metadata for the active schema definition with the specified id.</p>
</dd>
<dt><a href="#getSchemaContent">getSchemaContent(schemaId)</a></dt>
<dd><p>Retrieves the content of the active schema definition file with the specified id.</p>
</dd>
<dt><a href="#getDeviceState">getDeviceState(schemaId)</a></dt>
<dd><p>Retrieve the current state of the device with the specified id.</p>
</dd>
<dt><a href="#getDraftEventTypes">getDraftEventTypes(Refer)</a></dt>
<dd><p>List of all of the draft event types that have been defined for the organization
in the Watson IoT Platform</p>
</dd>
<dt><a href="#addDraftEventTypes">addDraftEventTypes(name, description, schemaId)</a></dt>
<dd><p>Creates a new draft event type for the organization in the Watson IoT Platform.
    The draft event type must reference the schema definition that defines the structure
    of the inbound MQTT event.</p>
</dd>
<dt><a href="#deleteDraftEventTypes">deleteDraftEventTypes(eventTypeId)</a></dt>
<dd><p>Deletes the draft event type with the specified id from the organization in the Watson IoT Platform.</p>
</dd>
<dt><a href="#getDraftEventType">getDraftEventType(eventTypeId)</a></dt>
<dd><p>Retrieve the draft event type with the specified id.</p>
</dd>
<dt><a href="#updateDraftEventTypes">updateDraftEventTypes(eventTypeId, schemaId, name, description)</a></dt>
<dd><p>Updates the draft event type with the specified id. The following properties can be updated:
      name
      description
      schemaId
    Note that if the description field is omitted from the body of the update, then any existing description will be removed from the event type.</p>
</dd>
<dt><a href="#getActiveEventTypes">getActiveEventTypes(Refer)</a></dt>
<dd><p>list of all of the active event types that have been defined for the organization
in the Watson IoT Platform</p>
</dd>
<dt><a href="#getActiveEventType">getActiveEventType(eventTypeId)</a></dt>
<dd><p>Retrieve the active event type with the specified id.</p>
</dd>
<dt><a href="#performOperationOnDeviceType">performOperationOnDeviceType(typeId, operationName)</a></dt>
<dd><p>Performs the specified operation against the device type. The following values can be specified for the operation property:</p>
<pre><code> 1. deactivate-configuration
</code></pre></dd>
<dt><a href="#getLogicalInterfacesforDeviceType">getLogicalInterfacesforDeviceType(typeId)</a></dt>
<dd><p>Retrieve the list of active logical interfaces that have been associated with the device type.</p>
</dd>
<dt><a href="#getMappingsforDeviceType">getMappingsforDeviceType(typeId)</a></dt>
<dd><p>Retrieve the list of active property mappings for the specified device type.</p>
</dd>
<dt><a href="#getMappingsforLogicalInterfaceForDeviceType">getMappingsforLogicalInterfaceForDeviceType(typeId, logicalInterfaceId)</a></dt>
<dd><p>Retrieves the active property mappings for a specific logical interface for the device type.</p>
</dd>
<dt><a href="#getPhysicalInterfacesforDeviceType">getPhysicalInterfacesforDeviceType(typeId)</a></dt>
<dd><p>Retrieve the active physical interface that has been associated with the device type</p>
</dd>
<dt><a href="#getDraftDeviceTypes">getDraftDeviceTypes(logicalInterfaceId, physicalInterfaceId)</a></dt>
<dd><p>Retrieves the list of device types that are associated with the logical interface and/or physical interface with the ids specified using the corresponding query parameters.</p>
<pre><code>  Note that at least one of the following query parameters must be specified:

  logicalInterfaceId
  physicalInterfaceId
</code></pre></dd>
<dt><a href="#performOperationOnDeviceType">performOperationOnDeviceType(typeId)</a></dt>
<dd><p>Performs the specified operation against the draft device type. The following values can be specified for the operation property:</p>
<pre><code>  validate-configuration
  activate-configuration
  list-differences
</code></pre></dd>
<dt><a href="#getDraftLogicalInterfacesforDeviceType">getDraftLogicalInterfacesforDeviceType(typeId)</a></dt>
<dd><p>Retrieve the list of draft logical interfaces that have been associated with the device type. At least one
active logical interface must be associated with the device type before any mappings can be defined that will
generate state for the device.</p>
</dd>
<dt><a href="#associateLogicalInterfaceToDeviceType">associateLogicalInterfaceToDeviceType(typeId, logicalInterfaceBody)</a></dt>
<dd><p>Associates a draft logical interface with the specified device type. The draft logical
    interface must already exist within the organization in the Watson IoT Platform.</p>
</dd>
<dt><a href="#removeLogicalInterfaceFromDeviceType">removeLogicalInterfaceFromDeviceType(typeId, logicalInterfaceId)</a></dt>
<dd><p>Disassociates the draft logical interface with the specified id from the device type.</p>
</dd>
<dt><a href="#getMappingsforDeviceType">getMappingsforDeviceType(typeId)</a></dt>
<dd><p>Retrieve the list of draft property mappings for the specified device type.</p>
</dd>
<dt><a href="#addMappingsforDeviceType">addMappingsforDeviceType(typeId, mappingsBody)</a></dt>
<dd><p>Associates a draft logical interface with the specified device type. The draft logical
    interface must already exist within the organization in the Watson IoT Platform.</p>
</dd>
<dt><a href="#removeMappingsFromDeviceType">removeMappingsFromDeviceType(typeId, logicalInterfaceId)</a></dt>
<dd><p>Deletes the draft property mappings for a specific logical interface for the device type.</p>
</dd>
<dt><a href="#getMappingsforLogicalInterfaceForDeviceType">getMappingsforLogicalInterfaceForDeviceType(typeId, logicalInterfaceId)</a></dt>
<dd><p>Retrieves the draft property mappings for a specific logical interface for the device type.</p>
</dd>
<dt><a href="#updateMappingsforLogicalInterfaceForDeviceType">updateMappingsforLogicalInterfaceForDeviceType(typeId, logicalInterfaceId, mappingsBody)</a></dt>
<dd><p>Updates the draft property mappings for a specific logical interface for the device type.</p>
</dd>
<dt><a href="#getPhysicalInterfaceforDeviceType">getPhysicalInterfaceforDeviceType(typeId)</a></dt>
<dd><p>Retrieve the draft physical interface that has been associated with the device type.</p>
</dd>
<dt><a href="#addPhysicalInterfaceforDeviceType">addPhysicalInterfaceforDeviceType(typeId, physicalinterfaceBody)</a></dt>
<dd><p>Associates a draft physical interface with the specified device type.
    The draft physical interface must already exist within the organization in the Watson IoT Platform.</p>
</dd>
<dt><a href="#removePhysicalInterfaceFromDeviceType">removePhysicalInterfaceFromDeviceType(typeId)</a></dt>
<dd><p>Disassociates the draft physical interface from the device type.</p>
</dd>
</dl>

<a name="registerMultipleDevices"></a>

## registerMultipleDevices(arryOfDevicesToBeAdded)
Register multiple new devices, each request can contain a maximum of 512KB.
The response body will contain the generated authentication tokens for all devices.
The caller of the method must make sure to record these tokens when processing
the response. The IBM Watson IoT Platform will not be able to retrieve lost authentication tokens

**Kind**: global function  

| Param | Description |
| --- | --- |
| arryOfDevicesToBeAdded | Array of JSON devices to be added. Refer to <a href="https://docs.internetofthings.ibmcloud.com/swagger/v0002.html#!/Bulk_Operations/post_bulk_devices_add">link</a> for more information about the schema to be used |

<a name="deleteMultipleDevices"></a>

## deleteMultipleDevices(arryOfDevicesToBeDeleted)
Delete multiple devices, each request can contain a maximum of 512Kb

**Kind**: global function  

| Param | Description |
| --- | --- |
| arryOfDevicesToBeDeleted | Array of JSON devices to be deleted. Refer to <a href="https://docs.internetofthings.ibmcloud.com/swagger/v0002.html#!/Bulk_Operations/post_bulk_devices_remove">link</a> for more information about the schema to be used. |

<a name="getPhysicalInterfaces"></a>

## getPhysicalInterfaces(Refer)
returns the list of all of the draft physical interfaces that have been defined
for the organization in the Watson IoT Platform. Various query parameters can be
used to filter, sort and page through the list of draft physical interfaces that are returned.

**Kind**: global function  

| Param | Description |
| --- | --- |
| Refer | to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Physical_Interfaces/get_draft_physicalinterfaces">link</a> |

<a name="addPhysicalInterface"></a>

## addPhysicalInterface(name, description)
Creates a new draft physical interface for the organization in the Watson IoT Platform.

**Kind**: global function  

| Param | Description |
| --- | --- |
| name | Name of the physical interface |
| description | Description of the physical interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Physical_Interfaces/get_draft_physicalinterfaces">link</a> |

<a name="deletePhysicalInterface"></a>

## deletePhysicalInterface(physicalInterfaceId)
Deletes the draft physical interface with the specified id from the organization in the Watson IoT Platform.

**Kind**: global function  

| Param | Description |
| --- | --- |
| physicalInterfaceId | Id of the physical interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Physical_Interfaces/get_draft_physicalinterfaces">link</a> |

<a name="getPhysicalInterface"></a>

## getPhysicalInterface(physicalInterfaceId)
Retrieve the draft physical interface with the specified id.

**Kind**: global function  

| Param | Description |
| --- | --- |
| physicalInterfaceId | Id of the physical interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Physical_Interfaces/get_draft_physicalinterfaces_physicalInterfaceId">link</a> |

<a name="updatePhysicalInterface"></a>

## updatePhysicalInterface(physicalInterfaceId, name, description)
Updates the draft physical interface with the specified id. The following properties can be updated:

**Kind**: global function  

| Param | Description |
| --- | --- |
| physicalInterfaceId | Id of the physical interface |
| name | Updated name of the physical interface |
| description | Updated Description of the physical interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Physical_Interfaces/get_draft_physicalinterfaces_physicalInterfaceId">link</a> |

<a name="getPhysicalInterfaceEventMapping"></a>

## getPhysicalInterfaceEventMapping(physicalInterfaceId)
Retrieve the list of event mappings for the draft physical interface.
Event mappings are keyed off of the event id specified in the MQTT topic
that the inbound events are published to.

**Kind**: global function  

| Param | Description |
| --- | --- |
| physicalInterfaceId | Id of the physical interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Physical_Interfaces/get_draft_physicalinterfaces_physicalInterfaceId">link</a> |

<a name="addPhysicalInterfaceEventMapping"></a>

## addPhysicalInterfaceEventMapping(physicalInterfaceId, eventId, eventTypeId)
Maps an event id to a specific event type for the draft specified physical interface.

**Kind**: global function  

| Param | Description |
| --- | --- |
| physicalInterfaceId | Id of the physical interface |
| eventId | Event ID |
| eventTypeId | Event Type ID Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Physical_Interfaces/post_draft_physicalinterfaces_physicalInterfaceId_events">link</a> |

<a name="removePhysicalInterfaceEventMapping"></a>

## removePhysicalInterfaceEventMapping(physicalInterfaceId, eventId)
Maps an event id to a specific event type for the draft specified physical interface.

**Kind**: global function  

| Param | Description |
| --- | --- |
| physicalInterfaceId | Id of the physical interface |
| eventId | Event ID Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Physical_Interfaces/delete_draft_physicalinterfaces_physicalInterfaceId_events_eventId">link</a> |

<a name="getActivePhysicalInterfaces"></a>

## getActivePhysicalInterfaces(Refer)
returns the list of all of the active physical interfaces that
have been defined for the organization in the Watson IoT Platform

**Kind**: global function  

| Param | Description |
| --- | --- |
| Refer | to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Physical_Interfaces/get_physicalinterfaces">link</a> |

<a name="getActivePhysicalInterface"></a>

## getActivePhysicalInterface(physicalInterfaceId)
Retrieve the active physical interface with the specified id.

**Kind**: global function  

| Param | Description |
| --- | --- |
| physicalInterfaceId | Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Physical_Interfaces/get_physicalinterfaces_physicalInterfaceId">link</a> |

<a name="getActivePhysicalInterfaceEventMapping"></a>

## getActivePhysicalInterfaceEventMapping(Refer)
Retrieve the list of event mappings for the active physical interface.
Event mappings are keyed off of the event id specified in the MQTT topic
that the inbound events are published to.

**Kind**: global function  

| Param | Description |
| --- | --- |
| Refer | to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Physical_Interfaces/get_physicalinterfaces_physicalInterfaceId_events">link</a> |

<a name="getLogicalInterfaces"></a>

## getLogicalInterfaces(Refer)
returns the list of all of the draft logical interfaces that have been defined
for the organization in the Watson IoT Platform

**Kind**: global function  

| Param | Description |
| --- | --- |
| Refer | to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Logical_Interfaces/get_draft_logicalinterfaces">link</a> |

<a name="addLogicalInterface"></a>

## addLogicalInterface(name, description, schemaId)
Creates a new draft logical interface for the organization in the Watson IoT Platform.
The logical interface must reference a schema definition that defines the structure of
the state that will be stored for the device or thing.

**Kind**: global function  

| Param | Description |
| --- | --- |
| name | Name of the Logical Interface |
| description | Description of the Logical Interface |
| schemaId | Schema ID for the Logical Interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Logical_Interfaces/post_draft_logicalinterfaces">link</a> |

<a name="deleteLogicalInterface"></a>

## deleteLogicalInterface(logicalInterfaceId)
Deletes the draft logical interface with the specified id from the organization in the Watson IoT Platform.

**Kind**: global function  

| Param | Description |
| --- | --- |
| logicalInterfaceId | Id of the Logical interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Logical_Interfaces/delete_draft_logicalinterfaces_logicalInterfaceId">link</a> |

<a name="getLogicalInterface"></a>

## getLogicalInterface(logicalInterfaceId)
Retrieve the draft logical interface with the specified id.

**Kind**: global function  

| Param | Description |
| --- | --- |
| logicalInterfaceId | Id of the Logical interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Logical_Interfaces/get_draft_logicalinterfaces_logicalInterfaceId">link</a> |

<a name="updateLogicalInterface"></a>

## updateLogicalInterface(logicalInterfaceId, name, description, schemaId)
Updates the draft logical interface with the specified id.

**Kind**: global function  

| Param | Description |
| --- | --- |
| logicalInterfaceId | Id of the Logical interface |
| name | Name of the Logical Interface |
| description | Description of the Logical Interface |
| schemaId | Schema ID for the Logical Interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Logical_Interfaces/put_draft_logicalinterfaces_logicalInterfaceId">link</a> |

<a name="performOperationOnLogicalInterface"></a>

## performOperationOnLogicalInterface(logicalInterfaceId, operationName)
Performs the specified operation against the draft logical interface. The following values can be specified for the operation property:

    1. validate-configuration
    2. activate-configuration
    3. list-differences

**Kind**: global function  

| Param | Description |
| --- | --- |
| logicalInterfaceId | Id of the Logical interface |
| operationName | Name of the operation Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Logical_Interfaces/patch_draft_logicalinterfaces_logicalInterfaceId">link</a> |

<a name="getActiveLogicalInterfaces"></a>

## getActiveLogicalInterfaces(Refer)
returns the list of all of the active logical interfaces that have been defined
for the organization in the Watson IoT Platform

**Kind**: global function  

| Param | Description |
| --- | --- |
| Refer | to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Logical_Interfaces/get_logicalinterfaces">link</a> |

<a name="getActiveLogicalInterface"></a>

## getActiveLogicalInterface(logicalInterfaceId)
Retrieve the active logical interface with the specified id.

**Kind**: global function  

| Param | Description |
| --- | --- |
| logicalInterfaceId | Id of the Logical interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Logical_Interfaces/get_logicalinterfaces_logicalInterfaceId">link</a> |

<a name="performOperationOnActiveLogicalInterface"></a>

## performOperationOnActiveLogicalInterface(logicalInterfaceId, operationName)
Performs the specified operation against the logical interface. The following values can be specified for the operation property:

    deactivate-configuration

**Kind**: global function  

| Param | Description |
| --- | --- |
| logicalInterfaceId | Id of the Logical interface |
| operationName | Name of the operation Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Logical_Interfaces/get_logicalinterfaces_logicalInterfaceId">link</a> |

<a name="getDraftSchemas"></a>

## getDraftSchemas(Refer)
returns the list of all of the draft schema for the organization
in the Watson IoT Platform

**Kind**: global function  

| Param | Description |
| --- | --- |
| Refer | to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Schemas/get_draft_schemas">link</a> |

<a name="addDraftSchema"></a>

## addDraftSchema(name, schemaFilePath, description)
Creates a new draft schema definition for the organization in the Watson IoT Platform.

**Kind**: global function  

| Param | Description |
| --- | --- |
| name | name of the schema |
| schemaFilePath | path of the schema file |
| description | description of the schema Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Schemas/post_draft_schemas">link</a> |

<a name="deleteDraftSchema"></a>

## deleteDraftSchema(schemaId)
Deletes the draft schema with the specified id from the organization in the Watson IoT Platform.

**Kind**: global function  

| Param | Description |
| --- | --- |
| schemaId | Id of the schema Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Schemas/delete_draft_schemas_schemaId">link</a> |

<a name="getDraftSchema"></a>

## getDraftSchema(schemaId)
Retrieves the metadata for the draft schema definition with the specified id.

**Kind**: global function  

| Param | Description |
| --- | --- |
| schemaId | schemaId Id of the schema Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Schemas/get_draft_schemas_schemaId">link</a> |

<a name="updateDraftSchema"></a>

## updateDraftSchema(schemaId, name, description)
Updates the metadata for the draft schema definition with the specified id. The following properties can be updated:
1. name
2. description
 Note that if the description field is omitted from the body of the update, then any existing description will be removed from the schema definition.

**Kind**: global function  

| Param | Description |
| --- | --- |
| schemaId | Id of the schema |
| name | Name of the schema |
| description | description of the schema Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Schemas/put_draft_schemas_schemaId">link</a> |

<a name="getDraftSchemaContent"></a>

## getDraftSchemaContent(schemaId)
Retrieves the content of the draft schema definition file with the specified id.

**Kind**: global function  

| Param | Description |
| --- | --- |
| schemaId | Id of the schema Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Schemas/get_draft_schemas_schemaId_content">link</a> |

<a name="updateDraftSchemaContent"></a>

## updateDraftSchemaContent(schemaId, schemaFilePath)
Updates the content of a draft schema definition file with the specified id.

**Kind**: global function  

| Param | Description |
| --- | --- |
| schemaId | Id of the schema |
| schemaFilePath | path of the schema file Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Schemas/get_draft_schemas_schemaId_content">link</a> |

<a name="getSchemas"></a>

## getSchemas(Refer)
returns the list of all of the active schema definitions for the organization in the Watson IoT Platform
in the Watson IoT Platform

**Kind**: global function  

| Param | Description |
| --- | --- |
| Refer | to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Schemas/get_schemas">link</a> |

<a name="getSchema"></a>

## getSchema(schemaId)
Retrieves the metadata for the active schema definition with the specified id.

**Kind**: global function  

| Param | Description |
| --- | --- |
| schemaId | schemaId Id of the schema Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Schemas/get_schemas_schemaId">link</a> |

<a name="getSchemaContent"></a>

## getSchemaContent(schemaId)
Retrieves the content of the active schema definition file with the specified id.

**Kind**: global function  

| Param | Description |
| --- | --- |
| schemaId | Id of the schema Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Schemas/get_schemas_schemaId_content">link</a> |

<a name="getDeviceState"></a>

## getDeviceState(schemaId)
Retrieve the current state of the device with the specified id.

**Kind**: global function  

| Param | Description |
| --- | --- |
| schemaId | Id of the schema Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Devices/get_device_types_typeId_devices_deviceId_state_logicalInterfaceId">link</a> |

<a name="getDraftEventTypes"></a>

## getDraftEventTypes(Refer)
List of all of the draft event types that have been defined for the organization
in the Watson IoT Platform

**Kind**: global function  

| Param | Description |
| --- | --- |
| Refer | to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Event_Types/get_draft_event_types">link</a> |

<a name="addDraftEventTypes"></a>

## addDraftEventTypes(name, description, schemaId)
Creates a new draft event type for the organization in the Watson IoT Platform.
    The draft event type must reference the schema definition that defines the structure
    of the inbound MQTT event.

**Kind**: global function  

| Param | Description |
| --- | --- |
| name | Name of the event type |
| description | description of the event type |
| schemaId | Id of the schema Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Event_Types/post_draft_event_types">link</a> |

<a name="deleteDraftEventTypes"></a>

## deleteDraftEventTypes(eventTypeId)
Deletes the draft event type with the specified id from the organization in the Watson IoT Platform.

**Kind**: global function  

| Param | Description |
| --- | --- |
| eventTypeId | Id of the event type Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Event_Types/delete_draft_event_types_eventTypeId">link</a> |

<a name="getDraftEventType"></a>

## getDraftEventType(eventTypeId)
Retrieve the draft event type with the specified id.

**Kind**: global function  

| Param | Description |
| --- | --- |
| eventTypeId | Id of the event type Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Event_Types/get_draft_event_types_eventTypeId">link</a> |

<a name="updateDraftEventTypes"></a>

## updateDraftEventTypes(eventTypeId, schemaId, name, description)
Updates the draft event type with the specified id. The following properties can be updated:
      name
      description
      schemaId
    Note that if the description field is omitted from the body of the update, then any existing description will be removed from the event type.

**Kind**: global function  

| Param | Description |
| --- | --- |
| eventTypeId | Id of the event type |
| schemaId | Id of the schema |
| name | Name of the schema |
| description | description of the schema Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Event_Types/put_draft_event_types_eventTypeId">link</a> |

<a name="getActiveEventTypes"></a>

## getActiveEventTypes(Refer)
list of all of the active event types that have been defined for the organization
in the Watson IoT Platform

**Kind**: global function  

| Param | Description |
| --- | --- |
| Refer | to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Event_Types/get_event_types">link</a> |

<a name="getActiveEventType"></a>

## getActiveEventType(eventTypeId)
Retrieve the active event type with the specified id.

**Kind**: global function  

| Param | Description |
| --- | --- |
| eventTypeId | Id of the event type Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Event_Types/get_draft_event_types_eventTypeId">link</a> |

<a name="performOperationOnDeviceType"></a>

## performOperationOnDeviceType(typeId, operationName)
Performs the specified operation against the device type. The following values can be specified for the operation property:

     1. deactivate-configuration

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the Device Type |
| operationName | Name of the operation Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Device_Types/patch_device_types_typeId">link</a> |

<a name="getLogicalInterfacesforDeviceType"></a>

## getLogicalInterfacesforDeviceType(typeId)
Retrieve the list of active logical interfaces that have been associated with the device type.

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Device_Types/get_device_types_typeId_logicalinterfaces">link</a> |

<a name="getMappingsforDeviceType"></a>

## getMappingsforDeviceType(typeId)
Retrieve the list of active property mappings for the specified device type.

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Device_Types/get_device_types_typeId_mappings">link</a> |

<a name="getMappingsforLogicalInterfaceForDeviceType"></a>

## getMappingsforLogicalInterfaceForDeviceType(typeId, logicalInterfaceId)
Retrieves the active property mappings for a specific logical interface for the device type.

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type |
| logicalInterfaceId | ID for logical interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Device_Types/get_device_types_typeId_mappings_logicalInterfaceId">link</a> |

<a name="getPhysicalInterfacesforDeviceType"></a>

## getPhysicalInterfacesforDeviceType(typeId)
Retrieve the active physical interface that has been associated with the device type

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html?cm_mc_uid=95177996809014882617847&cm_mc_sid_50200000=1502710506#!/Device_Types/get_device_types_typeId_physicalinterface">link</a> |

<a name="getDraftDeviceTypes"></a>

## getDraftDeviceTypes(logicalInterfaceId, physicalInterfaceId)
Retrieves the list of device types that are associated with the logical interface and/or physical interface with the ids specified using the corresponding query parameters.

      Note that at least one of the following query parameters must be specified:

      logicalInterfaceId
      physicalInterfaceId

**Kind**: global function  

| Param | Description |
| --- | --- |
| logicalInterfaceId | ID for logical interface |
| physicalInterfaceId | Id for physical interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Device_Types/get_draft_device_types">link</a> |

<a name="performOperationOnDeviceType"></a>

## performOperationOnDeviceType(typeId)
Performs the specified operation against the draft device type. The following values can be specified for the operation property:

      validate-configuration
      activate-configuration
      list-differences

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Device_Types/patch_draft_device_types_typeId">link</a> |

<a name="getDraftLogicalInterfacesforDeviceType"></a>

## getDraftLogicalInterfacesforDeviceType(typeId)
Retrieve the list of draft logical interfaces that have been associated with the device type. At least one
active logical interface must be associated with the device type before any mappings can be defined that will
generate state for the device.

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Device_Types/get_draft_device_types_typeId_logicalinterfaces">link</a> |

<a name="associateLogicalInterfaceToDeviceType"></a>

## associateLogicalInterfaceToDeviceType(typeId, logicalInterfaceBody)
Associates a draft logical interface with the specified device type. The draft logical
    interface must already exist within the organization in the Watson IoT Platform.

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type |
| logicalInterfaceBody | JSON representation of the draft logical interface. Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Device_Types/post_draft_device_types_typeId_logicalinterfaces">link</a> |

<a name="removeLogicalInterfaceFromDeviceType"></a>

## removeLogicalInterfaceFromDeviceType(typeId, logicalInterfaceId)
Disassociates the draft logical interface with the specified id from the device type.

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type |
| logicalInterfaceId | ID for logical interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Device_Types/delete_draft_device_types_typeId_logicalinterfaces_logicalInterfaceId">link</a> |

<a name="getMappingsforDeviceType"></a>

## getMappingsforDeviceType(typeId)
Retrieve the list of draft property mappings for the specified device type.

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Device_Types/get_draft_device_types_typeId_mappings">link</a> |

<a name="addMappingsforDeviceType"></a>

## addMappingsforDeviceType(typeId, mappingsBody)
Associates a draft logical interface with the specified device type. The draft logical
    interface must already exist within the organization in the Watson IoT Platform.

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type |
| mappingsBody | The JSON representation of the draft device type property mappings. Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Device_Types/post_draft_device_types_typeId_logicalinterfaces">link</a> |

<a name="removeMappingsFromDeviceType"></a>

## removeMappingsFromDeviceType(typeId, logicalInterfaceId)
Deletes the draft property mappings for a specific logical interface for the device type.

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type |
| logicalInterfaceId | ID for logical interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Device_Types/delete_draft_device_types_typeId_logicalinterfaces_logicalInterfaceId">link</a> |

<a name="getMappingsforLogicalInterfaceForDeviceType"></a>

## getMappingsforLogicalInterfaceForDeviceType(typeId, logicalInterfaceId)
Retrieves the draft property mappings for a specific logical interface for the device type.

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type |
| logicalInterfaceId | ID for logical interface Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Device_Types/get_draft_device_types_typeId_mappings_logicalInterfaceId">link</a> |

<a name="updateMappingsforLogicalInterfaceForDeviceType"></a>

## updateMappingsforLogicalInterfaceForDeviceType(typeId, logicalInterfaceId, mappingsBody)
Updates the draft property mappings for a specific logical interface for the device type.

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type |
| logicalInterfaceId | ID for logical interface |
| mappingsBody | The JSON representation of the draft device type property mappings. Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Device_Types/put_draft_device_types_typeId_mappings_logicalInterfaceId">link</a> |

<a name="getPhysicalInterfaceforDeviceType"></a>

## getPhysicalInterfaceforDeviceType(typeId)
Retrieve the draft physical interface that has been associated with the device type.

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Device_Types/get_draft_device_types_typeId_physicalinterface">link</a> |

<a name="addPhysicalInterfaceforDeviceType"></a>

## addPhysicalInterfaceforDeviceType(typeId, physicalinterfaceBody)
Associates a draft physical interface with the specified device type.
    The draft physical interface must already exist within the organization in the Watson IoT Platform.

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type |
| physicalinterfaceBody | The JSON representation of the draft physical interface. Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Device_Types/post_draft_device_types_typeId_physicalinterface">link</a> |

<a name="removePhysicalInterfaceFromDeviceType"></a>

## removePhysicalInterfaceFromDeviceType(typeId)
Disassociates the draft physical interface from the device type.

**Kind**: global function  

| Param | Description |
| --- | --- |
| typeId | Id of the device type Refer to <a href="https://docs.internetofthings.ibmcloud.com/apis/swagger/v0002/state-mgmt.html#!/Device_Types/delete_draft_device_types_typeId_physicalinterface">link</a> |

