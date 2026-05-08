---
name: gcloud
description: Context regard the gcloud CLI
metadata:
  author: Liam Grossman
  version: 0.0.1
---

### List Bindings with Alpha Version

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/cloud-bindings/list

This command uses the alpha version of the access-context-manager to list cloud bindings. Ensure you have the alpha components installed.

```bash
gcloud alpha access-context-manager cloud-bindings list
```

--------------------------------

### Example Access Binding Output (YAML)

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/cloud-bindings/list

This is an example of the YAML output format for a Google Cloud user access binding. It details access levels, group keys, and session settings.

```yaml
---
accessLevels:
- accessPolicies/9522/accessLevels/device_trusted
dryRunAccessLevels:
- accessPolicies/9522/accessLevels/specific_location
groupKey: a3dad
name: organizations/256/gcpUserAccessBindings/b3-BhcX_Ud5N
sessionSettings:
  sessionLength: 57600s
  sessionLengthEnabled: true
  sessionReauthMethod: LOGIN

```

--------------------------------

### JSON instances file example

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai-platform/local/predict

Instances are read from a local file in JSON format, with each instance on a new line. This format is suitable for structured data.

```json
{"images": [0.0, …, 0.1], "key": 3}
{"images": [0.0, …, 0.1], "key": 2}
…
```

--------------------------------

### Text instances file example

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai-platform/local/predict

Instances are read from a local file in UTF-8 encoded text format, with each instance on a new line. This is useful for simple, non-structured data like CSV.

```text
107,4.9,2.5,4.5,1.7
100,5.7,2.8,4.1,1.3
…
```

--------------------------------

### List VPC Service Controls Supported Services

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/supported-services

Use this command to see all VPC Service Controls supported services. No specific setup or imports are required beyond having the gcloud CLI installed.

```bash
gcloud access-context-manager supported-services list
```

--------------------------------

### Example Access Binding Output with Scoped Settings (YAML)

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/cloud-bindings/list

This YAML output demonstrates a more complex access binding configuration, including scoped access settings for different client applications and environments.

```yaml
---
accessLevels:
- accessPolicies/9522/accessLevels/device_trusted
dryRunAccessLevels:
- accessPolicies/9522/accessLevels/specific_location
groupKey: a3dad
name: organizations/256/gcpUserAccessBindings/b3-BhcX_Ud5N
scopedAccessSettings:
- activeSettings:
    accessLevels:
    - accessPolicies/9522/accessLevels/device_trusted
  dryRunSettings:
    accessLevels:
    - accessPolicies/9522/accessLevels/specific_location
  scope:
    clientScope:
      restrictedClientApplication:
        clientId: 123.apps.googleusercontent.com
- activeSettings:
    accessLevels:
    - accessPolicies/9522/accessLevels/device_trusted
  dryRunSettings:
    accessLevels:
    - accessPolicies/9522/accessLevels/specific_location
  scope:
    clientScope:
      restrictedClientApplication:
        name: Cloud Console
- activeSettings:
    sessionSettings:
      sessionLength: 57600s
      sessionLengthEnabled: true
      sessionReauthMethod: LOGIN
  scope:
    clientScope:
      restrictedClientApplication:
        clientId: 123.apps.googleusercontent.com
sessionSettings:
  sessionLength: 57600s
  sessionLengthEnabled: true
  sessionReauthMethod: LOGIN

```

--------------------------------

### List AI Platform Jobs

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai-platform/jobs/list

Use this command to list all existing AI Platform jobs. No specific setup is required beyond having the gcloud CLI installed and authenticated.

```bash
gcloud ai-platform jobs list
```

--------------------------------

### Configure Private Service Connect (PSC) auto-connections

Source: https://docs.cloud.google.com/sdk/gcloud/reference/alloydb/instances/create-secondary

Specify consumer project and network pairs for Private Service Connect (PSC) connectivity. Both project and network must be specified. Example: --psc-auto-connections=project=project1,network=projects/vpc-host-project1/global/networks/network1

```bash
--psc-auto-connections=[`network`=`NETWORK`],[`project`=`PROJECT`]
```

```bash
--psc-auto-connections=network=string,project=string
```

```bash
--psc-auto-connections='{"network": "string", "project": "string"}'
```

```bash
--psc-auto-connections=path_to_file.(yaml|json)
```

--------------------------------

### Describe an AlloyDB instance

Source: https://docs.cloud.google.com/sdk/gcloud/reference/alloydb/instances/describe

Use this command to get detailed information about an AlloyDB instance. Specify the instance ID, cluster ID, and region. The `--view` flag can be used to control the level of detail returned.

```bash
gcloud alloydb instances describe my-instance --cluster=my-cluster --region=us-central1 --view=BASIC/FULL
```

--------------------------------

### JSON request file example

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai-platform/local/predict

A local file containing the body of a JSON request, which includes a list of instances. This is a common format for sending multiple prediction requests.

```json
{
  "instances": [
    {"x": [1, 2], "y": [3, 4]},
    {"x": [-1, -2], "y": [-3, -4]}
  ]
}
```

--------------------------------

### Describe a custom job

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/custom-jobs/describe

Use this command to get detailed information about a specific custom job. Ensure you provide the job ID and the region where it is located. The `--project` flag can be used to specify the project.

```bash
gcloud ai custom-jobs describe 123 --project=example --region=us-central1
```

--------------------------------

### Describe VPC Service Controls Supported Service

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/supported-services

Use this command to get support information about a specific VPC Service Controls supported service. Replace SERVICE_NAME with the actual service name.

```bash
gcloud access-context-manager supported-services describe SERVICE_NAME
```

--------------------------------

### Configure database flags

Source: https://docs.cloud.google.com/sdk/gcloud/reference/alloydb/instances/create-secondary

Set database flags for the instance. Flags can be set with values, or without values for flags like skip_grant_tables. Use on/off for boolean flags. Example: --database-flags max_allowed_packet=55555,skip_grant_tables=,log_output=1

```bash
--database-flags `FLAG`=`VALUE`,[`FLAG`=`VALUE`,...]
```

--------------------------------

### Describe a Tensorboard with full path

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/tensorboards/describe

Use this command to describe a Tensorboard by providing its full resource path, including project, location, and Tensorboard ID. Ensure the project and region are correctly specified.

```bash
gcloud ai tensorboards describe projects/my-project/locations/us-central1/tensorboards/12345
```

--------------------------------

### List Cloud Access Bindings

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/cloud-bindings/list

Run this command to list all cloud access bindings under your organization. The output is provided in YAML format.

```bash
gcloud access-context-manager cloud-bindings list
```

--------------------------------

### Use beta version of gcloud ai tensorboards describe

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/tensorboards/describe

This command uses the beta version of the gcloud AI Tensorboards describe command. Beta versions offer features that are close to final but may still undergo changes.

```bash
gcloud beta ai tensorboards describe
```

--------------------------------

### Describe an AlloyDB instance (Beta)

Source: https://docs.cloud.google.com/sdk/gcloud/reference/alloydb/instances/describe

This command is available in the beta version of the gcloud CLI.

```bash
gcloud beta alloydb instances describe
```

--------------------------------

### GET gcloud active-directory peerings list

Source: https://docs.cloud.google.com/sdk/gcloud/reference/active-directory/peerings/list

Lists all Managed Microsoft AD domain peerings in the given project.

```APIDOC
## GET gcloud active-directory peerings list

### Description
List all Managed Microsoft AD domain peerings in the given project.

### Method
GET

### Endpoint
gcloud active-directory peerings list

### Parameters
#### Query Parameters
- **--filter** (EXPRESSION) - Optional - Apply a Boolean filter EXPRESSION to each resource item to be listed.
- **--limit** (LIMIT) - Optional - Maximum number of resources to list.
- **--page-size** (PAGE_SIZE) - Optional - Maximum number of resources per page.
- **--sort-by** (FIELD,...) - Optional - Comma-separated list of resource field key names to sort by.
- **--uri** (boolean) - Optional - Print a list of resource URIs instead of the default output.

### Request Example
```
gcloud active-directory peerings list --limit=5
```
```

--------------------------------

### Configure PSC network attachment URI

Source: https://docs.cloud.google.com/sdk/gcloud/reference/alloydb/instances/create-secondary

Specify the full URI of the network attachment for outbound connectivity from an AlloyDB instance using Private Service Connect (PSC). Example: psc-network-attachment-uri=projects/test-project/regions/us-central1/networkAttachments/my-na

```bash
--psc-network-attachment-uri=`PSC_NETWORK_ATTACHMENT_URI`
```

--------------------------------

### Create an access policy with beta version

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy using the beta version of the gcloud access-context-manager component. Beta versions offer more features than stable releases but may still have some instability.

```bash
gcloud beta access-context-manager policies create --organization=organizations/123 --title="My Beta Policy"
```

--------------------------------

### gcloud ai-platform local predict command

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai-platform/local/predict

This command runs prediction locally. Ensure the TensorFlow SDK is installed and specify the model directory along with one of the instance input flags.

```bash
gcloud ai-platform local predict --model-dir=MODEL_DIR --json-instances=JSON_INSTANCES
```

--------------------------------

### Create an access policy with multiple scopes

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command demonstrates creating an access policy with multiple scopes, such as both a folder and a project. Note that the documentation states only one folder or project can be specified as a scope.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --scopes=folders/345,projects/567 --title="My Multi-Scope Policy"
```

--------------------------------

### Create an access policy with an access token file

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy using an access token from a file. The `--access-token-file` flag allows you to authenticate using a pre-obtained access token.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --title="My Access Token Policy" --access-token-file=token.txt
```

--------------------------------

### Beta version of describe command

Source: https://docs.cloud.google.com/sdk/gcloud/reference/active-directory/domains/describe

This is an alternative command for describing a Managed Microsoft AD domain using the beta version of the gcloud CLI.

```bash
gcloud beta active-directory domains describe
```

--------------------------------

### Enable connection pooling

Source: https://docs.cloud.google.com/sdk/gcloud/reference/alloydb/instances/create-secondary

Enable connection pooling for the instance. Use --enable-connection-pooling to enable and --no-enable-connection-pooling to disable.

```bash
--[no-]enable-connection-pooling
```

--------------------------------

### Describe an AlloyDB instance (Alpha)

Source: https://docs.cloud.google.com/sdk/gcloud/reference/alloydb/instances/describe

This command is available in the alpha version of the gcloud CLI.

```bash
gcloud alpha alloydb instances describe
```

--------------------------------

### Create an access policy with a configuration file

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy using a configuration file. The `--flags-file` flag allows you to specify a file containing command-line flags, which can help in managing complex configurations.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --title="My Config File Policy" --flags-file=config.txt
```

--------------------------------

### gcloud ai-platform local predict

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai-platform/local/predict

Runs prediction locally with the given instances. Requires the TensorFlow SDK to be installed locally. The output format mirrors `gcloud ai-platform predict` (online prediction). Custom prediction routines cannot be used with this command.

```APIDOC
## gcloud ai-platform local predict

### Description
Performs prediction locally with the given instances. Requires the TensorFlow SDK to be installed locally. The output format mirrors `gcloud ai-platform predict` (online prediction). You cannot use this command with custom prediction routines.

### Method
COMMAND

### Endpoint
gcloud ai-platform local predict

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
None

### Flags
#### Required Flags
* `--model-dir`=`MODEL_DIR` (string) - Path to the model.

Exactly one of the following must be specified:
* `--json-instances`=`JSON_INSTANCES` (string) - Path to a local file from which instances are read. Instances are in JSON format; newline delimited. This flag accepts "-" for stdin.
* `--json-request`=`JSON_REQUEST` (string) - Path to a local file containing the body of JSON request. This flag accepts "-" for stdin.
* `--text-instances`=`TEXT_INSTANCES` (string) - Path to a local file from which instances are read. Instances are in UTF-8 encoded text format; newline delimited. This flag accepts "-" for stdin.

#### Optional Flags
* `--framework`=`FRAMEWORK` (string) - ML framework used to train this version of the model. If not specified, defaults to 'tensorflow'. `FRAMEWORK` must be one of: `scikit-learn`, `tensorflow`, `xgboost`.
* `--signature-name`=`SIGNATURE_NAME` (string) - Name of the signature defined in the SavedModel to use for this job. Defaults to DEFAULT_SERVING_SIGNATURE_DEF_KEY in https://www.tensorflow.org/api_docs/python/tf/compat/v1/saved_model/signature_constants, which is "serving_default". Only applies to TensorFlow models.

#### Gcloud Wide Flags
These flags are available to all commands: `--access-token-file`, `--account`, `--billing-project`, `--configuration`, `--flags-file`, `--flatten`, `--format`, `--help`, `--impersonate-service-account`, `--log-http`, `--project`, `--quiet`, `--trace-token`, `--user-output-enabled`, `--verbosity`. Run `$ gcloud help` for details.

### Request Example
```bash
gcloud ai-platform local predict \
  --model-dir="/path/to/your/model" \
  --json-instances="/path/to/instances.jsonl"
```

### Response
#### Success Response (200)
Output format mirrors `gcloud ai-platform predict` (online prediction).

#### Response Example
```json
{
  "predictions": [
    [0.1, 0.9],
    [0.8, 0.2]
  ]
}
```

### Variants
* `gcloud alpha ai-platform local predict`
* `gcloud beta ai-platform local predict`
```

--------------------------------

### Copy a model to a new model ID

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/models/copy

This command copies a source model and assigns it a new, unique ID in the destination. The new model ID must be between 1 and 63 characters and can only contain lowercase letters, numbers, and hyphens. It cannot start with a number or hyphen.

```bash
gcloud ai models copy --source-model=SOURCE_MODEL --destination-model-id=DESTINATION_MODEL_ID
```

--------------------------------

### Use alpha version of gcloud ai tensorboards describe

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/tensorboards/describe

This command uses the alpha version of the gcloud AI Tensorboards describe command. Alpha versions may include experimental features and are subject to change.

```bash
gcloud alpha ai tensorboards describe
```

--------------------------------

### Deploy a Model Garden model

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/model-garden/models/deploy

Use this command to deploy a model from Model Garden. Ensure you specify the correct model format and project details.

```bash
gcloud ai model-garden models deploy --model=google/gemma2@gemma-2-9b --project=example --region=us-central1
```

--------------------------------

### gcloud beta ai custom-jobs describe

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/custom-jobs/describe

This is a beta version of the command to describe a custom job. It offers more stability than alpha but may still evolve.

```bash
gcloud beta ai custom-jobs describe
```

--------------------------------

### Create an access policy with a trace token

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy and includes a trace token for debugging. The `--trace-token` flag is useful for tracking requests through the Google Cloud infrastructure.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --title="My Trace Token Policy" --trace-token=my-trace-id
```

--------------------------------

### List AD Domain Peerings with Limit

Source: https://docs.cloud.google.com/sdk/gcloud/reference/active-directory/peerings/list

Use this command to list a specified number of AD domain peerings in your project. Ensure your account has the necessary permissions.

```bash
gcloud active-directory peerings list --limit=5
```

--------------------------------

### Create an access policy for the entire organization

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

Use this command to create a new access policy that applies to your entire organization. Ensure you have the correct organization ID and a descriptive title.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --title="My Policy"
```

--------------------------------

### gcloud beta ai models list

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/models/list

This is a beta version of the command. It offers more features than the stable version but may still be subject to change.

```bash
gcloud beta ai models list
```

--------------------------------

### Describe a Tensorboard using flags

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/tensorboards/describe

This command describes a Tensorboard using its ID and specifying the region and project via flags. This is a more concise way to target a specific Tensorboard when the full path is not provided.

```bash
gcloud ai tensorboards describe 12345
```

--------------------------------

### Create a Service Perimeter

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/perimeters

Use the `create` command to establish a new service perimeter.

```APIDOC
## POST /api/access-context-manager/v1/perimeters

### Description
Creates a new service perimeter.

### Method
POST

### Endpoint
`/api/access-context-manager/v1/perimeters`

### Parameters
#### Query Parameters
- **parent** (string) - Required - The name of the parent resource (e.g., `organizations/123`).

#### Request Body
- **name** (string) - Required - The name of the Service Perimeter to create. Example: `projects/my-project/servicePerimeters/myPerimeter`.
- **title** (string) - Optional - A human-readable title for the Service Perimeter.
- **resources** (array of strings) - Optional - A list of Google Cloud resource names that are part of this Service Perimeter. Example: `["projects/12345"]`.
- **restrictedServices** (array of strings) - Optional - A list of Google Cloud services that are restricted from being accessed from outside the perimeter. Example: `["storage.googleapis.com"]`.
- **ingressPolicies** (array of objects) - Optional - Defines the conditions for traffic ingress into the perimeter.
- **egressPolicies** (array of objects) - Optional - Defines the conditions for traffic egress from the perimeter.

### Request Example
```json
{
  "name": "organizations/123/locations/global/servicePerimeters/myPerimeter",
  "title": "My Perimeter",
  "resources": ["projects/12345"]
}
```

### Response
#### Success Response (200)
- **name** (string) - The resource name of the Service Perimeter.
- **title** (string) - The human-readable title of the Service Perimeter.
- **resources** (array of strings) - The list of Google Cloud resources included in the perimeter.
- **restrictedServices** (array of strings) - The list of restricted services.
- **ingressPolicies** (array of objects) - The ingress policies.
- **egressPolicies** (array of objects) - The egress policies.

#### Response Example
```json
{
  "name": "organizations/123/locations/global/servicePerimeters/myPerimeter",
  "title": "My Perimeter",
  "resources": ["projects/12345"],
  "restrictedServices": [],
  "ingressPolicies": [],
  "egressPolicies": []
}
```
```

--------------------------------

### Beta version of gcloud ai models copy

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/models/copy

This command is a beta version for copying AI models. It offers more stability than alpha but may still undergo changes.

```bash
gcloud beta ai models copy
```

--------------------------------

### Create an access policy with HTTP logging

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy and enables HTTP logging. The `--log-http` flag is useful for debugging by showing the raw HTTP requests and responses.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --title="My HTTP Log Policy" --log-http
```

--------------------------------

### List AlloyDB Users (Beta)

Source: https://docs.cloud.google.com/sdk/gcloud/reference/alloydb/users/list

This command is part of the beta release for managing AlloyDB users. It offers more stability than alpha but may still evolve.

```bash
gcloud beta alloydb users list
```

--------------------------------

### Create an access policy asynchronously

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy and returns immediately without waiting for the operation to complete. This is useful for scripting or when you don't need to monitor the creation process in real-time.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --title="My Policy" --async
```

--------------------------------

### Create an access policy with a billing project

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy and specifies a billing project. The `--billing-project` flag is used to associate the operation with a specific billing project.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --title="My Billing Project Policy" --billing-project=my-billing-project
```

--------------------------------

### Deploy Model to Vertex AI

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/model-garden/models/deploy

This snippet demonstrates how to deploy a model from the Model Garden to Vertex AI, specifying various configuration options.

```APIDOC
## POST /v1/projects/{projectId}/locations/{locationId}/endpoints/{endpointId}:deployModel

### Description
Deploys a model from the Model Garden to a Vertex AI endpoint.

### Method
POST

### Endpoint
`/v1/projects/{projectId}/locations/{locationId}/endpoints/{endpointId}:deployModel`

### Parameters
#### Query Parameters
- `--container-image` (string) - Required - URI of the Model serving container file in the Container Registry (e.g. gcr.io/myproject/server:latest).
- `--container-ports` (list of numbers) - Container ports to receive http requests at. Must be a number between 1 and 65535, inclusive.
- `--container-predict-route` (string) - HTTP path to send prediction requests to inside the container.
- `--container-shared-memory-size-mb` (number) - The amount of the VM memory to reserve as the shared memory for the model in megabytes.
- `--container-startup-probe-exec` (list of strings) - Exec specifies the action to take. Used by startup probe. An example of this argument would be ["cat", "/tmp/healthy"].
- `--container-startup-probe-period-seconds` (number) - How often (in seconds) to perform the startup probe. Default to 10 seconds. Minimum value is 1.
- `--container-startup-probe-timeout-seconds` (number) - Number of seconds after which the startup probe times out. Defaults to 1 second. Minimum value is 1.
- `--disable-dedicated-endpoint` (boolean) - If true, the dedicated endpoint will be disabled and the deployed model will be exposed through the shared DNS.
- `--enable-fast-tryout` (boolean) - If True, model will be deployed using faster deployment path. Useful for quick experiments. Not for production workloads. Only available for most popular models with certain machine types.
- `--endpoint-display-name` (string) - Display name of the endpoint with the deployed model.
- `--hugging-face-access-token` (string) - The access token from Hugging Face needed to read the model artifacts of gated models. It is only needed when the Hugging Face model to deploy is gated.
- `--machine-type` (string) - The machine type to deploy the model to. It should be a supported machine type from the deployment configurations of the model. Use `gcloud ai model-garden models list-deployment-config` to check the supported machine types.
- `--region` (string) - ID of the region or fully qualified identifier for the region.
- `--reservation-affinity` (object) - A ReservationAffinity can be used to configure a Vertex AI resource (e.g., a DeployedModel) to draw its Compute Engine resources from a Shared Reservation, or exclusively from on-demand capacity. Structure: `key`=`KEY`, `reservation-affinity-type`=`RESERVATION-AFFINITY-TYPE`, `values`=`VALUES`.
- `--spot` (boolean) - If true, schedule the deployment workload on Spot VM.
- `--use-dedicated-endpoint` (boolean) - If true, the endpoint will be exposed through a dedicated DNS. Your request to the dedicated endpoint will be isolated from other users' traffic and will have better performance and reliability.

### Request Example
```json
{
  "containerImage": "gcr.io/myproject/server:latest",
  "containerPorts": [8080],
  "containerPredictRoute": "/predict",
  "containerSharedMemorySizeMb": 1024,
  "containerStartupProbeExec": ["cat", "/tmp/healthy"],
  "containerStartupProbePeriodSeconds": 10,
  "containerStartupProbeTimeoutSeconds": 1,
  "disableDedicatedEndpoint": false,
  "enableFastTryout": false,
  "endpointDisplayName": "my-model-endpoint",
  "huggingFaceAccessToken": "hf_token",
  "machineType": "n1-standard-4",
  "region": "us-central1",
  "reservationAffinity": {
    "key": "my-reservation",
    "reservationAffinityType": "SPECIFIC_RESERVATION",
    "values": ["reservation-id-1"]
  },
  "spot": false,
  "useDedicatedEndpoint": true
}
```

### Response
#### Success Response (200)
- `id` (string) - The unique identifier for the deployed model.
- `displayName` (string) - The display name of the deployed model.
- `createTime` (string) - The timestamp when the model was created.

#### Response Example
```json
{
  "id": "1234567890",
  "displayName": "my-model-endpoint",
  "createTime": "2023-10-27T10:00:00Z"
}
```
```

--------------------------------

### gcloud access-context-manager policies describe

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies

Show details about a specific access policy.

```APIDOC
## gcloud access-context-manager policies describe

### Description
Show details about an access policy.

### Method
`gcloud access-context-manager policies describe`

### Endpoint
Not applicable (gcloud command)

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
None (uses gcloud flags)

### Request Example
```bash
gcloud access-context-manager policies describe POLICY_NAME
```

### Response
#### Success Response (200)
Details of the access policy, including its name, parent, and etag.

#### Response Example
```json
{
  "name": "accessPolicies/12345",
  "parent": "organizations/67890",
  "etag": "etag123"
}
```
```

--------------------------------

### Create an access policy with a specific format

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy and specifies the output format. The `--format` flag allows you to control how the command's output is presented, such as JSON or YAML.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --title="My Formatted Policy" --format=json
```

--------------------------------

### Create an access policy with user output enabled

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy and ensures that user output is enabled. The `--user-output-enabled` flag controls whether user-facing output is displayed.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --title="My User Output Policy" --user-output-enabled=true
```

--------------------------------

### Alpha version of describe command

Source: https://docs.cloud.google.com/sdk/gcloud/reference/active-directory/domains/describe

This is an alternative command for describing a Managed Microsoft AD domain using the alpha version of the gcloud CLI.

```bash
gcloud alpha active-directory domains describe
```

--------------------------------

### Create an access policy with a specific account

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy using a specified account. The `--account` flag allows you to authenticate with a particular Google Cloud account.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --title="My Account Policy" --account=user@example.com
```

--------------------------------

### Create an access policy with custom scopes

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command shows how to create an access policy with custom scopes, which can include folders and projects. The `--scopes` flag accepts a comma-separated list of scopes.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --scopes="folders/345,projects/567" --title="My Custom Scopes Policy"
```

--------------------------------

### List Active Directory Peerings (Beta)

Source: https://docs.cloud.google.com/sdk/gcloud/reference/active-directory/peerings/list

This command lists Active Directory peerings using the beta version of the API. Beta features are more stable than alpha but may still evolve.

```bash
gcloud beta active-directory peerings list
```

--------------------------------

### gcloud alpha ai models list

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/models/list

This is an alpha version of the command. Use with caution as it may change or be removed.

```bash
gcloud alpha ai models list
```

--------------------------------

### Create an access policy with alpha version

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy using the alpha version of the gcloud access-context-manager component. Alpha versions may include experimental features and are subject to change.

```bash
gcloud alpha access-context-manager policies create --organization=organizations/123 --title="My Alpha Policy"
```

--------------------------------

### Deploy a Hugging Face model

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/model-garden/models/deploy

Deploy a Hugging Face model by providing its identifier and an access token. This command is suitable for models hosted on Hugging Face.

```bash
gcloud ai model-garden models deploy --model=meta-llama/Meta-Llama-3-8B --hugging-face-access-token={hf_token} --project=example --region=us-central1
```

--------------------------------

### gcloud alpha ai custom-jobs describe

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/custom-jobs/describe

This is an alpha version of the command to describe a custom job. Use with caution as features may change.

```bash
gcloud alpha ai custom-jobs describe
```

--------------------------------

### Configure SSL mode

Source: https://docs.cloud.google.com/sdk/gcloud/reference/alloydb/instances/create-secondary

Specify the SSL mode for instance connections to the database. Default SSL mode matches the primary instance. Options include ALLOW_UNENCRYPTED_AND_ENCRYPTED and ENCRYPTED_ONLY.

```bash
--ssl-mode=`SSL_MODE`
```

--------------------------------

### Access Beta Version of Supported Services

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/supported-services

This command accesses the beta version of the supported-services command group. Beta features are more stable than alpha but may still evolve.

```bash
gcloud beta access-context-manager supported-services
```

--------------------------------

### gcloud access-context-manager policies create

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies

Create a new access policy.

```APIDOC
## gcloud access-context-manager policies create

### Description
Create a new access policy.

### Method
`gcloud access-context-manager policies create`

### Endpoint
Not applicable (gcloud command)

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
None (uses gcloud flags)

### Request Example
```bash
gcloud access-context-manager policies create --organization=ORGANIZATION_ID
```

### Response
None explicitly defined for this command, success is indicated by exit code.
```

--------------------------------

### Create an access policy with verbose logging

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy and enables verbose logging. The `--verbosity` flag can be set to different levels (e.g., debug, info, warning, error) to control the amount of output.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --title="My Verbose Policy" --verbosity=debug
```

--------------------------------

### List Beta AI Platform Jobs

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai-platform/jobs/list

This command lists jobs available in the beta version of AI Platform. Ensure you are using the correct gcloud components for beta releases.

```bash
gcloud beta ai-platform jobs list
```

--------------------------------

### Copy a model as a new version

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/models/copy

Use this command to add a new version of an existing model. Specify the parent model resource name to append the copied model as a new version.

```bash
gcloud ai models copy --source-model=SOURCE_MODEL --destination-parent-model=DESTINATION_PARENT_MODEL
```

--------------------------------

### Create an access policy with a specific project

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy and specifies the project to use for the operation. The `--project` flag sets the default project for the gcloud command.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --title="My Project Specific Policy" --project=my-gcp-project
```

--------------------------------

### Create an access policy scoped to a project

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

Use this command to create an access policy that applies only to a specific project. This limits the scope of service perimeters defined by this policy to the specified project. Ensure the project number is correct.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --scopes=projects/567 --title="My Project Policy"
```

--------------------------------

### Create a new secondary AlloyDB instance

Source: https://docs.cloud.google.com/sdk/gcloud/reference/alloydb/instances/create-secondary

Use this command to create a new secondary instance for your AlloyDB cluster. Ensure you specify the instance name, cluster ID, and region.

```bash
gcloud alloydb instances create-secondary my-instance --cluster=my-cluster --region=us-central1
```

--------------------------------

### Create an access policy with impersonation

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy while impersonating a service account. This is useful for granting specific permissions to a service account to perform this action.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --title="My Impersonated Policy" --impersonate-service-account=my-sa@my-project.iam.gserviceaccount.com
```

--------------------------------

### Alpha version of gcloud ai models copy

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/models/copy

This command is an alpha version for copying AI models. Use with caution as features may change.

```bash
gcloud alpha ai models copy
```

--------------------------------

### gcloud beta alloydb clusters import

Source: https://docs.cloud.google.com/sdk/gcloud/reference/alloydb/clusters/import

This is a beta version of the command for importing data into an AlloyDB cluster. It offers more stability than alpha but may still undergo changes.

```bash
gcloud beta alloydb clusters import
```

--------------------------------

### List models in a specific project and region

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/models/list

Use this command to list all AI models associated with a particular Google Cloud project and region. Ensure you have the correct project ID and region specified.

```bash
gcloud ai models list --project=example --region=us-central1
```

--------------------------------

### Create an access policy scoped to a folder

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy that is restricted to a specific folder. Only projects within this folder can be added to service perimeters defined by this policy. The folder ID must be valid and exist within the specified organization.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --scopes=folders/345 --title="My Folder Policy"
```

--------------------------------

### Copy a model between regions

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/models/copy

Use this command to copy a model from a source project and region to a destination region. Ensure the source model exists and specify both source and destination regions.

```bash
gcloud ai models copy --source-model=projects/example/locations/us-central1/models/123 --region=projects/example/locations/europe-west4
```

--------------------------------

### List Cloud Access Bindings

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/cloud-bindings/list

Lists all cloud access bindings under the specified organization. You can filter, limit, and sort the results.

```APIDOC
## GET /v1/organizations/{parent}/gcpUserAccessBindings

### Description
Lists cloud access bindings under a specified organization.

### Method
GET

### Endpoint
`https://accesscontextmanager.googleapis.com/v1/organizations/{parent}/gcpUserAccessBindings`

### Parameters
#### Path Parameters
- **parent** (string) - Required - The organization to list bindings for. Example: `organizations/12345`.

#### Query Parameters
- **filter** (string) - Optional - An expression to filter the list of bindings. For example, `name.startsWith('organizations/12345/gcpUserAccessBindings/abc')`.
- **pageSize** (integer) - Optional - The maximum number of bindings to return per page.
- **pageToken** (string) - Optional - The page token to retrieve the next page of results.
- **sortBy** (string) - Optional - The field to sort the results by. Example: `name` or `~name` for descending order.

### Response
#### Success Response (200)
- **gcpUserAccessBindings** (array) - A list of gcpUserAccessBindings.
  - **accessLevels** (array) - List of access level resource names.
  - **dryRunAccessLevels** (array) - List of dry run access level resource names.
  - **groupKey** (string) - The email address of the group.
  - **name** (string) - The resource name of the binding.
  - **sessionSettings** (object) - Settings for the session.
    - **sessionLength** (string) - The duration of the session.
    - **sessionLengthEnabled** (boolean) - Whether session length is enabled.
    - **sessionReauthMethod** (string) - The reauthentication method for the session.
  - **scopedAccessSettings** (object) - Settings for scoped access.
    - **activeSettings** (object) - The active access settings.
      - **accessLevels** (array) - List of access level resource names.
      - **sessionSettings** (object) - Settings for the session.
    - **dryRunSettings** (object) - The dry run access settings.
      - **accessLevels** (array) - List of access level resource names.

#### Response Example
```json
{
  "gcpUserAccessBindings": [
    {
      "accessLevels": [
        "accessPolicies/9522/accessLevels/device_trusted"
      ],
      "dryRunAccessLevels": [
        "accessPolicies/9522/accessLevels/specific_location"
      ],
      "groupKey": "a3dad",
      "name": "organizations/256/gcpUserAccessBindings/b3-BhcX_Ud5N",
      "sessionSettings": {
        "sessionLength": "57600s",
        "sessionLengthEnabled": true,
        "sessionReauthMethod": "LOGIN"
      }
    }
  ]
}
```
```

--------------------------------

### gcloud ai model-monitoring-jobs Commands

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/model-monitoring-jobs

Overview of available commands for managing Vertex AI model monitoring jobs.

```APIDOC
## gcloud ai model-monitoring-jobs

### Description
Manage Vertex AI model monitoring jobs.

### Commands
- **create**: Create a new Vertex AI model monitoring job.
- **delete**: Delete an existing Vertex AI model deployment monitoring job.
- **describe**: Get detailed model deployment monitoring job information about the given job id.
- **list**: List the model deployment monitoring jobs of the given project and region.
- **pause**: Pause a running Vertex AI model deployment monitoring job.
- **resume**: Resume a paused Vertex AI model deployment monitoring job.
- **update**: Update an Vertex AI model deployment monitoring job.
```

--------------------------------

### List AlloyDB Users (Alpha)

Source: https://docs.cloud.google.com/sdk/gcloud/reference/alloydb/users/list

This command is part of the alpha release for managing AlloyDB users. Use with caution as features may change.

```bash
gcloud alpha alloydb users list
```

--------------------------------

### Create an access policy with flattened output

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies/create

This command creates an access policy and flattens the output. The `--flatten` flag is useful for simplifying complex nested output structures, making it easier to parse.

```bash
gcloud access-context-manager policies create --organization=organizations/123 --title="My Flattened Policy" --flatten=field
```

--------------------------------

### Access Approval request approval variants

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-approval/requests/approve

Alternative command variants for alpha and beta releases.

```bash
gcloud alpha access-approval requests approve
```

```bash
gcloud beta access-approval requests approve
```

--------------------------------

### List Alpha AI Platform Jobs

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai-platform/jobs/list

This command lists jobs available in the alpha version of AI Platform. Ensure you are using the correct gcloud components for alpha releases.

```bash
gcloud alpha ai-platform jobs list
```

--------------------------------

### gcloud ai model-garden models deploy

Source: https://docs.cloud.google.com/sdk/gcloud/reference/ai/model-garden/models/deploy

Deploys a model from Model Garden to a Vertex AI endpoint. This command supports deploying models from Model Garden, Hugging Face, and custom weights stored in GCS. It allows for detailed configuration of the deployment, including hardware specifications, container settings, and health probes.

```APIDOC
## POST /v1/projects/{projectId}/locations/{locationId}/endpoints/{endpointId}/deployedModels

### Description
Deploys a model from Model Garden to a Vertex AI endpoint.

### Method
POST

### Endpoint
`/v1/projects/{projectId}/locations/{locationId}/endpoints/{endpointId}/deployedModels`

### Parameters
#### Path Parameters
- **projectId** (string) - Required - The Google Cloud project ID.
- **locationId** (string) - Required - The region where the Vertex AI endpoint is located.
- **endpointId** (string) - Required - The ID of the Vertex AI endpoint.

#### Query Parameters
- **--model** (string) - Required - The model to be deployed. Format: `{publisher_name}/{model_name}@{model_version_name}` for Model Garden models, `{model_name}` for Hugging Face models, or `gs://{gcs_bucket_uri}` for custom weights.
- **--accelerator-count** (integer) - Optional - The number of accelerators to use for serving the model. Must be non-negative.
- **--accelerator-type** (string) - Optional - The type of accelerator to use. Must be a supported type for the model.
- **--accept-eula** (boolean) - Optional - If set, the user accepts the End User License Agreement (EULA) of the model.
- **--asynchronous** (boolean) - Optional - If set to true, the command terminates immediately without polling the operation status.
- **--container-args** (list of strings) - Optional - Comma-separated arguments passed to the container image's command.
- **--container-command** (list of strings) - Optional - Entrypoint for the container image.
- **--container-deployment-timeout-seconds** (integer) - Optional - Deployment timeout in seconds.
- **--container-env-vars** (list of key-value pairs) - Optional - Environment variables to set in the container (e.g., `KEY=VALUE`).
- **--container-grpc-ports** (list of integers) - Optional - Container ports for gRPC requests (1-65535).
- **--container-health-probe-exec** (list of strings) - Optional - Exec action for health probe (e.g., `["cat", "/tmp/healthy"]`).
- **--container-health-probe-period-seconds** (integer) - Optional - How often to perform the health probe (default: 10 seconds, min: 1).
- **--container-health-probe-timeout-seconds** (integer) - Optional - Timeout for health probe in seconds (default: 1 second, min: 1).
- **--container-health-route** (string) - Optional - HTTP path for health checks within the container.
- **--container-image-uri** (string) - Optional - The URI of the container image.
- **--container-ports** (list of integers) - Optional - Container ports to receive requests.
- **--container-predict-route** (string) - Optional - HTTP path for prediction requests within the container.
- **--container-shared-memory-size-mb** (integer) - Optional - Shared memory size in MB for the container.
- **--container-startup-probe-exec** (list of strings) - Optional - Exec action for startup probe.
- **--container-startup-probe-period-seconds** (integer) - Optional - How often to perform the startup probe.
- **--container-startup-probe-timeout-seconds** (integer) - Optional - Timeout for startup probe in seconds.
- **--disable-dedicated-endpoint** (boolean) - Optional - Disables the use of a dedicated endpoint.
- **--enable-fast-tryout** (boolean) - Optional - Enables fast tryout mode.
- **--endpoint-display-name** (string) - Optional - Display name for the endpoint.
- **--hugging-face-access-token** (string) - Optional - Access token for Hugging Face models.
- **--machine-type** (string) - Optional - The machine type to use for the deployment.
- **--region** (string) - Optional - The region for the deployment (if not specified in the endpoint).
- **--reservation-affinity** (object) - Optional - Reservation affinity configuration.
- **--spot** (boolean) - Optional - Use spot instances for the deployment.
- **--use-dedicated-endpoint** (boolean) - Optional - Uses a dedicated endpoint for the deployment.

### Request Example
```json
{
  "model": "google/gemma2@gemma-2-9b",
  "project": "example",
  "region": "us-central1"
}
```

### Response
#### Success Response (200)
- **operation** (object) - Details of the long-running operation for deployment.

#### Response Example
```json
{
  "operation": {
    "name": "projects/example/locations/us-central1/operations/1234567890",
    "metadata": {
      "@type": "type.googleapis.com/google.cloud.aiplatform.v1.DeploymentModelOperationMetadata"
    },
    "done": false
  }
}
```
```

--------------------------------

### gcloud access-context-manager policies list

Source: https://docs.cloud.google.com/sdk/gcloud/reference/access-context-manager/policies

List all access policies within an organization.

```APIDOC
## gcloud access-context-manager policies list

### Description
List access policies.

### Method
`gcloud access-context-manager policies list`

### Endpoint
Not applicable (gcloud command)

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
None (uses gcloud flags)

### Request Example
```bash
gcloud access-context-manager policies list --organization=ORGANIZATION_ID
```

### Response
#### Success Response (200)
A list of access policies, each with its name, parent, and etag.

#### Response Example
```json
[
  {
    "name": "accessPolicies/12345",
    "parent": "organizations/67890",
    "etag": "etag123"
  },
  {
    "name": "accessPolicies/67890",
    "parent": "organizations/67890",
    "etag": "etag456"
  }
]
```
```

--------------------------------

### Describe a Managed Microsoft AD domain

Source: https://docs.cloud.google.com/sdk/gcloud/reference/active-directory/domains/describe

Use this command to view metadata for a specific Managed Microsoft AD domain. Ensure the domain name is accurate and your account has the necessary permissions.

```bash
gcloud active-directory domains describe my-domain.com
```

--------------------------------

### gcloud wide flags

Source: https://docs.cloud.google.com/sdk/gcloud/reference/alloydb/instances/create-secondary

Global flags available for all gcloud commands, including --access-token-file, --account, --billing-project, and others. Run '$ gcloud help' for details.

```bash
--access-token-file
     --account
     --billing-project
     --configuration
     --flags-file
     --flatten
     --format
     --help
     --impersonate-service-account
     --log-http
     --project
     --quiet
     --trace-token
     --user-output-enabled
     --verbosity
```
