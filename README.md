Google Cloud Java Client
==========================

Java idiomatic client for [Google Cloud Platform][cloud-platform] services.

[![Build Status](https://travis-ci.org/GoogleCloudPlatform/gcloud-java.svg?branch=master)](https://travis-ci.org/GoogleCloudPlatform/gcloud-java)
[![Coverage Status](https://coveralls.io/repos/GoogleCloudPlatform/gcloud-java/badge.svg?branch=master)](https://coveralls.io/r/GoogleCloudPlatform/gcloud-java?branch=master)
[![Maven](https://img.shields.io/maven-central/v/com.google.cloud/gcloud-java.svg)]( https://img.shields.io/maven-central/v/com.google.cloud/gcloud-java.svg)
[![Codacy Badge](https://api.codacy.com/project/badge/grade/9da006ad7c3a4fe1abd142e77c003917)](https://www.codacy.com/app/mziccard/gcloud-java)
[![Dependency Status](https://www.versioneye.com/user/projects/56bd8ee72a29ed002d2b0969/badge.svg?style=flat)](https://www.versioneye.com/user/projects/56bd8ee72a29ed002d2b0969)

-  [Homepage] (https://googlecloudplatform.github.io/gcloud-java/)
-  [API Documentation] (http://googlecloudplatform.github.io/gcloud-java/apidocs)

This client supports the following Google Cloud Platform services:

-  [Google Cloud BigQuery] (#google-cloud-bigquery-alpha) (Alpha)
-  [Google Cloud Compute] (#google-cloud-compute-alpha) (Alpha)
-  [Google Cloud Datastore] (#google-cloud-datastore)
-  [Google Cloud DNS] (#google-cloud-dns-alpha) (Alpha)
-  [Google Cloud Pub/Sub] (#google-cloud-pubsub-alpha) (Alpha - Not working on App Engine Standard)
-  [Google Cloud Resource Manager] (#google-cloud-resource-manager-alpha) (Alpha)
-  [Google Cloud Storage] (#google-cloud-storage)

> Note: This client is a work-in-progress, and may occasionally
> make backwards-incompatible changes.

Quickstart
----------

> As of April 12th, 2016, `gcloud-java`'s group ID and base package were renamed to `com.google.cloud`. If you haven't already, please update your dependencies.

If you are using Maven, add this to your pom.xml file
```xml
<dependency>
  <groupId>com.google.cloud</groupId>
  <artifactId>gcloud-java</artifactId>
  <version>0.2.4</version>
</dependency>
```
If you are using Gradle, add this to your dependencies
```Groovy
compile 'com.google.cloud:gcloud-java:0.2.4'
```
If you are using SBT, add this to your dependencies
```Scala
libraryDependencies += "com.google.cloud" % "gcloud-java" % "0.2.4"
```

Example Applications
--------------------

- [`BigQueryExample`](./gcloud-java-examples/src/main/java/com/google/cloud/examples/bigquery/BigQueryExample.java) - A simple command line interface providing some of Cloud BigQuery's functionality
  - Read more about using this application on the [`BigQueryExample` docs page](http://googlecloudplatform.github.io/gcloud-java/apidocs/?com/google/cloud/examples/bigquery/BigQueryExample.html).
- [`ComputeExample`](./gcloud-java-examples/src/main/java/com/google/cloud/examples/compute/ComputeExample.java) - A simple command line interface providing some of Cloud Compute's functionality
  - Read more about using this application on the [`gcloud-java-examples` docs page](http://googlecloudplatform.github.io/gcloud-java/apidocs/?com/google/cloud/examples/compute/ComputeExample.html).
- [`Bookshelf`](https://github.com/GoogleCloudPlatform/getting-started-java/tree/master/bookshelf) - An App Engine app that manages a virtual bookshelf.
  - This app uses `gcloud-java` to interface with Cloud Datastore and Cloud Storage. It also uses Cloud SQL, another Google Cloud Platform service.
- [`DatastoreExample`](./gcloud-java-examples/src/main/java/com/google/cloud/examples/datastore/DatastoreExample.java) - A simple command line interface for Cloud Datastore
  - Read more about using this application on the [`DatastoreExample` docs page](http://googlecloudplatform.github.io/gcloud-java/apidocs/?com/google/cloud/examples/datastore/DatastoreExample.html).
- [`DnsExample`](./gcloud-java-examples/src/main/java/com/google/cloud/examples/dns/DnsExample.java) - A simple command line interface for Cloud DNS
  - Read more about using this application on the [`DnsExample` docs page](http://googlecloudplatform.github.io/gcloud-java/apidocs/?com/google/cloud/examples/dns/DnsExample.html).
- [`Flexible Environment/Datastore example`](https://github.com/GoogleCloudPlatform/java-docs-samples/tree/master/managed_vms/datastore) - A simple app that uses Cloud Datastore to list the last 10 IP addresses that visited your site.
  - Read about how to run the application [here](https://github.com/GoogleCloudPlatform/java-docs-samples/blob/master/managed_vms/README.md).
- [`Flexible Environment/Storage example`](https://github.com/GoogleCloudPlatform/java-docs-samples/tree/master/managed_vms/cloudstorage) - An app that uploads files to a public Cloud Storage bucket on the App Engine Flexible Environment runtime.
- [`PubSubExample`](./gcloud-java-examples/src/main/java/com/google/cloud/examples/pubsub/PubSubExample.java) - A simple command line interface providing some of Cloud Pub/Sub's functionality
  - Read more about using this application on the [`PubSubExample` docs page](http://googlecloudplatform.github.io/gcloud-java/apidocs/?com/google/cloud/examples/pubsub/PubSubExample.html).
- [`ResourceManagerExample`](./gcloud-java-examples/src/main/java/com/google/cloud/examples/resourcemanager/ResourceManagerExample.java) - A simple command line interface providing some of Cloud Resource Manager's functionality
  - Read more about using this application on the [`ResourceManagerExample` docs page](http://googlecloudplatform.github.io/gcloud-java/apidocs/?com/google/cloud/examples/resourcemanager/ResourceManagerExample.html).
- [`SparkDemo`](https://github.com/GoogleCloudPlatform/java-docs-samples/blob/master/managed_vms/sparkjava) - An example of using `gcloud-java-datastore` from within the SparkJava and App Engine Flexible Environment frameworks.
  - Read about how it works on the example's [README page](https://github.com/GoogleCloudPlatform/java-docs-samples/tree/master/managed_vms/sparkjava#how-does-it-work).
- [`StorageExample`](./gcloud-java-examples/src/main/java/com/google/cloud/examples/storage/StorageExample.java) - A simple command line interface providing some of Cloud Storage's functionality
  - Read more about using this application on the [`StorageExample` docs page](http://googlecloudplatform.github.io/gcloud-java/apidocs/?com/google/cloud/examples/storage/StorageExample.html).
- [`TaskList`](https://github.com/GoogleCloudPlatform/java-docs-samples/blob/master/datastore/src/main/java/com/google/datastore/snippets/TaskList.java) - A command line application that uses Cloud Datastore to manage a to-do list.
  - Read about how to run the application on its [README page](https://github.com/GoogleCloudPlatform/java-docs-samples/tree/master/datastore).

Specifying a Project ID
-----------------------

Most `gcloud-java` libraries require a project ID.  There are multiple ways to specify this project ID.

1. When using `gcloud-java` libraries from within Compute/App Engine, there's no need to specify a project ID.  It is automatically inferred from the production environment.
2. When using `gcloud-java` elsewhere, you can do one of the following:
  * Supply the project ID when building the service options.  For example, to use Datastore from a project with ID "PROJECT_ID", you can write:

  ```java
  Datastore datastore = DatastoreOptions.builder().projectId("PROJECT_ID").build().service(); 
  ```
  * Specify the environment variable `GCLOUD_PROJECT` to be your desired project ID.
  * Set the project ID using the [Google Cloud SDK](https://cloud.google.com/sdk/?hl=en).  To use the SDK, [download the SDK](https://cloud.google.com/sdk/?hl=en) if you haven't already, and set the project ID from the command line.  For example:

  ```
  gcloud config set project PROJECT_ID
  ```

`gcloud-java` determines the project ID from the following sources in the listed order, stopping once it finds a value:

1. Project ID supplied when building the service options
2. Project ID specified by the environment variable `GCLOUD_PROJECT`
3. App Engine project ID
4. Project ID specified in the JSON credentials file pointed by the `GOOGLE_APPLICATION_CREDENTIALS` environment variable
5. Google Cloud SDK project ID
6. Compute Engine project ID

Authentication
--------------

First, ensure that the necessary Google Cloud APIs are enabled for your project. To do this, follow the instructions on the [authentication document](https://github.com/GoogleCloudPlatform/gcloud-common/blob/master/authentication/readme.md#authentication) shared by all the gcloud language libraries.

Next, choose a method for authenticating API requests from within your project:

1. When using `gcloud-java` libraries from within Compute/App Engine, no additional authentication steps are necessary.
2. When using `gcloud-java` libraries elsewhere, there are three options:
  * [Generate a JSON service account key](https://cloud.google.com/storage/docs/authentication?hl=en#service_accounts).  After downloading that key, you must do one of the following:
    * Define the environment variable GOOGLE_APPLICATION_CREDENTIALS to be the location of the key.  For example:
    ```bash
    export GOOGLE_APPLICATION_CREDENTIALS=/path/to/my/key.json
    ```
    * Supply the JSON credentials file when building the service options.  For example, this Storage object has the necessary permissions to interact with your Google Cloud Storage data:
    ```java
    Storage storage = StorageOptions.builder()
        .authCredentials(AuthCredentials.createForJson(new FileInputStream("/path/to/my/key.json"))
        .build()
        .service();
    ```
  * If running locally for development/testing, you can use Google Cloud SDK.  Download the SDK if you haven't already, then login using the SDK (`gcloud auth login` in command line).  Be sure to set your project ID as described above.
  * If you already have an OAuth2 access token, you can use it to authenticate (notice that in this case the access token will not be automatically refreshed):
  ```java
  Storage storage = StorageOptions.builder()
      .authCredentials(AuthCredentials.createFor("your_access_token"))
      .build()
      .service();
  ```

`gcloud-java` looks for credentials in the following order, stopping once it finds credentials:

1. Credentials supplied when building the service options
2. App Engine credentials
3. Key file pointed to by the GOOGLE_APPLICATION_CREDENTIALS environment variable
4. Google Cloud SDK credentials
5. Compute Engine credentials

Google Cloud BigQuery (Alpha)
----------------------

- [API Documentation][bigquery-api]
- [Official Documentation][cloud-bigquery-docs]

#### Preview

Here is a code snippet showing a simple usage example from within Compute/App Engine. Note that you
must [supply credentials](#authentication) and a project ID if running this snippet elsewhere.
Complete source code can be found at
[CreateTableAndLoadData.java](./gcloud-java-examples/src/main/java/com/google/cloud/examples/bigquery/snippets/CreateTableAndLoadData.java).

```java
import com.google.cloud.bigquery.BigQuery;
import com.google.cloud.bigquery.BigQueryOptions;
import com.google.cloud.bigquery.Field;
import com.google.cloud.bigquery.FormatOptions;
import com.google.cloud.bigquery.Job;
import com.google.cloud.bigquery.Schema;
import com.google.cloud.bigquery.StandardTableDefinition;
import com.google.cloud.bigquery.Table;
import com.google.cloud.bigquery.TableId;
import com.google.cloud.bigquery.TableInfo;

BigQuery bigquery = BigQueryOptions.defaultInstance().service();
TableId tableId = TableId.of("dataset", "table");
Table table = bigquery.getTable(tableId);
if (table == null) {
  System.out.println("Creating table " + tableId);
  Field integerField = Field.of("fieldName", Field.Type.integer());
  Schema schema = Schema.of(integerField);
  table = bigquery.create(TableInfo.of(tableId, StandardTableDefinition.of(schema)));
}
System.out.println("Loading data into table " + tableId);
Job loadJob = table.load(FormatOptions.csv(), "gs://bucket/path");
loadJob = loadJob.waitFor();
if (loadJob.status().error() != null) {
  System.out.println("Job completed with errors");
} else {
  System.out.println("Job succeeded");
}
```

Google Cloud Compute (Alpha)
----------------------

- [API Documentation][compute-api]
- [Official Documentation][cloud-compute-docs]

#### Preview

Here are two code snippets showing simple usage examples from within Compute/App Engine. Note that
you must [supply credentials](#authentication) and a project ID if running this snippet elsewhere.

The first snippet shows how to create a snapshot from an existing disk. Complete source code can be
found at
[CreateSnapshot.java](./gcloud-java-examples/src/main/java/com/google/cloud/examples/compute/snippets/CreateSnapshot.java).

```java
import com.google.cloud.compute.Compute;
import com.google.cloud.compute.ComputeOptions;
import com.google.cloud.compute.Disk;
import com.google.cloud.compute.DiskId;
import com.google.cloud.compute.Snapshot;

Compute compute = ComputeOptions.defaultInstance().service();
DiskId diskId = DiskId.of("us-central1-a", "disk-name");
Disk disk = compute.getDisk(diskId, Compute.DiskOption.fields());
if (disk != null) {
  String snapshotName = "disk-name-snapshot";
  Operation operation = disk.createSnapshot(snapshotName);
  operation = operation.waitFor();
  if (operation.errors() == null) {
    // use snapshot
    Snapshot snapshot = compute.getSnapshot(snapshotName);
  }
}
```
The second snippet shows how to create a virtual machine instance. Complete source code can be found
at
[CreateInstance.java](./gcloud-java-examples/src/main/java/com/google/cloud/examples/compute/snippets/CreateInstance.java).
```java
import com.google.cloud.compute.AttachedDisk;
import com.google.cloud.compute.Compute;
import com.google.cloud.compute.ComputeOptions;
import com.google.cloud.compute.ImageId;
import com.google.cloud.compute.Instance;
import com.google.cloud.compute.InstanceId;
import com.google.cloud.compute.InstanceInfo;
import com.google.cloud.compute.MachineTypeId;
import com.google.cloud.compute.NetworkId;

Compute compute = ComputeOptions.defaultInstance().service();
ImageId imageId = ImageId.of("debian-cloud", "debian-8-jessie-v20160329");
NetworkId networkId = NetworkId.of("default");
AttachedDisk attachedDisk = AttachedDisk.of(AttachedDisk.CreateDiskConfiguration.of(imageId));
NetworkInterface networkInterface = NetworkInterface.of(networkId);
InstanceId instanceId = InstanceId.of("us-central1-a", "instance-name");
MachineTypeId machineTypeId = MachineTypeId.of("us-central1-a", "n1-standard-1");
Operation operation =
    compute.create(InstanceInfo.of(instanceId, machineTypeId, attachedDisk, networkInterface));
operation = operation.waitFor();
if (operation.errors() == null) {
  // use instance
  Instance instance = compute.getInstance(instanceId);
}
```

Google Cloud Datastore
----------------------

- [API Documentation][datastore-api]
- [Official Documentation][cloud-datastore-docs]

*Follow the [activation instructions][cloud-datastore-activation] to use the Google Cloud Datastore API with your project.*

#### Preview

Here are two code snippets showing simple usage examples from within Compute/App Engine. Note that you must [supply credentials](#authentication) and a project ID if running this snippet elsewhere.

The first snippet shows how to create a Datastore entity. Complete source code can be found at
[CreateEntity.java](./gcloud-java-examples/src/main/java/com/google/cloud/examples/datastore/snippets/CreateEntity.java).

```java
import com.google.cloud.datastore.Datastore;
import com.google.cloud.datastore.DatastoreOptions;
import com.google.cloud.datastore.DateTime;
import com.google.cloud.datastore.Entity;
import com.google.cloud.datastore.Key;
import com.google.cloud.datastore.KeyFactory;

Datastore datastore = DatastoreOptions.defaultInstance().service();
KeyFactory keyFactory = datastore.newKeyFactory().kind("keyKind");
Key key = keyFactory.newKey("keyName");
Entity entity = Entity.builder(key)
    .set("name", "John Doe")
    .set("age", 30)
    .set("access_time", DateTime.now())
    .build();
datastore.put(entity);
```
The second snippet shows how to update a Datastore entity if it exists. Complete source code can be
found at
[UpdateEntity.java](./gcloud-java-examples/src/main/java/com/google/cloud/examples/datastore/snippets/UpdateEntity.java).
```java
import com.google.cloud.datastore.Datastore;
import com.google.cloud.datastore.DatastoreOptions;
import com.google.cloud.datastore.DateTime;
import com.google.cloud.datastore.Entity;
import com.google.cloud.datastore.Key;
import com.google.cloud.datastore.KeyFactory;

Datastore datastore = DatastoreOptions.defaultInstance().service();
KeyFactory keyFactory = datastore.newKeyFactory().kind("keyKind");
Key key = keyFactory.newKey("keyName");
Entity entity = datastore.get(key);
if (entity != null) {
  System.out.println("Updating access_time for " + entity.getString("name"));
  entity = Entity.builder(entity)
      .set("access_time", DateTime.now())
      .build();
  datastore.update(entity);
}
```

Google Cloud DNS (Alpha)
----------------------
- [API Documentation][dns-api]
- [Official Documentation][cloud-dns-docs]

*Follow the [activation instructions][cloud-dns-activation] to use the Google Cloud DNS API with your project.*

#### Preview

Here are two code snippets showing simple usage examples from within Compute/App Engine. Note that you must [supply credentials](#authentication) and a project ID if running this snippet elsewhere.

The first snippet shows how to create a zone resource. Complete source code can be found on
[CreateZone.java](./gcloud-java-examples/src/main/java/com/google/cloud/examples/dns/snippets/CreateZone.java).

```java
import com.google.cloud.dns.Dns;
import com.google.cloud.dns.DnsOptions;
import com.google.cloud.dns.Zone;
import com.google.cloud.dns.ZoneInfo;

Dns dns = DnsOptions.defaultInstance().service();
String zoneName = "my-unique-zone";
String domainName = "someexampledomain.com.";
String description = "This is a gcloud-java-dns sample zone.";
ZoneInfo zoneInfo = ZoneInfo.of(zoneName, domainName, description);
Zone zone = dns.create(zoneInfo);
```

The second snippet shows how to create records inside a zone. The complete code can be found on [CreateOrUpdateRecordSets.java](./gcloud-java-examples/src/main/java/com/google/cloud/examples/dns/snippets/CreateOrUpdateRecordSets.java).

```java
import com.google.cloud.dns.ChangeRequestInfo;
import com.google.cloud.dns.Dns;
import com.google.cloud.dns.DnsOptions;
import com.google.cloud.dns.RecordSet;
import com.google.cloud.dns.Zone;

import java.util.Iterator;
import java.util.concurrent.TimeUnit;

Dns dns = DnsOptions.defaultInstance().service();
String zoneName = "my-unique-zone";
Zone zone = dns.getZone(zoneName);
String ip = "12.13.14.15";
RecordSet toCreate = RecordSet.builder("www.someexampledomain.com.", RecordSet.Type.A)
    .ttl(24, TimeUnit.HOURS)
    .addRecord(ip)
    .build();
ChangeRequestInfo.Builder changeBuilder = ChangeRequestInfo.builder().add(toCreate);

// Verify that the record does not exist yet.
// If it does exist, we will overwrite it with our prepared record.
Iterator<RecordSet> recordSetIterator = zone.listRecordSets().iterateAll();
while (recordSetIterator.hasNext()) {
  RecordSet current = recordSetIterator.next();
  if (toCreate.name().equals(current.name()) &&
      toCreate.type().equals(current.type())) {
    changeBuilder.delete(current);
  }
}

ChangeRequestInfo changeRequest = changeBuilder.build();
zone.applyChangeRequest(changeRequest);
```

Google Cloud Pub/Sub (Alpha)
----------------------

- [API Documentation][pubsub-api]
- [Official Documentation][cloud-pubsub-docs]

#### Preview

Here is a code snippet showing a simple usage example from within Compute Engine/App Engine
Flexible. Note that you must [supply credentials](#authentication) and a project ID if running this
snippet elsewhere. Complete source code can be found at
[CreateSubscriptionAndPullMessages.java](./gcloud-java-examples/src/main/java/com/google/cloud/examples/pubsub/snippets/CreateSubscriptionAndPullMessages.java).

```java
import com.google.cloud.pubsub.Message;
import com.google.cloud.pubsub.PubSub;
import com.google.cloud.pubsub.PubSub.MessageConsumer;
import com.google.cloud.pubsub.PubSub.MessageProcessor;
import com.google.cloud.pubsub.PubSubOptions;
import com.google.cloud.pubsub.Subscription;
import com.google.cloud.pubsub.SubscriptionInfo;

try (PubSub pubsub = PubSubOptions.defaultInstance().service()) {
  Subscription subscription =
      pubsub.create(SubscriptionInfo.of("test-topic", "test-subscription"));
  MessageProcessor callback = new MessageProcessor() {
    @Override
    public void process(Message message) throws Exception {
      System.out.printf("Received message \"%s\"%n", message.payloadAsString());
    }
  };
  // Create a message consumer and pull messages (for 60 seconds)
  try (MessageConsumer consumer = subscription.pullAsync(callback)) {
    Thread.sleep(60_000);
  }
}
```

Google Cloud Resource Manager (Alpha)
----------------------

- [API Documentation][resourcemanager-api]
- [Official Documentation][cloud-resourcemanager-docs]

#### Preview

Here is a code snippet showing a simple usage example. Note that you must supply Google SDK credentials for this service, not other forms of authentication listed in the [Authentication section](#authentication).
Complete source code can be found at
[UpdateAndListProjects.java](./gcloud-java-examples/src/main/java/com/google/cloud/examples/resourcemanager/snippets/UpdateAndListProjects.java).
```java
import com.google.cloud.resourcemanager.Project;
import com.google.cloud.resourcemanager.ResourceManager;
import com.google.cloud.resourcemanager.ResourceManagerOptions;

import java.util.Iterator;

ResourceManager resourceManager = ResourceManagerOptions.defaultInstance().service();
Project project = resourceManager.get("some-project-id"); // Use an existing project's ID
if (project != null) {
  Project newProject = project.toBuilder()
      .addLabel("launch-status", "in-development")
      .build()
      .replace();
  System.out.println("Updated the labels of project " + newProject.projectId()
      + " to be " + newProject.labels());
}
Iterator<Project> projectIterator = resourceManager.list().iterateAll();
System.out.println("Projects I can view:");
while (projectIterator.hasNext()) {
  System.out.println(projectIterator.next().projectId());
}
```

Google Cloud Storage
----------------------

- [API Documentation][storage-api]
- [Official Documentation][cloud-storage-docs]

*Follow the [activation instructions][cloud-storage-activation] to use the Google Cloud Storage API with your project.*

#### Preview

Here are two code snippets showing simple usage examples from within Compute/App Engine.  Note that you must [supply credentials](#authentication) and a project ID if running this snippet elsewhere.

The first snippet shows how to create a Storage blob. Complete source code can be found at
[CreateBlob.java](./gcloud-java-examples/src/main/java/com/google/cloud/examples/storage/snippets/CreateBlob.java).

```java
import static java.nio.charset.StandardCharsets.UTF_8;

import com.google.cloud.storage.Blob;
import com.google.cloud.storage.BlobId;
import com.google.cloud.storage.BlobInfo;
import com.google.cloud.storage.Storage;
import com.google.cloud.storage.StorageOptions;

Storage storage = StorageOptions.defaultInstance().service();
BlobId blobId = BlobId.of("bucket", "blob_name");
BlobInfo blobInfo = BlobInfo.builder(blobId).contentType("text/plain").build();
Blob blob = storage.create(blobInfo, "Hello, Cloud Storage!".getBytes(UTF_8));
```
The second snippet shows how to update a Storage blob if it exists. Complete source code can be
found at
[UpdateBlob.java](./gcloud-java-examples/src/main/java/com/google/cloud/examples/storage/snippets/UpdateBlob.java).
```java
import static java.nio.charset.StandardCharsets.UTF_8;

import com.google.cloud.storage.Blob;
import com.google.cloud.storage.BlobId;
import com.google.cloud.storage.Storage;
import com.google.cloud.storage.StorageOptions;

import java.nio.ByteBuffer;
import java.nio.channels.WritableByteChannel;

Storage storage = StorageOptions.defaultInstance().service();
BlobId blobId = BlobId.of("bucket", "blob_name");
Blob blob = storage.get(blobId);
if (blob != null) {
  byte[] prevContent = blob.content();
  System.out.println(new String(prevContent, UTF_8));
  WritableByteChannel channel = blob.writer();
  channel.write(ByteBuffer.wrap("Updated content".getBytes(UTF_8)));
  channel.close();
}
```

Troubleshooting
---------------

To get help, follow the `gcloud-java` links in the `gcloud-*` [shared Troubleshooting document](https://github.com/GoogleCloudPlatform/gcloud-common/blob/master/troubleshooting/readme.md#troubleshooting).

Java Versions
-------------

Java 7 or above is required for using this client.

Testing
-------

This library provides tools to help write tests for code that uses gcloud-java services.

See [TESTING] to read more about using our testing helpers.

Versioning
----------

This library follows [Semantic Versioning] (http://semver.org/).

It is currently in major version zero (``0.y.z``), which means that anything
may change at any time and the public API should not be considered
stable.

Contributing
------------

Contributions to this library are always welcome and highly encouraged.

See `gcloud-java`'s [CONTRIBUTING] documentation and the `gcloud-*` [shared documentation](https://github.com/GoogleCloudPlatform/gcloud-common/blob/master/contributing/readme.md#how-to-contribute-to-gcloud) for more information on how to get started.

Please note that this project is released with a Contributor Code of Conduct. By participating in this project you agree to abide by its terms. See [Code of Conduct][code-of-conduct] for more information.

License
-------

Apache 2.0 - See [LICENSE] for more information.


[CONTRIBUTING]:https://github.com/GoogleCloudPlatform/gcloud-java/blob/master/CONTRIBUTING.md
[code-of-conduct]:https://github.com/GoogleCloudPlatform/gcloud-java/blob/master/CODE_OF_CONDUCT.md#contributor-code-of-conduct
[LICENSE]: https://github.com/GoogleCloudPlatform/gcloud-java/blob/master/LICENSE
[TESTING]: https://github.com/GoogleCloudPlatform/gcloud-java/blob/master/TESTING.md
[cloud-platform]: https://cloud.google.com/
[cloud-datastore]: https://cloud.google.com/datastore/docs
[cloud-datastore-docs]: https://cloud.google.com/datastore/docs
[cloud-datastore-activation]: https://cloud.google.com/datastore/docs/activate
[datastore-api]: http://googlecloudplatform.github.io/gcloud-java/apidocs/index.html?com/google/cloud/datastore/package-summary.html

[dns-api]: http://googlecloudplatform.github.io/gcloud-java/apidocs/index.html?com/google/cloud/dns/package-summary.html
[cloud-dns-docs]: https://cloud.google.com/dns/docs
[cloud-dns-activation]: https://console.cloud.google.com/start/api?id=dns

[pubsub-api]: http://googlecloudplatform.github.io/gcloud-java/apidocs/index.html?com/google/cloud/pubsub/package-summary.html
[cloud-pubsub]: https://cloud.google.com/pubsub/
[cloud-pubsub-docs]: https://cloud.google.com/pubsub/docs

[cloud-storage]: https://cloud.google.com/storage/
[cloud-storage-docs]: https://cloud.google.com/storage/docs/overview
[cloud-storage-create-bucket]: https://cloud.google.com/storage/docs/cloud-console#_creatingbuckets
[cloud-storage-activation]: https://cloud.google.com/storage/docs/signup
[storage-api]: http://googlecloudplatform.github.io/gcloud-java/apidocs/index.html?com/google/cloud/storage/package-summary.html

[resourcemanager-api]:http://googlecloudplatform.github.io/gcloud-java/apidocs/index.html?com/google/cloud/resourcemanager/package-summary.html
[cloud-resourcemanager-docs]:https://cloud.google.com/resource-manager/

[cloud-bigquery]: https://cloud.google.com/bigquery/
[cloud-bigquery-docs]: https://cloud.google.com/bigquery/docs/overview
[bigquery-api]: http://googlecloudplatform.github.io/gcloud-java/apidocs/index.html?com/google/cloud/bigquery/package-summary.html

[cloud-compute]: https://cloud.google.com/compute/
[cloud-compute-docs]: https://cloud.google.com/compute/docs/overview
[compute-api]: http://googlecloudplatform.github.io/gcloud-java/apidocs/index.html?com/google/cloud/compute/package-summary.html
