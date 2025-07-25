# Inspector

The [Amazon Inspector](https://docs.aws.amazon.com/inspector/) integration collects and parses data from Amazon Inspector [Findings](https://docs.aws.amazon.com/inspector/v2/APIReference/API_ListFindings.html) REST APIs.

**IMPORTANT: Extra AWS charges on API requests will be generated by this integration. Check [API Requests](https://www.elastic.co/docs/current/integrations/aws#api-requests) for more details.**

## Compatibility
This module is tested against `Amazon Inspector API version 2.0`.

## Agentless-enabled integration

Agentless integrations allow you to collect data without having to manage Elastic Agent in your cloud. They make manual agent deployment unnecessary, so you can focus on your data instead of the agent that collects it. For more information, refer to [Agentless integrations](https://www.elastic.co/guide/en/serverless/current/security-agentless-integrations.html) and the [Agentless integrations FAQ](https://www.elastic.co/guide/en/serverless/current/agentless-integration-troubleshooting.html).

Agentless deployments are only supported in Elastic Serverless and Elastic Cloud environments. This functionality is in beta and is subject to change. Beta features are not subject to the support SLA of official GA features.

## To collect data from Amazon Inspector API, users must have an Access Key and a Secret Key. To create API token follow below steps:

  1. Login to https://console.aws.amazon.com/.
  2. Go to https://console.aws.amazon.com/iam/ to access the IAM console.
  3. On the navigation menu, choose Users.
  4. Choose your IAM user name.
  5. Select Create access key from the Security Credentials tab.
  6. To see the new access key, choose Show.

## Note

  - For the current integration package, it is compulsory to add Secret Access Key and Access Key ID.
  - This data stream doesn't support setting a Role ARN.
  - Ensure your IAM has the `inspector2:ListFindings` permission granted. Without this permission, API requests will be denied.

## Logs

### Inspector

This is the [`Inspector`](https://docs.aws.amazon.com/inspector/v2/APIReference/API_ListFindings.html#inspector2-ListFindings-response-findings) data stream.

{{event "inspector"}}

**ECS Field Reference**

Please refer to the following [document](https://www.elastic.co/guide/en/ecs/current/ecs-field-reference.html) for detailed information on ECS fields.

{{fields "inspector"}}
