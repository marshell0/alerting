[![Test Workflow](https://github.com/opendistro-for-elasticsearch/alerting/workflows/Test%20Workflow/badge.svg)](https://github.com/opendistro-for-elasticsearch/alerting/actions)
[![codecov](https://codecov.io/gh/opendistro-for-elasticsearch/alerting/branch/main/graph/badge.svg)](https://codecov.io/gh/opendistro-for-elasticsearch/alerting)
[![Documentation](https://img.shields.io/badge/api-reference-blue.svg)](https://opendistro.github.io/for-elasticsearch-docs/docs/alerting/api/)
[![Chat](https://img.shields.io/badge/chat-on%20forums-blue)](https://discuss.opendistrocommunity.dev/c/alerting/)
![PRs welcome!](https://img.shields.io/badge/PRs-welcome!-success)

# Changes made on orginal version
1. `alerting\notification\src\main\java\com\amazon\opendistroforelasticsearch\alerting\destination\client\DestinationEmailClient.java` 
   Added HTML content support to the email body, but still support original pure text format, which format will be used depends on the email content, if there is HTML tag then HTML format, or pure text
1. `alerting\alerting\src\main\kotlin\com\amazon\opendistroforelasticsearch\alerting\model\destination\DestinationContextFactory.kt` 
   Added support to username and password authentication for plan text protocol, original code only read usename/password if the protocol is TLS/HTTPS protocol 
1. `alerting\alerting\src\main\kotlin\com\amazon\opendistroforelasticsearch\alerting\script\TriggerExecutionContext.kt`
   Changed the notification PeriodStart & PeriodEnd to local time zone

# Open Distro for Elasticsearch Alerting

### Building from the command line

1. `gradle build -x :alerting:integTest -x :alerting:jacocoTestReport -x :ktlint` builds subprojects, deliverable may need to be renamed.
