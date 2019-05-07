# ![LOGO](logo.png) Face Client **flow**ground Connector

## Description

A generated **flow**ground connector for the Face Client API (version 1.0).

Generated from: https://api.apis.guru/v2/specs/azure.com/cognitiveservices-Face/1.0/swagger.json<br/>
Generated at: 2019-05-07T17:37:44+03:00

## API Description

An API for face detection, verification, and identification.

## Authorization

Supported authorization schemes:
- API Key
## Actions

### Detect human faces in an image and returns face locations, and optionally with faceIds, landmarks, and attributes.

#### Input Parameters
* `returnFaceId` - _optional_ - A value indicating whether the operation should return faceIds of detected faces.
* `returnFaceLandmarks` - _optional_ - A value indicating whether the operation should return landmarks of the detected faces.
* `returnFaceAttributes` - _optional_ - Analyze and return the one or more specified face attributes in the comma-separated string like "returnFaceAttributes=age,gender". Supported face attributes include age, gender, headPose, smile, facialHair, glasses and emotion. Note that each face attribute analysis has additional computational and time cost.

### Retrieve information about all existing face lists. Only faceListId, name and userData will be returned.

### Delete an existing face list according to faceListId. Persisted face images in the face list will also be deleted.

#### Input Parameters
* `faceListId` - _required_ - Id referencing a particular face list.

### Retrieve a face list's information.

#### Input Parameters
* `faceListId` - _required_ - Id referencing a particular face list.

### Update information of a face list.

#### Input Parameters
* `faceListId` - _required_ - Id referencing a particular face list.

### Create an empty face list. Up to 64 face lists are allowed to exist in one subscription.

#### Input Parameters
* `faceListId` - _required_ - Id referencing a particular face list.

### Add a face to a face list. The input face is specified as an image with a targetFace rectangle. It returns a persistedFaceId representing the added face, and persistedFaceId will not expire.

#### Input Parameters
* `faceListId` - _required_ - Id referencing a particular face list.
* `userData` - _optional_ - User-specified data about the face for any purpose. The maximum length is 1KB.
* `targetFace` - _optional_ - A face rectangle to specify the target face to be added to a person in the format of "targetFace=left,top,width,height". E.g. "targetFace=10,10,100,100". If there is more than one face in the image, targetFace is required to specify which face to add. No targetFace means there is only one face detected in the entire image.

### Delete an existing face from a face list (given by a persistedFaceId and a faceListId). Persisted image related to the face will also be deleted.

#### Input Parameters
* `faceListId` - _required_ - Id referencing a particular face list.
* `persistedFaceId` - _required_ - Id referencing a particular persistedFaceId of an existing face.

### Given query face's faceId, find the similar-looking faces from a faceId array, a face list or a large face list.

### Divide candidate faces into groups based on face similarity.

### 1-to-many identification to find the closest matches of the specific query person face from a person group or large person group.

### Retrieve information about all existing large face lists. Only largeFaceListId, name and userData will be returned.

### Delete an existing large face list according to faceListId. Persisted face images in the large face list will also be deleted.

#### Input Parameters
* `largeFaceListId` - _required_ - Id referencing a particular large face list.

### Retrieve a large face list's information.

#### Input Parameters
* `largeFaceListId` - _required_ - Id referencing a particular large face list.

### Update information of a large face list.

#### Input Parameters
* `largeFaceListId` - _required_ - Id referencing a particular large face list.

### Create an empty large face list. Up to 64 large face lists are allowed to exist in one subscription.

#### Input Parameters
* `largeFaceListId` - _required_ - Id referencing a particular large face list.

### List all faces in a large face list, and retrieve face information (including userData and persistedFaceIds of registered faces of the face).

#### Input Parameters
* `largeFaceListId` - _required_ - Id referencing a particular large face list.
* `start` - _optional_ - Starting face id to return (used to list a range of faces).
* `top` - _optional_ - Number of faces to return starting with the face id indicated by the 'start' parameter.

### Add a face to a large face list. The input face is specified as an image with a targetFace rectangle. It returns a persistedFaceId representing the added face, and persistedFaceId will not expire.

#### Input Parameters
* `largeFaceListId` - _required_ - Id referencing a particular large face list.
* `userData` - _optional_ - User-specified data about the face for any purpose. The maximum length is 1KB.
* `targetFace` - _optional_ - A face rectangle to specify the target face to be added to a person in the format of "targetFace=left,top,width,height". E.g. "targetFace=10,10,100,100". If there is more than one face in the image, targetFace is required to specify which face to add. No targetFace means there is only one face detected in the entire image.

### Delete an existing face from a large face list (given by a persistedFaceId and a largeFaceListId). Persisted image related to the face will also be deleted.

#### Input Parameters
* `largeFaceListId` - _required_ - Id referencing a particular large face list.
* `persistedFaceId` - _required_ - Id referencing a particular persistedFaceId of an existing face.

### Retrieve information about a persisted face (specified by persistedFaceId and its belonging largeFaceListId).

#### Input Parameters
* `largeFaceListId` - _required_ - Id referencing a particular large face list.
* `persistedFaceId` - _required_ - Id referencing a particular persistedFaceId of an existing face.

### Update a persisted face's userData field.

#### Input Parameters
* `largeFaceListId` - _required_ - Id referencing a particular large face list.
* `persistedFaceId` - _required_ - Id referencing a particular persistedFaceId of an existing face.

### Queue a large face list training task, the training task may not be started immediately.

#### Input Parameters
* `largeFaceListId` - _required_ - Id referencing a particular large face list.

### Retrieve the training status of a large face list (completed or ongoing).

#### Input Parameters
* `largeFaceListId` - _required_ - Id referencing a particular large face list.

### List large person groups and their information.

#### Input Parameters
* `start` - _optional_ - List large person groups from the least largePersonGroupId greater than the "start".
* `top` - _optional_ - The number of large person groups to list.

### Delete an existing large person group. Persisted face features of all people in the large person group will also be deleted.

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.

### Retrieve the information of a large person group, including its name and userData.

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.

### Update an existing large person group's display name and userData. The properties which does not appear in request body will not be updated.

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.

### Create a new large person group with specified largePersonGroupId, name and user-provided userData.

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.

### List all persons in a large person group, and retrieve person information (including personId, name, userData and persistedFaceIds of registered faces of the person).

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.
* `start` - _optional_ - Starting person id to return (used to list a range of persons).
* `top` - _optional_ - Number of persons to return starting with the person id indicated by the 'start' parameter.

### Create a new person in a specified large person group.

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.

### Delete an existing person from a large person group. All stored person data, and face features in the person entry will be deleted.

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.
* `personId` - _required_ - Id referencing a particular person.

### Retrieve a person's information, including registered persisted faces, name and userData.

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.
* `personId` - _required_ - Id referencing a particular person.

### Update name or userData of a person.

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.
* `personId` - _required_ - Id referencing a particular person.

### Add a representative face to a person for identification. The input face is specified as an image with a targetFace rectangle.

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.
* `personId` - _required_ - Id referencing a particular person.
* `userData` - _optional_ - User-specified data about the face for any purpose. The maximum length is 1KB.
* `targetFace` - _optional_ - A face rectangle to specify the target face to be added to a person in the format of "targetFace=left,top,width,height". E.g. "targetFace=10,10,100,100". If there is more than one face in the image, targetFace is required to specify which face to add. No targetFace means there is only one face detected in the entire image.

### Delete a face from a person. Relative feature for the persisted face will also be deleted.

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.
* `personId` - _required_ - Id referencing a particular person.
* `persistedFaceId` - _required_ - Id referencing a particular persistedFaceId of an existing face.

### Retrieve information about a persisted face (specified by persistedFaceId, personId and its belonging largePersonGroupId).

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.
* `personId` - _required_ - Id referencing a particular person.
* `persistedFaceId` - _required_ - Id referencing a particular persistedFaceId of an existing face.

### Update a person persisted face's userData field.

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.
* `personId` - _required_ - Id referencing a particular person.
* `persistedFaceId` - _required_ - Id referencing a particular persistedFaceId of an existing face.

### Queue a large person group training task, the training task may not be started immediately.

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.

### Retrieve the training status of a large person group (completed or ongoing).

#### Input Parameters
* `largePersonGroupId` - _required_ - Id referencing a particular large person group.

### Retrieve the status of a take/apply snapshot operation.

#### Input Parameters
* `operationId` - _required_ - Id referencing a particular take/apply snapshot operation.

### List person groups and their information.

#### Input Parameters
* `start` - _optional_ - List person groups from the least personGroupId greater than the "start".
* `top` - _optional_ - The number of person groups to list.

### Delete an existing person group. Persisted face features of all people in the person group will also be deleted.

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.

### Retrieve the information of a person group, including its name and userData.

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.

### Update an existing person group's display name and userData. The properties which does not appear in request body will not be updated.

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.

### Create a new person group with specified personGroupId, name and user-provided userData.

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.

### List all persons in a person group, and retrieve person information (including personId, name, userData and persistedFaceIds of registered faces of the person).

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.
* `start` - _optional_ - Starting person id to return (used to list a range of persons).
* `top` - _optional_ - Number of persons to return starting with the person id indicated by the 'start' parameter.

### Create a new person in a specified person group.

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.

### Delete an existing person from a person group. All stored person data, and face features in the person entry will be deleted.

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.
* `personId` - _required_ - Id referencing a particular person.

### Retrieve a person's information, including registered persisted faces, name and userData.

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.
* `personId` - _required_ - Id referencing a particular person.

### Update name or userData of a person.

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.
* `personId` - _required_ - Id referencing a particular person.

### Add a representative face to a person for identification. The input face is specified as an image with a targetFace rectangle.

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.
* `personId` - _required_ - Id referencing a particular person.
* `userData` - _optional_ - User-specified data about the face for any purpose. The maximum length is 1KB.
* `targetFace` - _optional_ - A face rectangle to specify the target face to be added to a person in the format of "targetFace=left,top,width,height". E.g. "targetFace=10,10,100,100". If there is more than one face in the image, targetFace is required to specify which face to add. No targetFace means there is only one face detected in the entire image.

### Delete a face from a person. Relative feature for the persisted face will also be deleted.

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.
* `personId` - _required_ - Id referencing a particular person.
* `persistedFaceId` - _required_ - Id referencing a particular persistedFaceId of an existing face.

### Retrieve information about a persisted face (specified by persistedFaceId, personId and its belonging personGroupId).

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.
* `personId` - _required_ - Id referencing a particular person.
* `persistedFaceId` - _required_ - Id referencing a particular persistedFaceId of an existing face.

### Update a person persisted face's userData field.

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.
* `personId` - _required_ - Id referencing a particular person.
* `persistedFaceId` - _required_ - Id referencing a particular persistedFaceId of an existing face.

### Queue a person group training task, the training task may not be started immediately.

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.

### Retrieve the training status of a person group (completed or ongoing).

#### Input Parameters
* `personGroupId` - _required_ - Id referencing a particular person group.

### List all accessible snapshots with related information, including snapshots that were taken by the user, or snapshots to be applied to the user (subscription id was included in the applyScope in Snapshot - Take).

#### Input Parameters
* `type` - _optional_ - User specified object type as a search filter.
    Possible values: FaceList, LargeFaceList, LargePersonGroup, PersonGroup.
* `applyScope` - _optional_ - User specified snapshot apply scopes as a search filter. ApplyScope is an array of the target Azure subscription ids for the snapshot, specified by the user who created the snapshot by Snapshot - Take.

### Submit an operation to take a snapshot of face list, large face list, person group or large person group, with user-specified snapshot type, source object id, apply scope and an optional user data.<br /><br/>
> The snapshot interfaces are for users to backup and restore their face data from one face subscription to another, inside same region or across regions. The workflow contains two phases, user first calls Snapshot - Take to create a copy of the source object and store it as a snapshot, then calls Snapshot - Apply to paste the snapshot to target subscription. The snapshots are stored in a centralized location (per Azure instance), so that they can be applied cross accounts and regions.<br /><br/>
> Taking snapshot is an asynchronous operation. An operation id can be obtained from the "Operation-Location" field in response header, to be used in OperationStatus - Get for tracking the progress of creating the snapshot. The snapshot id will be included in the "resourceLocation" field in OperationStatus - Get response when the operation status is "succeeded".<br /><br/>
> Snapshot taking time depends on the number of person and face entries in the source object. It could be in seconds, or up to several hours for 1,000,000 persons with multiple faces.<br /><br/>
> Snapshots will be automatically expired and cleaned in 48 hours after it is created by Snapshot - Take. User can delete the snapshot using Snapshot - Delete by themselves any time before expiration.<br /><br/>
> Taking snapshot for a certain object will not block any other operations against the object. All read-only operations (Get/List and Identify/FindSimilar/Verify) can be conducted as usual. For all writable operations, including Add/Update/Delete the source object or its persons/faces and Train, they are not blocked but not recommended because writable updates may not be reflected on the snapshot during its taking. After snapshot taking is completed, all readable and writable operations can work as normal. Snapshot will also include the training results of the source object, which means target subscription the snapshot applied to does not need re-train the target object before calling Identify/FindSimilar.<br /><br/>
> * Free-tier subscription quota: 100 take operations per month.<br/>
> * S0-tier subscription quota: 100 take operations per day.

### Delete an existing snapshot according to the snapshotId. All object data and information in the snapshot will also be deleted. Only the source subscription who took the snapshot can delete the snapshot. If the user does not delete a snapshot with this API, the snapshot will still be automatically deleted in 48 hours after creation.

#### Input Parameters
* `snapshotId` - _required_ - Id referencing a particular snapshot.

### Retrieve information about a snapshot. Snapshot is only accessible to the source subscription who took it, and target subscriptions included in the applyScope in Snapshot - Take.

#### Input Parameters
* `snapshotId` - _required_ - Id referencing a particular snapshot.

### Update the information of a snapshot. Only the source subscription who took the snapshot can update the snapshot.

#### Input Parameters
* `snapshotId` - _required_ - Id referencing a particular snapshot.

### Submit an operation to apply a snapshot to current subscription. For each snapshot, only subscriptions included in the applyScope of Snapshot - Take can apply it.<br /><br/>
> The snapshot interfaces are for users to backup and restore their face data from one face subscription to another, inside same region or across regions. The workflow contains two phases, user first calls Snapshot - Take to create a copy of the source object and store it as a snapshot, then calls Snapshot - Apply to paste the snapshot to target subscription. The snapshots are stored in a centralized location (per Azure instance), so that they can be applied cross accounts and regions.<br /><br/>
> Applying snapshot is an asynchronous operation. An operation id can be obtained from the "Operation-Location" field in response header, to be used in OperationStatus - Get for tracking the progress of applying the snapshot. The target object id will be included in the "resourceLocation" field in OperationStatus - Get response when the operation status is "succeeded".<br /><br/>
> Snapshot applying time depends on the number of person and face entries in the snapshot object. It could be in seconds, or up to 1 hour for 1,000,000 persons with multiple faces.<br /><br/>
> Snapshots will be automatically expired and cleaned in 48 hours after it is created by Snapshot - Take. So the target subscription is required to apply the snapshot in 48 hours since its creation.<br /><br/>
> Applying a snapshot will not block any other operations against the target object, however it is not recommended because the correctness cannot be guaranteed during snapshot applying. After snapshot applying is completed, all operations towards the target object can work as normal. Snapshot also includes the training results of the source object, which means target subscription the snapshot applied to does not need re-train the target object before calling Identify/FindSimilar.<br /><br/>
> One snapshot can be applied multiple times in parallel, while currently only CreateNew apply mode is supported, which means the apply operation will fail if target subscription already contains an object of same type and using the same objectId. Users can specify the "objectId" in request body to avoid such conflicts.<br /><br/>
> * Free-tier subscription quota: 100 apply operations per month.<br/>
> * S0-tier subscription quota: 100 apply operations per day.

#### Input Parameters
* `snapshotId` - _required_ - Id referencing a particular snapshot.

### Verify whether two faces belong to a same person or whether one face belongs to a person.

## License

**flow**ground :- Telekom iPaaS / azure-com-cognitiveservices-face-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
