# New Relic Interview Questions & Answers

> A curated list of New Relic interview questions covering Fundamentals, the New Relic One Platform, APM, Java Agent Monitoring, Distributed Tracing, OpenTelemetry Integration, Infrastructure Monitoring, Kubernetes Monitoring, Logs Management, NRQL, Dashboards & Visualization, Alerting & Incident Management, SRE & Reliability Engineering, Cloud Monitoring, and Advanced & Scenario-Based Questions — each with a clear explanation and Java code example or NRQL query where applicable.

---

### Table of Contents

<details open>
<summary>
Hide/Show table of contents
</summary>

| No. | Questions |
| --- | --------- |
|     | **New Relic Fundamentals** |
| 1 | [What is New Relic and how does it differ from traditional monitoring tools?](#what-is-new-relic-and-how-does-it-differ-from-traditional-monitoring-tools) |
| 2 | [What are the core components of the New Relic platform?](#what-are-the-core-components-of-the-new-relic-platform) |
| 3 | [What is observability, and how does New Relic support it?](#what-is-observability-and-how-does-new-relic-support-it) |
| 4 | [What types of telemetry data does New Relic collect?](#what-types-of-telemetry-data-does-new-relic-collect) |
| 5 | [What is the difference between monitoring and observability?](#what-is-the-difference-between-monitoring-and-observability) |
| 6 | [Explain the New Relic architecture](#explain-the-new-relic-architecture) |
| 7 | [What are the key use cases of New Relic in enterprise applications?](#what-are-the-key-use-cases-of-new-relic-in-enterprise-applications) |
| 8 | [What are the advantages of SaaS-based monitoring platforms like New Relic?](#what-are-the-advantages-of-saas-based-monitoring-platforms-like-new-relic) |
| 9 | [How does New Relic provide end-to-end visibility across distributed systems?](#how-does-new-relic-provide-end-to-end-visibility-across-distributed-systems) |
| 10 | [What licensing models are available in New Relic?](#what-licensing-models-are-available-in-new-relic) |
|     | **New Relic One Platform** |
| 11 | [What is New Relic One?](#what-is-new-relic-one) |
| 12 | [What are the major capabilities of New Relic One?](#what-are-the-major-capabilities-of-new-relic-one) |
| 13 | [How does New Relic One unify logs, metrics, traces and events?](#how-does-new-relic-one-unify-logs-metrics-traces-and-events) |
| 14 | [What is the Entity Explorer?](#what-is-the-entity-explorer) |
| 15 | [What are workloads in New Relic?](#what-are-workloads-in-new-relic) |
| 16 | [How do you organize services within New Relic?](#how-do-you-organize-services-within-new-relic) |
| 17 | [What are tags and labels in New Relic?](#what-are-tags-and-labels-in-new-relic) |
| 18 | [What is the purpose of the Service Map?](#what-is-the-purpose-of-the-service-map) |
| 19 | [How does New Relic support multi-cloud environments?](#how-does-new-relic-support-multi-cloud-environments) |
| 20 | [What are the benefits of a unified observability platform?](#what-are-the-benefits-of-a-unified-observability-platform) |
|     | **APM (Application Performance Monitoring)** |
| 21 | [What is APM in New Relic?](#what-is-apm-in-new-relic) |
| 22 | [How does New Relic APM monitor application performance?](#how-does-new-relic-apm-monitor-application-performance) |
| 23 | [What metrics are typically collected by APM agents?](#what-metrics-are-typically-collected-by-apm-agents) |
| 24 | [What is transaction tracing?](#what-is-transaction-tracing) |
| 25 | [What is a transaction in New Relic?](#what-is-a-transaction-in-new-relic) |
| 26 | [What is throughput in APM?](#what-is-throughput-in-apm) |
| 27 | [What is Apdex score?](#what-is-apdex-score) |
| 28 | [How is Apdex calculated?](#how-is-apdex-calculated) |
| 29 | [What factors affect Apdex scores?](#what-factors-affect-apdex-scores) |
| 30 | [What is response time in APM?](#what-is-response-time-in-apm) |
| 31 | [What is error rate in New Relic?](#what-is-error-rate-in-new-relic) |
| 32 | [How do you identify slow transactions?](#how-do-you-identify-slow-transactions) |
| 33 | [What is transaction breakdown analysis?](#what-is-transaction-breakdown-analysis) |
| 34 | [What is transaction trace sampling?](#what-is-transaction-trace-sampling) |
| 35 | [What is thread profiling in New Relic?](#what-is-thread-profiling-in-new-relic) |
| 36 | [What is CPU profiling?](#what-is-cpu-profiling) |
| 37 | [What is code-level visibility?](#what-is-code-level-visibility) |
| 38 | [What are custom transactions?](#what-are-custom-transactions) |
| 39 | [How do you instrument custom methods?](#how-do-you-instrument-custom-methods) |
| 40 | [What are transaction naming strategies?](#what-are-transaction-naming-strategies) |
|     | **Java Agent Monitoring** |
| 41 | [How does the New Relic Java Agent work?](#how-does-the-new-relic-java-agent-work) |
| 42 | [How do you install a Java agent in a Spring Boot application?](#how-do-you-install-a-java-agent-in-a-spring-boot-application) |
| 43 | [What JVM metrics are collected by New Relic?](#what-jvm-metrics-are-collected-by-new-relic) |
| 44 | [How does New Relic monitor garbage collection?](#how-does-new-relic-monitor-garbage-collection) |
| 45 | [How does New Relic monitor memory utilization?](#how-does-new-relic-monitor-memory-utilization) |
| 46 | [What JVM thread metrics are available?](#what-jvm-thread-metrics-are-available) |
| 47 | [How does New Relic detect slow JDBC queries?](#how-does-new-relic-detect-slow-jdbc-queries) |
| 48 | [How are external service calls monitored?](#how-are-external-service-calls-monitored) |
| 49 | [How do you configure custom instrumentation in Java?](#how-do-you-configure-custom-instrumentation-in-java) |
| 50 | [What is the role of newrelic.yml?](#what-is-the-role-of-newrelicyml) |
| 51 | [How do you enable distributed tracing in Java applications?](#how-do-you-enable-distributed-tracing-in-java-applications) |
| 52 | [How do you monitor Kafka consumers using New Relic?](#how-do-you-monitor-kafka-consumers-using-new-relic) |
| 53 | [How do you monitor Spring Boot Actuator metrics?](#how-do-you-monitor-spring-boot-actuator-metrics) |
| 54 | [How do you troubleshoot agent connectivity issues?](#how-do-you-troubleshoot-agent-connectivity-issues) |
| 55 | [What are common performance overhead concerns with agents?](#what-are-common-performance-overhead-concerns-with-agents) |
|     | **Distributed Tracing** |
| 56 | [What is distributed tracing?](#what-is-distributed-tracing) |
| 57 | [Why is distributed tracing important in microservices?](#why-is-distributed-tracing-important-in-microservices) |
| 58 | [How does New Relic implement distributed tracing?](#how-does-new-relic-implement-distributed-tracing) |
| 59 | [What is a trace?](#what-is-a-trace) |
| 60 | [What is a span?](#what-is-a-span) |
| 61 | [What information does a span contain?](#what-information-does-a-span-contain) |
| 62 | [How do parent and child spans work?](#how-do-parent-and-child-spans-work) |
| 63 | [How do traces help identify bottlenecks?](#how-do-traces-help-identify-bottlenecks) |
| 64 | [What is W3C Trace Context?](#what-is-w3c-trace-context) |
| 65 | [What is trace propagation?](#what-is-trace-propagation) |
| 66 | [How does New Relic integrate with OpenTelemetry tracing?](#how-does-new-relic-integrate-with-opentelemetry-tracing) |
| 67 | [How do you troubleshoot broken traces?](#how-do-you-troubleshoot-broken-traces) |
| 68 | [What is span enrichment?](#what-is-span-enrichment) |
| 69 | [How can custom attributes be added to traces?](#how-can-custom-attributes-be-added-to-traces) |
| 70 | [How do you analyze service dependencies using traces?](#how-do-you-analyze-service-dependencies-using-traces) |
|     | **OpenTelemetry Integration** |
| 71 | [What is OpenTelemetry?](#what-is-opentelemetry) |
| 72 | [Why is OpenTelemetry becoming an industry standard?](#why-is-opentelemetry-becoming-an-industry-standard) |
| 73 | [How does New Relic support OpenTelemetry?](#how-does-new-relic-support-opentelemetry) |
| 74 | [What is the OpenTelemetry Collector?](#what-is-the-opentelemetry-collector) |
| 75 | [What telemetry signals are supported by OpenTelemetry?](#what-telemetry-signals-are-supported-by-opentelemetry) |
| 76 | [What is auto-instrumentation?](#what-is-auto-instrumentation) |
| 77 | [What is manual instrumentation?](#what-is-manual-instrumentation) |
| 78 | [How do you export OpenTelemetry data to New Relic?](#how-do-you-export-opentelemetry-data-to-new-relic) |
| 79 | [What are resource attributes in OpenTelemetry?](#what-are-resource-attributes-in-opentelemetry) |
| 80 | [What is baggage propagation?](#what-is-baggage-propagation) |
| 81 | [What are semantic conventions in OpenTelemetry?](#what-are-semantic-conventions-in-opentelemetry) |
| 82 | [How do you instrument a Spring Boot application using OpenTelemetry?](#how-do-you-instrument-a-spring-boot-application-using-opentelemetry) |
| 83 | [What are the advantages of OpenTelemetry over vendor-specific agents?](#what-are-the-advantages-of-opentelemetry-over-vendor-specific-agents) |
| 84 | [How do traces and metrics correlate in OpenTelemetry?](#how-do-traces-and-metrics-correlate-in-opentelemetry) |
| 85 | [What challenges arise during OpenTelemetry adoption?](#what-challenges-arise-during-opentelemetry-adoption) |
|     | **Infrastructure Monitoring** |
| 86 | [What is Infrastructure Monitoring in New Relic?](#what-is-infrastructure-monitoring-in-new-relic) |
| 87 | [How do Infrastructure Agents work?](#how-do-infrastructure-agents-work) |
| 88 | [What metrics are collected from Linux servers?](#what-metrics-are-collected-from-linux-servers) |
| 89 | [What metrics are collected from Windows servers?](#what-metrics-are-collected-from-windows-servers) |
| 90 | [How do you monitor Kubernetes clusters?](#how-do-you-monitor-kubernetes-clusters) |
| 91 | [How do you monitor Docker containers?](#how-do-you-monitor-docker-containers) |
| 92 | [What is host inventory data?](#what-is-host-inventory-data) |
| 93 | [How does New Relic monitor CPU utilization?](#how-does-new-relic-monitor-cpu-utilization) |
| 94 | [How does New Relic monitor memory consumption?](#how-does-new-relic-monitor-memory-consumption) |
| 95 | [How do you identify resource bottlenecks?](#how-do-you-identify-resource-bottlenecks) |
| 96 | [How do you monitor disk I/O performance?](#how-do-you-monitor-disk-io-performance) |
| 97 | [What is process monitoring?](#what-is-process-monitoring) |
| 98 | [How do you monitor cloud infrastructure?](#how-do-you-monitor-cloud-infrastructure) |
| 99 | [What are Infrastructure Events?](#what-are-infrastructure-events) |
| 100 | [How do you create infrastructure dashboards?](#how-do-you-create-infrastructure-dashboards) |
|     | **Kubernetes Monitoring** |
| 101 | [How does New Relic monitor Kubernetes clusters?](#how-does-new-relic-monitor-kubernetes-clusters-1) |
| 102 | [What Kubernetes metrics are available?](#what-kubernetes-metrics-are-available) |
| 103 | [How do you install New Relic on AKS?](#how-do-you-install-new-relic-on-aks) |
| 104 | [How do you install New Relic on EKS?](#how-do-you-install-new-relic-on-eks) |
| 105 | [How do you install New Relic on GKE?](#how-do-you-install-new-relic-on-gke) |
| 106 | [What is kube-state-metrics?](#what-is-kube-state-metrics) |
| 107 | [How do you identify unhealthy pods?](#how-do-you-identify-unhealthy-pods) |
| 108 | [How do you troubleshoot pod restarts?](#how-do-you-troubleshoot-pod-restarts) |
| 109 | [What Kubernetes dashboards are available?](#what-kubernetes-dashboards-are-available) |
| 110 | [How do you monitor node utilization?](#how-do-you-monitor-node-utilization) |
| 111 | [How do you monitor namespaces?](#how-do-you-monitor-namespaces) |
| 112 | [How do you analyze container resource consumption?](#how-do-you-analyze-container-resource-consumption) |
| 113 | [What is Cluster Explorer?](#what-is-cluster-explorer) |
| 114 | [How do you monitor deployments and ReplicaSets?](#how-do-you-monitor-deployments-and-replicasets) |
| 115 | [How do you correlate Kubernetes issues with application traces?](#how-do-you-correlate-kubernetes-issues-with-application-traces) |
|     | **Logs Management** |
| 116 | [What is New Relic Logs?](#what-is-new-relic-logs) |
| 117 | [How are logs ingested into New Relic?](#how-are-logs-ingested-into-new-relic) |
| 118 | [What log forwarding options are available?](#what-log-forwarding-options-are-available) |
| 119 | [What is log parsing?](#what-is-log-parsing) |
| 120 | [What are structured logs?](#what-are-structured-logs) |
| 121 | [What are unstructured logs?](#what-are-unstructured-logs) |
| 122 | [How do you correlate logs with traces?](#how-do-you-correlate-logs-with-traces) |
| 123 | [What is logs-in-context?](#what-is-logs-in-context) |
| 124 | [How do you search logs efficiently?](#how-do-you-search-logs-efficiently) |
| 125 | [What are log patterns?](#what-are-log-patterns) |
| 126 | [How do you detect anomalies in logs?](#how-do-you-detect-anomalies-in-logs) |
| 127 | [How do you create log alerts?](#how-do-you-create-log-alerts) |
| 128 | [What are common log ingestion challenges?](#what-are-common-log-ingestion-challenges) |
| 129 | [How do you reduce log costs?](#how-do-you-reduce-log-costs) |
| 130 | [What log retention options are available?](#what-log-retention-options-are-available) |
|     | **NRQL (New Relic Query Language)** |
| 131 | [What is NRQL?](#what-is-nrql) |
| 132 | [How is NRQL different from SQL?](#how-is-nrql-different-from-sql) |
| 133 | [What are Events in NRQL?](#what-are-events-in-nrql) |
| 134 | [What are Metrics in NRQL?](#what-are-metrics-in-nrql) |
| 135 | [What are Facets in NRQL?](#what-are-facets-in-nrql) |
| 136 | [What is TIMESERIES?](#what-is-timeseries) |
| 137 | [What are SINCE and UNTIL?](#what-are-since-and-until) |
| 138 | [How do you aggregate data in NRQL?](#how-do-you-aggregate-data-in-nrql) |
| 139 | [How do you calculate average response time using NRQL?](#how-do-you-calculate-average-response-time-using-nrql) |
| 140 | [How do you calculate error percentage using NRQL?](#how-do-you-calculate-error-percentage-using-nrql) |
| 141 | [How do you filter data using WHERE clauses?](#how-do-you-filter-data-using-where-clauses) |
| 142 | [What is FACET in NRQL?](#what-is-facet-in-nrql) |
| 143 | [How do you query logs using NRQL?](#how-do-you-query-logs-using-nrql) |
| 144 | [What are nested aggregations?](#what-are-nested-aggregations) |
| 145 | [What are subqueries in NRQL?](#what-are-subqueries-in-nrql) |
| 146 | [What is rate() in NRQL?](#what-is-rate-in-nrql) |
| 147 | [What is percentile() in NRQL?](#what-is-percentile-in-nrql) |
| 148 | [What is uniqueCount()?](#what-is-uniquecount) |
| 149 | [How do you optimize NRQL queries?](#how-do-you-optimize-nrql-queries) |
| 150 | [How do you build custom dashboards using NRQL?](#how-do-you-build-custom-dashboards-using-nrql) |
|     | **Dashboards & Visualization** |
| 151 | [What types of visualizations are available in New Relic?](#what-types-of-visualizations-are-available-in-new-relic) |
| 152 | [How do you create custom dashboards?](#how-do-you-create-custom-dashboards) |
| 153 | [What is a dashboard widget?](#what-is-a-dashboard-widget) |
| 154 | [How do you share dashboards?](#how-do-you-share-dashboards) |
| 155 | [What are dashboard permissions?](#what-are-dashboard-permissions) |
| 156 | [How do you create executive dashboards?](#how-do-you-create-executive-dashboards) |
| 157 | [How do you visualize SLA metrics?](#how-do-you-visualize-sla-metrics) |
| 158 | [How do you visualize business KPIs?](#how-do-you-visualize-business-kpis) |
| 159 | [How do you create service health dashboards?](#how-do-you-create-service-health-dashboards) |
| 160 | [What are golden signals dashboards?](#what-are-golden-signals-dashboards) |
|     | **Alerting & Incident Management** |
| 161 | [What are alert policies?](#what-are-alert-policies) |
| 162 | [What are alert conditions?](#what-are-alert-conditions) |
| 163 | [What is baseline alerting?](#what-is-baseline-alerting) |
| 164 | [What is static threshold alerting?](#what-is-static-threshold-alerting) |
| 165 | [What is anomaly detection?](#what-is-anomaly-detection) |
| 166 | [What are NRQL alerts?](#what-are-nrql-alerts) |
| 167 | [How do you configure incident preferences?](#how-do-you-configure-incident-preferences) |
| 168 | [What is alert aggregation?](#what-is-alert-aggregation) |
| 169 | [How do you reduce alert fatigue?](#how-do-you-reduce-alert-fatigue) |
| 170 | [What are muting rules?](#what-are-muting-rules) |
| 171 | [How do you configure escalation policies?](#how-do-you-configure-escalation-policies) |
| 172 | [How do you integrate New Relic with PagerDuty?](#how-do-you-integrate-new-relic-with-pagerduty) |
| 173 | [How do you integrate New Relic with Slack?](#how-do-you-integrate-new-relic-with-slack) |
| 174 | [What are workflows in New Relic?](#what-are-workflows-in-new-relic) |
| 175 | [What are issue intelligence capabilities?](#what-are-issue-intelligence-capabilities) |
| 176 | [How do you monitor SLO violations?](#how-do-you-monitor-slo-violations) |
| 177 | [What is alert noise reduction?](#what-is-alert-noise-reduction) |
| 178 | [How do you troubleshoot missing alerts?](#how-do-you-troubleshoot-missing-alerts) |
| 179 | [What is incident correlation?](#what-is-incident-correlation) |
| 180 | [How do you create actionable alerts?](#how-do-you-create-actionable-alerts) |
|     | **SRE & Reliability Engineering** |
| 181 | [What are the Four Golden Signals?](#what-are-the-four-golden-signals) |
| 182 | [How do you measure availability using New Relic?](#how-do-you-measure-availability-using-new-relic) |
| 183 | [What is an SLI?](#what-is-an-sli) |
| 184 | [What is an SLO?](#what-is-an-slo) |
| 185 | [What is an SLA?](#what-is-an-sla) |
| 186 | [How do you create SLOs in New Relic?](#how-do-you-create-slos-in-new-relic) |
| 187 | [What is error budget?](#what-is-error-budget) |
| 188 | [How do you track error budget burn rates?](#how-do-you-track-error-budget-burn-rates) |
| 189 | [How do you monitor reliability trends?](#how-do-you-monitor-reliability-trends) |
| 190 | [How do you perform root cause analysis?](#how-do-you-perform-root-cause-analysis) |
| 191 | [How do you use observability for incident management?](#how-do-you-use-observability-for-incident-management) |
| 192 | [How do you measure service health?](#how-do-you-measure-service-health) |
| 193 | [How do you identify reliability bottlenecks?](#how-do-you-identify-reliability-bottlenecks) |
| 194 | [How do you monitor customer experience?](#how-do-you-monitor-customer-experience) |
| 195 | [How do you establish observability maturity?](#how-do-you-establish-observability-maturity) |
|     | **Cloud Monitoring** |
| 196 | [How does New Relic integrate with AWS?](#how-does-new-relic-integrate-with-aws) |
| 197 | [How does New Relic integrate with Azure?](#how-does-new-relic-integrate-with-azure) |
| 198 | [How does New Relic integrate with GCP?](#how-does-new-relic-integrate-with-gcp) |
| 199 | [What AWS services can be monitored?](#what-aws-services-can-be-monitored) |
| 200 | [How do you monitor Azure AKS clusters?](#how-do-you-monitor-azure-aks-clusters) |
| 201 | [How do you monitor Azure App Services?](#how-do-you-monitor-azure-app-services) |
| 202 | [How do you monitor AWS Lambda functions?](#how-do-you-monitor-aws-lambda-functions) |
| 203 | [What cloud-native metrics are collected?](#what-cloud-native-metrics-are-collected) |
| 204 | [How do you monitor managed databases?](#how-do-you-monitor-managed-databases) |
| 205 | [How do you correlate cloud infrastructure with application performance?](#how-do-you-correlate-cloud-infrastructure-with-application-performance) |
|     | **Advanced & Scenario-Based Questions** |
| 206 | [A Spring Boot application's response time suddenly increases. How would you troubleshoot using New Relic?](#a-spring-boot-applications-response-time-suddenly-increases-how-would-you-troubleshoot-using-new-relic) |
| 207 | [Users report intermittent API failures. How would you identify the root cause?](#users-report-intermittent-api-failures-how-would-you-identify-the-root-cause) |
| 208 | [How would you investigate a memory leak using New Relic?](#how-would-you-investigate-a-memory-leak-using-new-relic) |
| 209 | [How would you analyze high GC pauses in production?](#how-would-you-analyze-high-gc-pauses-in-production) |
| 210 | [How would you identify a slow database query impacting application performance?](#how-would-you-identify-a-slow-database-query-impacting-application-performance) |
| 211 | [How would you troubleshoot Kafka consumer lag using New Relic?](#how-would-you-troubleshoot-kafka-consumer-lag-using-new-relic) |
| 212 | [How would you detect a dependency service outage?](#how-would-you-detect-a-dependency-service-outage) |
| 213 | [How would you monitor a microservices architecture with 100+ services?](#how-would-you-monitor-a-microservices-architecture-with-100-services) |
| 214 | [How would you implement observability for an AKS-hosted Spring Boot platform?](#how-would-you-implement-observability-for-an-aks-hosted-spring-boot-platform) |
| 215 | [How would you create a dashboard for business transactions and technical metrics?](#how-would-you-create-a-dashboard-for-business-transactions-and-technical-metrics) |
| 216 | [How would you monitor a payment processing workflow end-to-end?](#how-would-you-monitor-a-payment-processing-workflow-end-to-end) |
| 217 | [How would you reduce monitoring costs while maintaining observability?](#how-would-you-reduce-monitoring-costs-while-maintaining-observability) |
| 218 | [How would you design alerting for a high-volume e-commerce platform?](#how-would-you-design-alerting-for-a-high-volume-e-commerce-platform) |
| 219 | [How would you implement OpenTelemetry with New Relic in a cloud-native environment?](#how-would-you-implement-opentelemetry-with-new-relic-in-a-cloud-native-environment) |
| 220 | [How would you establish an observability strategy for a large enterprise migrating to microservices?](#how-would-you-establish-an-observability-strategy-for-a-large-enterprise-migrating-to-microservices) |

</details>

---

## New Relic Fundamentals

1. ### What is New Relic and how does it differ from traditional monitoring tools?

   New Relic is a **SaaS observability platform** that collects metrics, traces, logs, and events from applications and infrastructure into a single data store. Traditional "systems monitoring" tools focus on host-level metrics (CPU, memory, disk) and answer the question *"is the server up?"*. New Relic instruments the application code itself with language agents, capturing distributed traces and code-level performance data — answering *"why is this request slow?"*. Key differences:

   - **Full-stack instrumentation** — from browser/mobile through services down to the database, not just the host.
   - **Unified telemetry** — metrics, events, logs, and traces (MELT) correlated in one platform rather than siloed point products.
   - **Ad-hoc analysis** — a query language (NRQL) lets you explore data interactively instead of only viewing pre-built charts.

   **[⬆ Back to Top](#table-of-contents)**

2. ### What are the core components of the New Relic platform?

   The platform is built from four logical layers:

   | Component | Role |
   | --- | --- |
   | **Agents** | Instrument application code and hosts (APM, Infrastructure, Browser, Mobile agents) |
   | **Ingest / Collectors** | Receive telemetry via ingest APIs and the Telemetry SDK |
   | **Telemetry Data Platform** | A cloud-hosted, multi-tenant data lake that stores all signals in a unified schema |
   | **User-facing apps** | New Relic One UI, dashboards, alerts, and the NRQL query interface |

   The four telemetry signals are **M**etrics, **E**vents, **L**ogs, and **T**races — commonly abbreviated **MELT**.

   **[⬆ Back to Top](#table-of-contents)**

3. ### What is observability, and how does New Relic support it?

   **Observability** describes how well you can infer the internal state of a system purely by examining its external outputs. A highly observable system lets you answer questions you didn't anticipate when you built it. New Relic supports observability by gathering telemetry across the entire stack — application performance metrics, logs, infrastructure data, browser and mobile data, and distributed traces — and **correlating them in a single platform** so you can pivot from a metric spike to the trace that caused it to the log line that explains it.

   **[⬆ Back to Top](#table-of-contents)**

4. ### What types of telemetry data does New Relic collect?

   New Relic collects the four MELT signals plus synthetic data:

   - **Metrics** — numeric measurements aggregated over time (response time, throughput, CPU).
   - **Events** — discrete, timestamped occurrences with attributes (a `Transaction`, a `K8sPodSample`).
   - **Logs** — textual records, structured or unstructured.
   - **Spans/Traces** — causal chains that follow a request across service boundaries.
   - **Synthetic data** — results from scripted monitors that probe endpoints proactively.

   It can also ingest arbitrary **custom attributes** and **custom events** for domain-specific context (e.g., `orderId`, `tenantId`).

   **[⬆ Back to Top](#table-of-contents)**

5. ### What is the difference between monitoring and observability?

   | | Monitoring | Observability |
   | --- | --- | --- |
   | **Question answered** | "Is a known metric breaching a threshold?" | "Why is the system behaving this way?" |
   | **Failure modes** | Detects *known unknowns* | Explores *unknown unknowns* |
   | **Method** | Pre-defined dashboards and alerts | Ad-hoc querying, drilling into traces and logs |
   | **Data** | Mostly metrics | Metrics + events + logs + traces correlated |

   Monitoring is a **subset** of observability. New Relic aims to provide observability rather than just threshold-watching.

   **[⬆ Back to Top](#table-of-contents)**

6. ### Explain the New Relic architecture.

   The data flow is:

   ```
   [ Apps + Hosts ]                 [ New Relic Cloud ]              [ Users ]
   ┌──────────────┐                 ┌──────────────────┐            ┌──────────────┐
   │ APM agent    │── telemetry ──▶ │ Ingest APIs      │            │ New Relic One│
   │ Infra agent  │   (HTTPS 443)   │       ↓          │            │ Dashboards   │
   │ OTel SDK     │                 │ Telemetry Data   │── query ──▶│ NRQL / NerdGraph
   │ Browser/Mob. │                 │ Platform (store) │            │ Alerts / AI  │
   └──────────────┘                 │       ↓          │            └──────────────┘
                                     │ Alerting / AI    │
                                     └──────────────────┘
   ```

   Agents instrument code and send telemetry to New Relic's ingest endpoints. The data is processed and stored in a multi-tenant cloud data store. Users access it through New Relic One, dashboards, the **NerdGraph GraphQL API**, or the **NRQL** query API. Alerting, anomaly detection, and AI features all run on the same unified data set.

   **[⬆ Back to Top](#table-of-contents)**

7. ### What are the key use cases of New Relic in enterprise applications?

   - **Performance troubleshooting** — pinpoint slow transactions and the code or query responsible.
   - **Root-cause analysis** — correlate metrics, logs, and traces during incidents.
   - **Capacity planning** — use infrastructure metrics to forecast resource needs.
   - **SLA/SLO tracking** — measure and report reliability targets with error budgets.
   - **Microservices & serverless monitoring** — trace requests across dozens of services and Lambda functions.
   - **Synthetic monitoring** — proactively measure uptime and end-user experience from global locations.

   **[⬆ Back to Top](#table-of-contents)**

8. ### What are the advantages of SaaS-based monitoring platforms like New Relic?

   - **No infrastructure to manage** — no monitoring servers, storage, or scaling to operate yourself.
   - **Automatic scaling** — the platform absorbs telemetry spikes without capacity planning on your side.
   - **Unified data** — all signals land in one place, enabling cross-signal correlation.
   - **Frequent feature delivery** — new capabilities ship continuously without upgrades on your end.
   - **Easy collaboration** — dashboards are accessible via a web URL to any authorized teammate.

   The trade-off is recurring cost tied to data volume and reduced control over data residency, which enterprises mitigate with drop rules and retention tuning.

   **[⬆ Back to Top](#table-of-contents)**

9. ### How does New Relic provide end-to-end visibility across distributed systems?

   Each service is instrumented with an agent that creates **distributed traces**. As a request crosses a process boundary, the agent injects trace context (trace ID, span ID) into outgoing headers and extracts it from incoming ones. Each segment becomes a **span** with timing, errors, and custom attributes; spans link into a parent–child tree forming a full trace. When these traces are combined with infrastructure metrics (which host/pod served the request) and logs (correlated by trace ID), you get a complete picture from the user click down to the database query.

   **[⬆ Back to Top](#table-of-contents)**

10. ### What licensing models are available in New Relic?

    New Relic uses a **usage-based pricing model** built on two dimensions:

    - **Data ingest (GB)** — you pay for the volume of telemetry ingested per month.
    - **User seats** — priced by user type (Basic, Core, Full Platform).

    Plan tiers include a **free tier** (100 GB/month ingest, limited users), **Standard**, **Pro**, and **Enterprise** plans that add extended data retention, more full-platform users, and advanced security/compliance. There are also two data options — standard **Data** and **Data Plus** (longer retention, more compliance features). Some newer AI/ML compute features use separate consumption-based pricing.

    > *Pricing details change frequently — always confirm current tiers and limits on New Relic's official pricing documentation.*

    **[⬆ Back to Top](#table-of-contents)**


## New Relic One Platform

11. ### What is New Relic One?

    **New Relic One** is the unified observability platform (the product UI and underlying experience) that brings together telemetry data, dashboards, alerts, incident management, and a marketplace of apps. It provides a **single UI** for exploring applications, services, hosts, Kubernetes clusters, and custom workloads, with everything backed by the same Telemetry Data Platform so you can move seamlessly between signals.

    **[⬆ Back to Top](#table-of-contents)**

12. ### What are the major capabilities of New Relic One?

    | Capability | Purpose |
    | --- | --- |
    | **Entity Explorer** | Browse all instrumented entities (apps, hosts, DBs, containers) |
    | **Workloads** | Group related entities into business/team units |
    | **Dashboards** | Custom NRQL-driven visualizations |
    | **NRQL** | Query language for all telemetry |
    | **Alerts & AI** | Conditions, anomaly detection, incident correlation |
    | **Distributed Tracing** | Cross-service request analysis |
    | **Service Maps** | Visual dependency topology |
    | **Instant Observability (I/O)** | Marketplace of quickstarts, dashboards, and custom apps |

    **[⬆ Back to Top](#table-of-contents)**

13. ### How does New Relic One unify logs, metrics, traces and events?

    All telemetry flows into the **Telemetry Data Platform** and is stored under a **unified schema**. Because every signal lives in the same store, you can query across metrics, events, logs, and traces with a single language (NRQL) and visualize them together on one dashboard. **Linking attributes** — most importantly `trace.id` and `span.id` — let New Relic stitch a log line to the span it came from and to the metric it influenced, enabling logs-in-context and one-click pivots between signals.

    **[⬆ Back to Top](#table-of-contents)**

14. ### What is the Entity Explorer?

    The **Entity Explorer** is the UI surface that lists every instrumented **entity** — applications, services, databases, hosts, containers, Lambda functions, and more. It organizes entities by account and domain (APM, Infrastructure, Browser, Mobile, Synthetics) and gives quick access to each entity's performance data, relationships, and dependency maps. An "entity" is any object New Relic can monitor and that has a unique GUID.

    **[⬆ Back to Top](#table-of-contents)**

15. ### What are workloads in New Relic?

    A **workload** is a logical group of entities (services, hosts, containers) that together represent a business function or a team's area of ownership — for example, "Checkout Platform" might bundle the cart service, payment service, their databases, and the hosts they run on. Workloads let you create dashboards, SLOs, and alert policies scoped to exactly that set of entities, and they roll up health status so you can see the function's overall state at a glance.

    **[⬆ Back to Top](#table-of-contents)**

16. ### How do you organize services within New Relic?

    Services are organized through several mechanisms that can be combined:

    - **Tags** — key–value attributes (`team:payments`, `env:prod`, `region:us-east`) used for grouping, filtering, and alert conditions.
    - **Labels** — a legacy, value-less form of tagging (prefer tags).
    - **Workloads** — explicit groupings for a business function.
    - **Account / sub-account structure** — separation by environment or business unit.
    - **Domain** — APM vs Infrastructure vs Browser, etc.

    **[⬆ Back to Top](#table-of-contents)**

17. ### What are tags and labels in New Relic?

    **Tags** are key–value pairs applied to entities — for example `team:checkout` or `environment:production`. They power grouping, filtering, faceting, and alert scoping. **Labels** are an older feature: simple strings without a value component. Tags supersede labels because the key–value structure is far more expressive and queryable, so the recommendation is to standardize on tags. Tags can be applied manually, via agent configuration, or automatically from cloud integrations.

    **[⬆ Back to Top](#table-of-contents)**

18. ### What is the purpose of the Service Map?

    The **Service Map** visualizes the dependencies between your services, databases, and external calls as a topology graph. Each node is a service or datastore; each edge represents a call with throughput, latency, and error data. It helps you **identify bottlenecks** (a slow downstream dependency lights up), understand **how failures propagate** through a microservices architecture, and onboard engineers by showing how the system actually fits together.

    **[⬆ Back to Top](#table-of-contents)**

19. ### How does New Relic support multi-cloud environments?

    New Relic instruments across **AWS, Azure, GCP, and on-premises** through three avenues: language **agents** in the application, the **Infrastructure agent** on hosts, and **cloud API integrations** that pull metrics directly from the provider (CloudWatch, Azure Monitor, GCP Operations Suite). Because all of this lands in one platform, you can build a single dashboard that shows an AWS RDS database, an Azure App Service, and a GKE pod side by side — eliminating the per-cloud tool sprawl.

    **[⬆ Back to Top](#table-of-contents)**

20. ### What are the benefits of a unified observability platform?

    - **No data silos** — every signal is queryable together, so correlations across metrics, logs, and traces are trivial.
    - **Single source of truth** — teams agree on one view of system health, speeding root-cause analysis.
    - **Faster MTTR** — one-click pivots (metric → trace → log) shorten incident resolution.
    - **Simplified operations** — unified billing, access control, and management instead of stitching multiple vendors together.
    - **Better collaboration** — shared dashboards and a common vocabulary across dev, ops, and SRE.

    **[⬆ Back to Top](#table-of-contents)**


## APM (Application Performance Monitoring)

21. ### What is APM in New Relic?

    **APM (Application Performance Monitoring)** is New Relic's capability for instrumenting application code. It provides language agents for **Java, .NET, Node.js, Python, Go, Ruby, and PHP**. Each agent hooks into the runtime to instrument function calls, record **transactions**, collect metrics (response time, throughput, error rate, Apdex), and capture detailed transaction traces — all with minimal code change.

    **[⬆ Back to Top](#table-of-contents)**

22. ### How does New Relic APM monitor application performance?

    The agent **wraps web framework handlers** and automatically instruments database calls, external HTTP requests, message queues, and (optionally) custom code. For each request it captures the start and end time, builds a segment breakdown, computes the **Apdex** score, and records any errors. This telemetry is transmitted to New Relic and rendered as charts (throughput, response time, error rate) and as drill-down transaction traces.

    ```java
    // The agent instruments this Spring controller automatically — no code needed.
    // It records the transaction name, duration, and any thrown exception.
    @RestController
    public class OrderController {
        @GetMapping("/orders/{id}")
        public Order getOrder(@PathVariable Long id) {
            return orderService.findById(id); // DB call is auto-instrumented too
        }
    }
    ```

    **[⬆ Back to Top](#table-of-contents)**

23. ### What metrics are typically collected by APM agents?

    | Metric | Meaning |
    | --- | --- |
    | **Throughput** | Requests per minute (rpm) |
    | **Average response time** | Mean transaction duration |
    | **Apdex score** | User-satisfaction index (0–1) |
    | **Error rate** | % of transactions ending in error |
    | **CPU & memory usage** | Process resource consumption |
    | **GC activity** | Garbage collection time and frequency |
    | **Database call counts/time** | Query volume and latency |
    | **External service time** | Latency of outbound HTTP calls |

    **[⬆ Back to Top](#table-of-contents)**

24. ### What is transaction tracing?

    **Transaction tracing** captures detailed information about a single transaction (request): the call stack, the timing of individual method/segment calls, every database query, and each external request. Because tracing every transaction would be too costly, the agent **samples** — automatically capturing the slowest and most representative transactions — and sends those full traces to New Relic for analysis. You can also force custom traces via the agent API.

    **[⬆ Back to Top](#table-of-contents)**

25. ### What is a transaction in New Relic?

    A **transaction** represents a single unit of work in your application — typically an inbound HTTP request, but it can also be a background job, a scheduled task, or a message-queue consumption. It encompasses the entire call stack from entry to response and contributes to aggregated metrics like response time, throughput, and Apdex. Transactions are stored as `Transaction` events queryable via NRQL.

    **[⬆ Back to Top](#table-of-contents)**

26. ### What is throughput in APM?

    **Throughput** measures how many transactions the application handles per minute (or second). It quantifies the **load** on the application. Throughput is most useful when correlated with other metrics — a response-time spike that coincides with a throughput surge points to a capacity issue, whereas a response-time spike with flat throughput points to a downstream slowdown.

    ```sql
    SELECT rate(count(*), 1 minute) AS 'Throughput (rpm)'
    FROM Transaction WHERE appName = 'order-service' SINCE 1 hour AGO TIMESERIES
    ```

    **[⬆ Back to Top](#table-of-contents)**

27. ### What is Apdex score?

    **Apdex (Application Performance Index)** is an industry-standard metric that quantifies user satisfaction with response times on a **0 to 1 scale** (1 = all users satisfied). It classifies each request against a threshold **T** into one of three buckets — **Satisfied**, **Tolerating**, or **Frustrated** — and combines them:

    ```
    Apdex = (Satisfied + (Tolerating / 2)) / Total requests
    ```

    Tolerating requests count as half because the user was inconvenienced but not blocked.

    **[⬆ Back to Top](#table-of-contents)**

28. ### How is Apdex calculated?

    1. Define a target threshold **T** (e.g., 0.5 s).
    2. Classify each request:
       - **Satisfied** — response time ≤ T
       - **Tolerating** — T < response time ≤ 4T
       - **Frustrated** — response time > 4T, *or* the request errored
    3. Apply the formula:

    ```
    Apdex = (Satisfied + Tolerating/2) / Total
    ```

    **Worked example** — with T = 0.5 s and 100 requests: 70 satisfied, 20 tolerating, 10 frustrated:

    ```
    Apdex = (70 + 20/2) / 100 = (70 + 10) / 100 = 0.80
    ```

    An Apdex of 0.80 is generally considered "Good".

    **[⬆ Back to Top](#table-of-contents)**

29. ### What factors affect Apdex scores?

    - **High response times** — slow code paths, lock contention, or large payloads.
    - **Database bottlenecks** — unindexed queries, N+1 query patterns.
    - **External API latency** — slow third-party dependencies counted within the transaction.
    - **Unhandled errors** — every errored request is automatically counted as Frustrated.
    - **An unrealistic threshold T** — setting T too low makes a healthy app look bad; too high hides real pain. Choose T from historical percentile data (a common starting point is around the 90th-percentile target).

    **[⬆ Back to Top](#table-of-contents)**

30. ### What is response time in APM?

    **Response time** is the duration between the application receiving a request and sending its response. New Relic reports it as **average**, **median (p50)**, **95th percentile (p95)**, and **99th percentile (p99)**. Percentiles matter more than the average for user experience: an average of 200 ms can hide a p99 of 3 s that frustrates the slowest 1% of users. Always investigate the tail, not just the mean.

    ```sql
    SELECT average(duration), percentile(duration, 50, 95, 99)
    FROM Transaction WHERE appName = 'order-service' SINCE 30 minutes AGO
    ```

    **[⬆ Back to Top](#table-of-contents)**

31. ### What is error rate in New Relic?

    **Error rate** is the percentage of transactions that end in an exception, an HTTP error status (typically 5xx), or another recorded failure. A rising error rate both **triggers alerts** and **lowers Apdex** (errored requests are counted as Frustrated). New Relic's error analytics group errors by class and message so you can see which exception dominates.

    ```sql
    SELECT percentage(count(*), WHERE error IS true) AS 'Error Rate %'
    FROM Transaction WHERE appName = 'order-service' SINCE 1 hour AGO
    ```

    **[⬆ Back to Top](#table-of-contents)**

32. ### How do you identify slow transactions?

    1. In the APM UI, open the **Transactions** tab and sort by **"Most time consuming"** (response time × throughput) — this surfaces transactions that hurt users most, not just the rarely-hit slow ones.
    2. Open a **transaction trace** to see where time is spent (code, DB query, external call).
    3. Cross-check with NRQL for precise filtering:

    ```sql
    SELECT name, average(duration), count(*)
    FROM Transaction WHERE appName = 'order-service'
    SINCE 1 hour AGO FACET name ORDER BY average(duration) DESC LIMIT 20
    ```

    **[⬆ Back to Top](#table-of-contents)**

33. ### What is transaction breakdown analysis?

    A **transaction breakdown** shows what proportion of a transaction's time is spent in each segment category — application code, database queries, external services, and other (e.g., queueing). This immediately tells you *where* slowness originates: if 80% of time is in the database, you optimize queries; if it's in an external call, you look at the dependency; if it's in app code, you profile the methods.

    **[⬆ Back to Top](#table-of-contents)**

34. ### What is transaction trace sampling?

    Because capturing a full trace for **every** transaction would add unacceptable overhead, the agent **samples** — it captures only the slowest or most representative transactions during each harvest cycle and sends those detailed traces. This keeps overhead low (typically a few percent) while still surfacing the traces that matter for diagnosis. Distributed tracing uses its own sampling configuration (head-based or adaptive).

    **[⬆ Back to Top](#table-of-contents)**

35. ### What is thread profiling in New Relic?

    The **Thread Profiler** captures periodic snapshots of your application's thread stacks over a defined period (e.g., 5 minutes) and aggregates them into a call tree showing where threads spend time. It's invaluable for diagnosing **deadlocks, blocking calls, and CPU hotspots** that don't show up in normal transaction traces. Because it adds overhead while running, it's started on demand and run in controlled windows rather than left on continuously.

    **[⬆ Back to Top](#table-of-contents)**

36. ### What is CPU profiling?

    **CPU profiling** tracks CPU consumption at the method level to identify code paths burning excessive CPU. New Relic's agents include **sampling profilers** that attribute CPU time to transaction segments, so you can see, for example, that a JSON-serialization method is responsible for most of a transaction's CPU. This complements thread profiling, which focuses on *what threads are doing* rather than *raw CPU cost*.

    **[⬆ Back to Top](#table-of-contents)**

37. ### What is code-level visibility?

    **Code-level visibility** is the ability to see exactly which methods or lines of code contribute to latency or errors. New Relic's **CodeStream** integration brings this into the IDE (VS Code, JetBrains), overlaying APM data — slow methods, error rates, golden signals — directly next to the source code, so a developer sees production performance without leaving their editor.

    **[⬆ Back to Top](#table-of-contents)**

38. ### What are custom transactions?

    **Custom transactions** let you instrument non-web work — background jobs, scheduled tasks, queue consumers, batch processors — by explicitly starting and naming a transaction in code. Without this, such work wouldn't appear in the APM UI because there's no web request to hook into. In Java this is most easily done with the `@Trace(dispatcher = true)` annotation, which marks a method as the root of a new transaction.

    ```java
    import com.newrelic.api.agent.Trace;

    public class NightlyReportJob {
        @Trace(dispatcher = true)   // dispatcher=true starts a NEW transaction
        public void generateReport() {
            // This background job now appears as its own transaction in APM
            buildReport();
        }
    }
    ```

    **[⬆ Back to Top](#table-of-contents)**

39. ### How do you instrument custom methods?

    In Java you have two main options: the **`@Trace` annotation** to mark methods as traced segments, and the **agent API** to add custom attributes or create segments programmatically.

    ```java
    import com.newrelic.api.agent.NewRelic;
    import com.newrelic.api.agent.Trace;

    public class PaymentService {

        @Trace(dispatcher = true)               // root transaction
        public void processPayment(Order order) {
            // Attach a custom attribute visible on the transaction and its spans
            NewRelic.addCustomParameter("orderId", order.getId());
            NewRelic.addCustomParameter("amount", order.getAmount());
            validate(order);
            charge(order);
        }

        @Trace                                  // a traced segment within the transaction
        private void charge(Order order) {
            // expensive call you want to see broken out in the trace
        }
    }
    ```

    For classes you can't annotate (third-party libraries), use **XML/YAML custom instrumentation** files instead.

    **[⬆ Back to Top](#table-of-contents)**

40. ### What are transaction naming strategies?

    Good transaction naming groups similar requests so metrics aren't fragmented and cardinality stays manageable:

    - **URI patterns with placeholders** — name `/orders/{id}` rather than `/orders/12345`, `/orders/12346`, … which would create thousands of distinct names.
    - **Framework defaults** — the agent names transactions by controller/action automatically.
    - **Custom naming via the API** — `NewRelic.setTransactionName("Custom", "OrderProcessing")` for fine control.

    The cardinal sin is **high-cardinality names** (embedding IDs), which explode the metric namespace and degrade dashboards. Use parameterized routes.

    ```java
    // Rename a transaction explicitly when the default isn't meaningful
    NewRelic.setTransactionName("Web", "Orders/Process");
    ```

    **[⬆ Back to Top](#table-of-contents)**


## Java Agent Monitoring

41. ### How does the New Relic Java Agent work?

    The New Relic Java Agent is a **`java.lang.instrument` agent** loaded into the JVM via the `-javaagent:newrelic.jar` flag. At class-load time it **modifies bytecode** (using a weaver) to insert hooks into well-known classes — servlets, JDBC drivers, HTTP clients, framework entry points — that measure timing and collect metadata. Because instrumentation happens at the bytecode level, **no source-code changes are required** for the bulk of monitoring; you only write code for custom instrumentation.

    **[⬆ Back to Top](#table-of-contents)**

42. ### How do you install a Java agent in a Spring Boot application?

    Download `newrelic-java.zip`, extract it, and launch the app with the agent attached:

    ```bash
    java -javaagent:/path/to/newrelic/newrelic.jar \
         -Dnewrelic.config.license_key=YOUR_LICENSE_KEY \
         -Dnewrelic.config.app_name="order-service" \
         -jar myapp.jar
    ```

    Place `newrelic.yml` alongside `newrelic.jar`. In **containerized environments**, prefer environment variables over baking secrets into YAML:

    ```dockerfile
    # Dockerfile
    COPY newrelic/ /app/newrelic/
    ENV NEW_RELIC_APP_NAME="order-service"
    ENV NEW_RELIC_LICENSE_KEY="${NEW_RELIC_LICENSE_KEY}"   # injected at runtime, not hardcoded
    ENTRYPOINT ["java","-javaagent:/app/newrelic/newrelic.jar","-jar","/app/myapp.jar"]
    ```

    **[⬆ Back to Top](#table-of-contents)**

43. ### What JVM metrics are collected by New Relic?

    | Category | Metrics |
    | --- | --- |
    | **Heap memory** | Used, committed, max heap; Eden, Survivor, Old Gen |
    | **Non-heap memory** | Metaspace, code cache |
    | **Garbage collection** | GC count, GC time, memory reclaimed (per collector) |
    | **Threads** | Total, daemon, blocked, by state |
    | **CPU** | Process CPU time and utilization |
    | **Class loading** | Loaded/unloaded class counts |
    | **JIT** | Compilation time |

    These help diagnose memory leaks (steadily rising Old Gen), GC pressure (high GC time), and thread exhaustion.

    **[⬆ Back to Top](#table-of-contents)**

44. ### How does New Relic monitor garbage collection?

    The agent reads GC activity through the JVM's monitoring APIs (the `GarbageCollectorMXBean`). It reports **GC counts**, **total time spent in GC**, and **memory reclaimed**, broken down by collector (e.g., G1 Young, G1 Old). High GC time relative to wall-clock time signals **memory pressure or a misconfigured heap** — for example, if the app spends 15% of its time in GC, you likely need a larger heap, fewer allocations, or a different collector. You can query GC as a metric:

    ```sql
    SELECT rate(sum(newrelic.timeslice.value), 1 minute)
    FROM Metric WHERE metricName = 'GC/G1 Young Generation/count'
    AND appName = 'order-service' TIMESERIES SINCE 1 hour AGO
    ```

    **[⬆ Back to Top](#table-of-contents)**

45. ### How does New Relic monitor memory utilization?

    The agent tracks each **heap and non-heap memory pool** over time. The APM **JVMs** page charts **used vs. committed** memory and breaks out Old Generation, Eden space, Survivor space, and Metaspace. A continuously climbing Old Gen that never drops after GC is the classic signature of a **memory leak**. You can set alerts on heap-usage percentage so you're paged before an `OutOfMemoryError`.

    **[⬆ Back to Top](#table-of-contents)**

46. ### What JVM thread metrics are available?

    New Relic reports **total thread count**, **daemon thread count**, **blocked threads**, and threads by **state** (runnable, waiting, timed-waiting, blocked), and it can identify **thread contention**. The **Thread Profiler** complements these aggregate numbers by capturing actual stack traces of long-running or stuck threads — essential for diagnosing deadlocks or a thread pool that's exhausted because every thread is blocked on a slow downstream call.

    **[⬆ Back to Top](#table-of-contents)**

47. ### How does New Relic detect slow JDBC queries?

    The agent instruments common JDBC drivers (MySQL, PostgreSQL, Oracle, SQL Server). For each query it measures **execution time** and captures the **SQL statement** (with parameter values **obfuscated by default** for security). Slow queries appear in the **Databases** tab with average and percentile durations and call counts, and they show up inside the transaction trace that issued them so you can see the calling context.

    ```sql
    -- Find the slowest database operations by total time
    SELECT average(duration), count(*)
    FROM Transaction WHERE appName = 'order-service'
    FACET databaseCallCount SINCE 1 hour AGO
    ```

    **[⬆ Back to Top](#table-of-contents)**

48. ### How are external service calls monitored?

    HTTP client libraries and frameworks — **Apache HttpClient, OkHttp, Spring `RestTemplate`/`WebClient`** — are instrumented to record outbound calls. External-service metrics include **response time, throughput, error rate, and the target host**. These calls also appear in **distributed traces**, so a slow external dependency is visible both as an aggregate metric and as a span within the specific trace that experienced the slowness.

    **[⬆ Back to Top](#table-of-contents)**

49. ### How do you configure custom instrumentation in Java?

    Three approaches, in order of increasing flexibility:

    1. **`@Trace` annotation** — mark your own methods (simplest).
    2. **XML/YAML custom instrumentation** — instrument third-party classes you can't annotate, by dropping a file in the `extensions/` directory.
    3. **Agent API** — programmatic control (custom segments, attributes, metrics).

    ```xml
    <!-- extensions/custom_instrumentation.xml — instrument a third-party class -->
    <extension xmlns="https://newrelic.com/docs/java/xsd/v1.0">
      <instrumentation>
        <pointcut transactionStartPoint="true">
          <className>com.thirdparty.LegacyProcessor</className>
          <method>
            <name>process</name>
            <parameters><type>java.lang.String</type></parameters>
          </method>
        </pointcut>
      </instrumentation>
    </extension>
    ```

    **[⬆ Back to Top](#table-of-contents)**

50. ### What is the role of newrelic.yml?

    `newrelic.yml` is the **agent configuration file**. It sets the application name, license key, log level, distributed-tracing toggle, custom instrumentation, Apdex threshold (`apdex_t`), error-collector behavior, and transaction-naming rules. It lives next to `newrelic.jar`, and **any setting can be overridden by an environment variable** (e.g., `NEW_RELIC_APP_NAME`) — which is the preferred approach in containers so secrets aren't committed to source control.

    ```yaml
    common: &default_settings
      license_key: '${NEW_RELIC_LICENSE_KEY}'
      app_name: order-service
      distributed_tracing:
        enabled: true
      transaction_tracer:
        enabled: true
        record_sql: obfuscated
      error_collector:
        enabled: true
      apdex_t: 0.5
    ```

    **[⬆ Back to Top](#table-of-contents)**

51. ### How do you enable distributed tracing in Java applications?

    Set `distributed_tracing.enabled: true` in `newrelic.yml` (it's on by default in recent agents). The agent then automatically **injects and extracts W3C Trace Context headers** (`traceparent`, `tracestate`) on instrumented HTTP clients and servers. For custom transports or manual propagation, use the API:

    ```java
    import com.newrelic.api.agent.NewRelic;
    import com.newrelic.api.agent.Headers;

    // When making a call over a transport the agent doesn't auto-instrument,
    // inject the trace context so the downstream service continues the trace.
    NewRelic.getAgent().getTransaction()
            .insertDistributedTraceHeaders(myHeadersWrapper);
    ```

    **[⬆ Back to Top](#table-of-contents)**

52. ### How do you monitor Kafka consumers using New Relic?

    Install the New Relic **Java agent**, which includes **Kafka client instrumentation**, or use New Relic's dedicated Kafka integration. The agent instruments the Kafka client library to record **message consumption latency, throughput, and offsets**, and ties consumption into distributed traces (a produced message can carry trace context that the consumer continues). For deeper lag visibility, New Relic also offers an **open-source consumer-lag monitoring** integration.

    ```java
    // The agent instruments the poll loop automatically.
    // Add custom attributes to enrich the consumer transaction:
    while (true) {
        ConsumerRecords<String, String> records = consumer.poll(Duration.ofMillis(500));
        for (ConsumerRecord<String, String> record : records) {
            NewRelic.addCustomParameter("kafka.topic", record.topic());
            NewRelic.addCustomParameter("kafka.partition", record.partition());
            NewRelic.addCustomParameter("kafka.offset", record.offset());
            process(record);
        }
        consumer.commitSync();
    }
    ```

    **[⬆ Back to Top](#table-of-contents)**

53. ### How do you monitor Spring Boot Actuator metrics?

    Spring Boot **Actuator** exposes metrics at `/actuator/metrics` via **Micrometer**. Add the New Relic Micrometer registry to export those metrics to New Relic's dimensional metric store:

    ```groovy
    // build.gradle
    dependencies {
        implementation 'io.micrometer:micrometer-registry-new-relic'
    }
    ```

    ```yaml
    # application.yml
    management:
      metrics:
        export:
          newrelic:
            enabled: true
            api-key: ${NEW_RELIC_INSERT_KEY}
            account-id: ${NEW_RELIC_ACCOUNT_ID}
    ```

    JVM, system, and any custom Micrometer metrics then appear in New Relic's metrics explorer alongside APM data.

    **[⬆ Back to Top](#table-of-contents)**

54. ### How do you troubleshoot agent connectivity issues?

    1. **Check the agent log** — `logs/newrelic_agent.log` carries detailed connection errors; this is the first place to look.
    2. **Verify network reachability** to New Relic endpoints — `collector.newrelic.com` for APM data and `log-api.newrelic.com` for logs, on **port 443 (HTTPS)**.
    3. **Confirm the license key** is correct and matches the region (US vs EU endpoints differ).
    4. **Check proxies/firewalls** allow the outbound HTTPS connection; configure the agent's proxy settings if needed.
    5. **Confirm the app actually receives traffic** — an idle app sends little data.

    **[⬆ Back to Top](#table-of-contents)**

55. ### What are common performance overhead concerns with agents?

    APM agents add overhead from **instrumentation and data transmission** — typically within **5–10% CPU/memory**, but it can climb if deep instrumentation or aggressive transaction tracing is enabled. To keep overhead in check:

    - **Disable unused integrations** and instrumentation modules.
    - **Reduce transaction-trace and distributed-tracing sampling** rates.
    - **Avoid high-cardinality custom attributes** that bloat payloads.
    - **Tune the harvest cycle** and limit custom-event volume.

    The goal is to balance diagnostic depth against the runtime cost.

    **[⬆ Back to Top](#table-of-contents)**


## Distributed Tracing

56. ### What is distributed tracing?

    **Distributed tracing** follows a single request as it travels through multiple services, recording timing for each segment along the way. It produces a holistic view of **latency, errors, and service dependencies** in microservice architectures, transforming a confusing web of service-to-service calls into a single readable timeline that shows exactly where a request spent its time and where it failed.

    **[⬆ Back to Top](#table-of-contents)**

57. ### Why is distributed tracing important in microservices?

    In a microservices system, one user request fans out into many internal calls across many services. Without tracing, when a request is slow you can't tell **which** of a dozen services caused it, or where in the chain an error originated. Distributed tracing **propagates a shared context** (trace ID, span ID) across every hop, pinpointing the bottleneck or failure precisely — turning "the checkout is slow somewhere" into "the inventory service's database call added 1.8 s".

    **[⬆ Back to Top](#table-of-contents)**

58. ### How does New Relic implement distributed tracing?

    New Relic supports the **W3C Trace Context** standard for cross-vendor interoperability. Each instrumented agent **injects** trace headers into outgoing requests and **extracts** them from incoming requests. Every segment of work becomes a **span** with attributes and a parent–child relationship to other spans; together these spans form a **trace**. New Relic also supports **Infinite Tracing** (tail-based sampling) for high-volume systems where you want to keep traces that contain errors or unusual latency regardless of head sampling.

    **[⬆ Back to Top](#table-of-contents)**

59. ### What is a trace?

    A **trace** is the complete collection of spans representing a single request as it moves across services. It has one **root span** (the entry point, with no parent) and any number of **child spans** for downstream calls (HTTP, database, cache). A single **trace ID** ties all the spans together, so the full request journey can be reconstructed and visualized as a waterfall.

    **[⬆ Back to Top](#table-of-contents)**

60. ### What is a span?

    A **span** is a single unit of work within a trace. It has a **start time, duration, operation name, attributes, and a parent span ID**. Examples include an inbound HTTP request to a service, an outbound HTTP call to another service, a database query, or a cache lookup. Spans nest to form the trace's tree structure.

    **[⬆ Back to Top](#table-of-contents)**

61. ### What information does a span contain?

    | Field | Example |
    | --- | --- |
    | **Trace ID** | Links the span to its trace |
    | **Span ID** | Unique identifier for this span |
    | **Parent ID** | The calling span (empty for the root) |
    | **Name / operation** | `GET /orders/{id}`, `SELECT orders` |
    | **Timing** | Start timestamp + duration |
    | **Status / error flag** | Success or failure |
    | **Attributes/tags** | `http.method`, `db.statement`, `http.url` |
    | **Links** | Correlated log IDs |

    These attributes are queryable in NRQL via the `Span` event type.

    **[⬆ Back to Top](#table-of-contents)**

62. ### How do parent and child spans work?

    The **root span** has no parent — it represents the entry point of the request. Every subsequent call creates a **child span** whose parent is the span representing the operation that made the call. This parent–child chaining builds a **tree** that mirrors the actual call graph: service A's span is the parent of the database span it triggered, and so on down the call stack.

    **[⬆ Back to Top](#table-of-contents)**

63. ### How do traces help identify bottlenecks?

    A trace renders as a **waterfall timeline** of spans. By scanning it you can immediately see which span has the **longest duration**, where **errors** were thrown, and how much time was spent **waiting on a dependency** versus doing local work. The longest span (or the gap between a parent and its first child) is usually the prime optimization target — for example, a 2-second database span jumps out visually in an otherwise fast trace.

    **[⬆ Back to Top](#table-of-contents)**

64. ### What is W3C Trace Context?

    **W3C Trace Context** is an open, vendor-neutral standard for propagating trace identifiers across services. It defines two HTTP headers — **`traceparent`** (carries trace ID, parent span ID, and sampling flags) and **`tracestate`** (vendor-specific data). Because it's a shared standard, a trace can flow seamlessly across services instrumented by different vendors and written in different languages, which is why New Relic adopts it.

    **[⬆ Back to Top](#table-of-contents)**

65. ### What is trace propagation?

    **Trace propagation** is the mechanism of carrying trace identifiers (trace ID, span ID, sampling flags) from one service to the next — typically in **HTTP headers** or **message metadata** (for queues like Kafka). Without propagation, each service would start its own disconnected trace and the spans would never link together, defeating the purpose of distributed tracing.

    **[⬆ Back to Top](#table-of-contents)**

66. ### How does New Relic integrate with OpenTelemetry tracing?

    New Relic accepts **OpenTelemetry spans via OTLP** (OpenTelemetry Protocol). You instrument your code with the OpenTelemetry SDK or auto-instrumentation agent, then point the **OTLP exporter** at New Relic's endpoint and include your license key. New Relic also ships its own distribution of the **OpenTelemetry Collector** for aggregating and processing telemetry before export.

    ```bash
    # Environment variables for an OTel-instrumented Java app exporting to New Relic
    export OTEL_EXPORTER_OTLP_ENDPOINT="https://otlp.nr-data.net:4317"
    export OTEL_EXPORTER_OTLP_HEADERS="api-key=YOUR_NEW_RELIC_LICENSE_KEY"
    export OTEL_SERVICE_NAME="order-service"
    java -javaagent:opentelemetry-javaagent.jar -jar myapp.jar
    ```

    **[⬆ Back to Top](#table-of-contents)**

67. ### How do you troubleshoot broken traces?

    A "broken" trace usually means context wasn't propagated across some hop. Check:

    1. **Proxies/load balancers** aren't stripping the `traceparent`/`tracestate` headers.
    2. **Message queues and async calls** carry the context explicitly (async boundaries are a common break point).
    3. **Instrumentation libraries are up to date** and the relevant framework is actually instrumented.
    4. **Custom code isn't dropping headers** when it builds requests manually.

    Use New Relic's **Trace Explorer** to spot missing spans and inspect span attributes for clues about where the chain stopped.

    **[⬆ Back to Top](#table-of-contents)**

68. ### What is span enrichment?

    **Span enrichment** is adding custom attributes to spans to give them business context — `userId`, `orderId`, `region`, `tenantId`. This lets you **filter and analyze traces by business dimensions** ("show me all slow traces for enterprise-tier customers in EU"). Enrichment turns raw technical spans into something analysts and product teams can reason about.

    ```java
    import com.newrelic.api.agent.NewRelic;
    // Enrich the current span/transaction with business context
    NewRelic.addCustomParameter("region", "us-east");
    NewRelic.addCustomParameter("customerTier", "enterprise");
    ```

    **[⬆ Back to Top](#table-of-contents)**

69. ### How can custom attributes be added to traces?

    In Java, call the agent API inside a traced method:

    ```java
    import com.newrelic.api.agent.NewRelic;

    @Trace(dispatcher = true)
    public void processOrder(Order order) {
        // Adds an attribute to the current transaction and its spans
        NewRelic.getAgent().getTransaction()
                .getTracedMethod().addCustomAttribute("orderId", order.getId());

        // Shorthand that attaches to the transaction
        NewRelic.addCustomParameter("paymentMethod", order.getPaymentMethod());
    }
    ```

    These attributes appear on the spans in Trace Explorer and become queryable via NRQL (`SELECT * FROM Span WHERE orderId = '...'`).

    **[⬆ Back to Top](#table-of-contents)**

70. ### How do you analyze service dependencies using traces?

    Use the **Service Map** or **Trace Explorer** to view the sequence of spans and their parent–child relationships. Cross-application traces reveal which services call which, and how often. NRQL on `Span` data quantifies the relationships:

    ```sql
    -- Count inbound root requests to service-A (spans with no parent)
    SELECT count(*) FROM Span
    WHERE service.name = 'service-A' AND parent.id IS NULL
    SINCE 1 hour AGO TIMESERIES

    -- Average duration of calls from service-A to its downstream dependencies
    SELECT average(duration) FROM Span
    WHERE service.name = 'service-A' FACET name SINCE 1 hour AGO
    ```

    **[⬆ Back to Top](#table-of-contents)**


## OpenTelemetry Integration

71. ### What is OpenTelemetry?

    **OpenTelemetry (OTel)** is an open, vendor-neutral standard and toolkit for collecting and exporting telemetry — **traces, metrics, and logs**. Formed by merging the earlier OpenTracing and OpenCensus projects, it provides **APIs, SDKs, and exporters** for many languages, plus the OpenTelemetry Collector. It's a CNCF project and has become the de facto standard for instrumentation.

    **[⬆ Back to Top](#table-of-contents)**

72. ### Why is OpenTelemetry becoming an industry standard?

    Because it is **vendor-neutral**: you instrument your code **once** with OTel APIs and can export the data to **any compatible backend** (New Relic, Jaeger, Prometheus, another vendor) by swapping the exporter configuration. This **eliminates vendor lock-in**, fosters interoperability, and means the instrumentation investment survives a change of observability vendor — which is precisely why cloud providers and observability vendors (New Relic included) have rallied behind it.

    **[⬆ Back to Top](#table-of-contents)**

73. ### How does New Relic support OpenTelemetry?

    New Relic provides **OTLP ingest endpoints** for spans, metrics, and logs, plus a **New Relic distribution of the OpenTelemetry Collector** for aggregating and processing telemetry before export. You can send data directly from an OTel SDK or route it through the Collector. New Relic then treats OTel data as first-class telemetry — building entities, dashboards, and alerts from it just like agent data.

    **[⬆ Back to Top](#table-of-contents)**

74. ### What is the OpenTelemetry Collector?

    The **Collector** is a standalone service that **receives** telemetry from instrumented applications, **processes** it (batching, filtering, sampling, attribute manipulation), and **exports** it to one or more backends. Its pipeline architecture has three stages — **receivers → processors → exporters** — and it can be deployed as an agent (sidecar/DaemonSet) close to the app or as a gateway that aggregates from many sources.

    ```yaml
    # collector-config.yaml
    receivers:
      otlp:
        protocols: { grpc: {}, http: {} }
    processors:
      batch: {}
    exporters:
      otlp:
        endpoint: otlp.nr-data.net:4317
        headers:
          api-key: ${NEW_RELIC_LICENSE_KEY}
    service:
      pipelines:
        traces:  { receivers: [otlp], processors: [batch], exporters: [otlp] }
        metrics: { receivers: [otlp], processors: [batch], exporters: [otlp] }
    ```

    **[⬆ Back to Top](#table-of-contents)**

75. ### What telemetry signals are supported by OpenTelemetry?

    - **Traces** — spans with parent–child relationships.
    - **Metrics** — counters, gauges, and histograms.
    - **Logs** — structured log records.
    - **Baggage** — propagated key–value pairs that travel with the trace context (not a stored signal per se, but a propagation mechanism).

    OpenTelemetry's goal is to cover all three pillars of observability (metrics, logs, traces) under one consistent API and wire protocol.

    **[⬆ Back to Top](#table-of-contents)**

76. ### What is auto-instrumentation?

    **Auto-instrumentation** instruments frameworks and libraries **without code changes** by attaching an agent or instrumentation libraries at startup. For Java, `opentelemetry-javaagent.jar` automatically instruments Spring Boot, JDBC, gRPC, HTTP clients, and dozens more. It's the fastest way to get broad coverage; you only fall back to manual instrumentation for custom business operations the agent can't see.

    ```bash
    java -javaagent:opentelemetry-javaagent.jar \
         -Dotel.service.name=order-service \
         -Dotel.exporter.otlp.endpoint=https://otlp.nr-data.net:4317 \
         -jar myapp.jar
    ```

    **[⬆ Back to Top](#table-of-contents)**

77. ### What is manual instrumentation?

    **Manual instrumentation** means inserting explicit OpenTelemetry API calls in your code to create spans, record metrics, or inject context. It gives you precise control to instrument **custom operations or business logic** that auto-instrumentation can't detect.

    ```java
    import io.opentelemetry.api.GlobalOpenTelemetry;
    import io.opentelemetry.api.trace.Span;
    import io.opentelemetry.api.trace.Tracer;

    Tracer tracer = GlobalOpenTelemetry.getTracer("order-service");

    public void settlePayment(Order order) {
        Span span = tracer.spanBuilder("settlePayment").startSpan();
        try (var scope = span.makeCurrent()) {
            span.setAttribute("order.id", order.getId());
            span.setAttribute("amount", order.getAmount());
            // business logic
        } catch (Exception e) {
            span.recordException(e);
            throw e;
        } finally {
            span.end();
        }
    }
    ```

    **[⬆ Back to Top](#table-of-contents)**

78. ### How do you export OpenTelemetry data to New Relic?

    Configure the **OTLP exporter** with New Relic's endpoint and your license key. In a Collector config:

    ```yaml
    exporters:
      otlp:
        endpoint: otlp.nr-data.net:4317
        headers:
          api-key: <NEW_RELIC_LICENSE_KEY>
    service:
      pipelines:
        traces:  { receivers: [otlp], exporters: [otlp] }
        metrics: { receivers: [otlp], exporters: [otlp] }
        logs:    { receivers: [otlp], exporters: [otlp] }
    ```

    For direct SDK export (no Collector), set `OTEL_EXPORTER_OTLP_ENDPOINT` and `OTEL_EXPORTER_OTLP_HEADERS` environment variables accordingly. Use the EU endpoint (`otlp.eu01.nr-data.net`) for EU accounts.

    **[⬆ Back to Top](#table-of-contents)**

79. ### What are resource attributes in OpenTelemetry?

    **Resource attributes** describe the **entity producing the telemetry** — `service.name`, `service.version`, `deployment.environment`, `host.name`, `cloud.region`. They provide the context for grouping and identifying data. New Relic uses resource attributes (especially `service.name`) to **populate entity names and tags**, so setting them correctly is what makes your OTel data show up as a properly-named service.

    **[⬆ Back to Top](#table-of-contents)**

80. ### What is baggage propagation?

    **Baggage** is an OpenTelemetry mechanism for propagating arbitrary **key–value pairs across process boundaries** alongside the trace context. It lets you attach metadata (e.g., `user.id`, `tenant`) at the start of a request and have it available on every downstream span without re-passing it explicitly. New Relic supports **W3C Baggage** propagation. Use it sparingly — baggage travels on every hop, so large baggage adds overhead.

    **[⬆ Back to Top](#table-of-contents)**

81. ### What are semantic conventions in OpenTelemetry?

    **Semantic conventions** are standardized attribute names for common operations — HTTP (`http.request.method`, `http.response.status_code`), databases (`db.system`, `db.statement`), messaging (`messaging.system`, `messaging.destination`). By agreeing on consistent names, telemetry from different libraries and languages is **queryable and interpretable in a uniform way**, so a dashboard built on `http.response.status_code` works regardless of which library produced the span.

    **[⬆ Back to Top](#table-of-contents)**

82. ### How do you instrument a Spring Boot application using OpenTelemetry?

    Attach the OTel Java agent at runtime and point it at New Relic:

    ```bash
    java -javaagent:opentelemetry-javaagent.jar \
         -Dotel.service.name=order-service \
         -Dotel.exporter.otlp.endpoint=https://otlp.nr-data.net:4317 \
         -Dotel.exporter.otlp.headers=api-key=YOUR_LICENSE_KEY \
         -jar myapp.jar
    ```

    The agent auto-instruments Spring MVC, JDBC, RestTemplate/WebClient, and more. Add the `opentelemetry-api` dependency only if you also want to create **manual** spans for custom business logic:

    ```groovy
    dependencies {
        implementation 'io.opentelemetry:opentelemetry-api:1.+'
    }
    ```

    **[⬆ Back to Top](#table-of-contents)**

83. ### What are the advantages of OpenTelemetry over vendor-specific agents?

    | OpenTelemetry | Vendor agent |
    | --- | --- |
    | Portable across backends (no lock-in) | Tied to one vendor |
    | Single API for traces, metrics, logs | Vendor-specific APIs |
    | Large open-source community | Vendor roadmap |
    | Consistent semantic conventions | Vendor-specific naming |

    The trade-off: **vendor agents often offer richer automatic instrumentation, deeper framework coverage, and turnkey features** out of the box, whereas OTel may require more configuration. Many teams run a hybrid — vendor agent where depth matters, OTel where portability matters.

    **[⬆ Back to Top](#table-of-contents)**

84. ### How do traces and metrics correlate in OpenTelemetry?

    Metrics can carry **exemplars** — sample data points that reference a **trace ID**, letting you jump from a spike on a latency histogram straight to an example trace that contributed to it. You can also derive metrics from span attributes. New Relic uses these correlations to **link metric dashboards to the underlying traces**, so an alert on p99 latency leads directly to representative slow traces.

    **[⬆ Back to Top](#table-of-contents)**

85. ### What challenges arise during OpenTelemetry adoption?

    - **Instrumenting legacy code** that auto-instrumentation doesn't cover.
    - **Controlling data volume** (and therefore cost) from verbose tracing.
    - **Mapping vendor concepts** to OTel equivalents during migration.
    - **Managing instrumentation overhead** and sampling strategy.
    - **Process and team alignment** — agreeing on naming, sampling, and ownership.
    - **Parallel running** — migrating from a vendor agent often means dual instrumentation and careful validation before cutover.

    **[⬆ Back to Top](#table-of-contents)**


## Infrastructure Monitoring

86. ### What is Infrastructure Monitoring in New Relic?

    **Infrastructure Monitoring** is a set of agents and integrations that collect **host and container metrics** — CPU, memory, disk, network, and process information — and feed them into the New Relic platform. The value is **correlation**: because infrastructure metrics live in the same store as APM data, you can overlay a host's CPU saturation against an application's response-time spike and see them line up.

    **[⬆ Back to Top](#table-of-contents)**

87. ### How do Infrastructure Agents work?

    The **Infrastructure agent** is a lightweight daemon that runs on Linux or Windows. It samples system metrics and host metadata at regular intervals and integrates with services like **Docker, Kubernetes, and cloud providers** through "on-host integrations." It transmits data using the New Relic **Telemetry SDK** over HTTPS. Being lightweight, it's designed to run on every host with minimal footprint.

    **[⬆ Back to Top](#table-of-contents)**

88. ### What metrics are collected from Linux servers?

    | Category | Metrics |
    | --- | --- |
    | **CPU** | User, system, idle, iowait percentages |
    | **Memory** | Used, free, cached, buffers |
    | **Disk I/O** | Reads/writes per second, utilization, latency |
    | **Network** | Bytes/packets in and out, errors |
    | **Load** | 1/5/15-minute load averages |
    | **Processes** | Per-process CPU, memory, count |
    | **Metadata** | OS version, kernel, hostname |

    These are stored in the `SystemSample`, `NetworkSample`, `StorageSample`, and `ProcessSample` event types.

    **[⬆ Back to Top](#table-of-contents)**

89. ### What metrics are collected from Windows servers?

    For Windows hosts the agent collects **CPU usage, memory metrics, disk and network I/O, system uptime, and Windows service status**. It can additionally integrate with **Windows Performance Counters** to pull a wide range of OS- and application-specific counters (e.g., .NET CLR metrics, IIS request queues), extending visibility beyond the default set.

    **[⬆ Back to Top](#table-of-contents)**

90. ### How do you monitor Kubernetes clusters?

    Install the **New Relic Kubernetes integration** (via the `nri-bundle` Helm chart). It deploys the Infrastructure agent as a **DaemonSet** (one pod per node), **Kube-State-Metrics**, and a metrics adapter. Together they capture pod and node CPU/memory, container restarts, and cluster events, and the **Cluster Explorer** provides a visual topology. (Covered in depth in the Kubernetes Monitoring section.)

    **[⬆ Back to Top](#table-of-contents)**

91. ### How do you monitor Docker containers?

    The Infrastructure agent **auto-detects Docker containers** running on a host and reports per-container **CPU, memory, network, and disk** metrics. Enabling the Docker integration additionally collects **container labels and image information**, so you can facet metrics by image version or label. Container data is correlated with the host it runs on and, if the app is instrumented, with APM data.

    ```sql
    SELECT average(cpuPercent), average(memoryResidentSizeBytes)
    FROM ContainerSample FACET containerName SINCE 30 minutes AGO
    ```

    **[⬆ Back to Top](#table-of-contents)**

92. ### What is host inventory data?

    **Host inventory** is the **static metadata** about a host — OS version, kernel, CPU count, memory size, installed packages, and configuration files. Unlike time-series metrics, inventory describes the host's *configuration state*. New Relic uses it for reporting and **change tracking**: if a package version or config file changes, that change is recorded and can be correlated with a performance regression.

    **[⬆ Back to Top](#table-of-contents)**

93. ### How does New Relic monitor CPU utilization?

    The agent reports CPU usage at the **host level** and **per process**, and in Kubernetes **per pod and container**. Charts break CPU into user, system, and idle percentages over time, and **iowait** is shown separately (high iowait signals disk bottlenecks rather than compute load). Alerts can be set on sustained high CPU.

    ```sql
    SELECT average(cpuPercent) FROM SystemSample
    FACET hostname SINCE 1 hour AGO TIMESERIES
    ```

    **[⬆ Back to Top](#table-of-contents)**

94. ### How does New Relic monitor memory consumption?

    Memory metrics track **used and free memory, swap usage, and page faults**. High memory usage often correlates with **increased GC activity** (in JVM apps) or **container OOM kills** (in Kubernetes). Watching memory alongside GC time and OOM events helps distinguish a genuine leak from normal high-but-stable usage.

    **[⬆ Back to Top](#table-of-contents)**

95. ### How do you identify resource bottlenecks?

    Build dashboards that **correlate CPU, memory, disk, and network** against application performance. Bottlenecks typically manifest as: **high CPU iowait** (disk-bound), **saturated network interfaces** (network-bound), **high disk I/O latency** (storage-bound), or **memory pressure** (swapping/OOM). New Relic's **anomaly detection** can flag these deviations automatically rather than relying on you to spot them.

    **[⬆ Back to Top](#table-of-contents)**

96. ### How do you monitor disk I/O performance?

    The agent reports **disk read/write bytes per second, IOPS, queue length, and latency**. Set alerts on high latency or high utilization (a disk consistently near 100% utilization is a bottleneck). For cloud-backed volumes (EBS, Azure Disks), use the corresponding **cloud integration** metrics to get provider-side insight like burst-balance depletion.

    ```sql
    SELECT average(diskUtilizationPercent), average(readBytesPerSecond + writeBytesPerSecond)
    FROM StorageSample FACET hostname, device SINCE 1 hour AGO
    ```

    **[⬆ Back to Top](#table-of-contents)**

97. ### What is process monitoring?

    **Process monitoring** captures metrics **per process or service** — CPU, memory, and restart count. New Relic's Infrastructure agent lists the **top processes by CPU or memory** on each host, which is the fastest way to find a runaway process consuming resources (e.g., a stuck worker pegging a core).

    ```sql
    SELECT average(cpuPercent) FROM ProcessSample
    FACET commandName SINCE 30 minutes AGO LIMIT 10
    ```

    **[⬆ Back to Top](#table-of-contents)**

98. ### How do you monitor cloud infrastructure?

    Integrate New Relic with **AWS, Azure, or GCP** via their cloud integrations. These use the **provider's APIs** (CloudWatch, Azure Monitor, GCP Operations) to collect metrics for managed services — EC2, RDS, S3, Lambda, Azure VMs, GKE, and more. The data appears in the cloud-integrations UI and can be correlated with APM data via shared tags. (Detailed in the Cloud Monitoring section.)

    **[⬆ Back to Top](#table-of-contents)**

99. ### What are Infrastructure Events?

    **Infrastructure events** are discrete occurrences — configuration changes, host reboots, deployment markers, container restarts. They provide the **context for changes** that explain a metric shift ("response time jumped right after this deployment event"). Events can trigger alerts or be overlaid on dashboards as markers so correlation between change and impact is visible.

    **[⬆ Back to Top](#table-of-contents)**

100. ### How do you create infrastructure dashboards?

     Use the **Dashboard Builder** in New Relic One. Add widgets backed by NRQL queries over infrastructure event types (`SystemSample`, `MemorySample`, `StorageSample`), pick a visualization (line, area, bar), and group with `FACET` by host, region, or tag to scope to the subset you care about.

     ```sql
     -- CPU and memory side by side, faceted by host
     SELECT average(cpuPercent) FROM SystemSample
     FACET hostname SINCE 3 hours AGO TIMESERIES

     SELECT average(memoryUsedBytes / memoryTotalBytes * 100) AS 'Mem %'
     FROM SystemSample FACET hostname SINCE 3 hours AGO TIMESERIES
     ```

     **[⬆ Back to Top](#table-of-contents)**


## Kubernetes Monitoring

101. ### How does New Relic monitor Kubernetes clusters?

     The **Kubernetes integration** installs the New Relic Infrastructure agent as a **DaemonSet** (one agent per node) plus **Kube-State-Metrics**. It collects metrics for **nodes, pods, deployments, ReplicaSets, DaemonSets, and services**, and the **Cluster Explorer** renders a topology view of the whole cluster with health overlays. It also captures Kubernetes **events** for context.

     **[⬆ Back to Top](#table-of-contents)**

102. ### What Kubernetes metrics are available?

     | Level | Metrics |
     | --- | --- |
     | **Pod** | CPU/memory usage, restart count, status, phase |
     | **Node** | CPU/memory usage, disk, conditions (Ready, MemoryPressure) |
     | **Container** | CPU/memory used vs. requests/limits, restart count |
     | **Deployment** | Desired vs. available replicas |
     | **Cluster** | Events, namespace usage |

     These map to event types like `K8sPodSample`, `K8sNodeSample`, `K8sContainerSample`, and `K8sDeploymentSample`.

     **[⬆ Back to Top](#table-of-contents)**

103. ### How do you install New Relic on AKS?

     Add the Helm repo and install the `nri-bundle` chart, supplying your license key and cluster name:

     ```bash
     helm repo add newrelic https://helm-charts.newrelic.com
     helm repo update

     helm upgrade --install newrelic-bundle newrelic/nri-bundle \
       --set global.licenseKey=YOUR_LICENSE_KEY \
       --set global.cluster=my-aks-cluster \
       --namespace newrelic --create-namespace
     ```

     The bundle includes the Infrastructure agent (DaemonSet), Kube-State-Metrics, and the metrics adapter.

     **[⬆ Back to Top](#table-of-contents)**

104. ### How do you install New Relic on EKS?

     The process mirrors AKS — use the same `nri-bundle` Helm chart with your EKS cluster name and license key. The key extra consideration is **IAM**: ensure the agent's service account has the permissions (via IAM Roles for Service Accounts, IRSA) needed to query the Kubernetes API server and any AWS metadata.

     ```bash
     helm upgrade --install newrelic-bundle newrelic/nri-bundle \
       --set global.licenseKey=YOUR_LICENSE_KEY \
       --set global.cluster=my-eks-cluster \
       --namespace newrelic --create-namespace
     ```

     **[⬆ Back to Top](#table-of-contents)**

105. ### How do you install New Relic on GKE?

     Again use the `nri-bundle` Helm chart with the GKE cluster name and license key. Optionally configure the **metrics adapter** to send Kubernetes metrics into New Relic's dimensional metric store. On GKE Autopilot, confirm the chart values are compatible with Autopilot's resource constraints.

     ```bash
     helm upgrade --install newrelic-bundle newrelic/nri-bundle \
       --set global.licenseKey=YOUR_LICENSE_KEY \
       --set global.cluster=my-gke-cluster \
       --namespace newrelic --create-namespace
     ```

     **[⬆ Back to Top](#table-of-contents)**

106. ### What is kube-state-metrics?

     **Kube-State-Metrics (KSM)** is an open-source service that listens to the Kubernetes API and **exposes the state of Kubernetes objects as metrics** — deployment replica counts, ReplicaSet status, DaemonSet readiness, node conditions, pod phases. New Relic scrapes KSM to obtain this object-state data, which complements the resource-usage metrics gathered by the agent.

     **[⬆ Back to Top](#table-of-contents)**

107. ### How do you identify unhealthy pods?

     Use the Cluster Explorer's health view, or query directly:

     ```sql
     -- Pods not running or restarting frequently
     SELECT latest(status), latest(restartCount)
     FROM K8sPodSample
     WHERE status != 'Running' OR restartCount > 0
     FACET podName, namespace SINCE 15 minutes AGO
     ```

     Set alerts on high `restartCount` or non-`Running` status so you're notified before users are affected.

     **[⬆ Back to Top](#table-of-contents)**

108. ### How do you troubleshoot pod restarts?

     1. **Inspect `K8sEvent`** records for the pod — they reveal OOMKills, failed liveness probes, or image-pull errors.
     2. **Check container resource usage** against limits — an OOMKill means memory exceeded the limit.
     3. **Use logs-in-context** — New Relic links container logs to the pod, so you can read the crash output right before the restart.
     4. **Look for crash loops** — a rapidly climbing `restartCount` indicates `CrashLoopBackOff`.

     ```sql
     SELECT count(*) FROM K8sEvent
     WHERE category = 'kube' AND reason IN ('OOMKilling','BackOff','Failed')
     FACET podName SINCE 1 hour AGO
     ```

     **[⬆ Back to Top](#table-of-contents)**

109. ### What Kubernetes dashboards are available?

     New Relic ships **built-in dashboards** for cluster overview, nodes, namespaces, deployments, and pods as part of the Kubernetes quickstart. You can clone and customize them, or build your own with NRQL to show exactly the metrics that matter for your workloads (e.g., per-team namespace dashboards).

     **[⬆ Back to Top](#table-of-contents)**

110. ### How do you monitor node utilization?

     Query the `K8sNodeSample` event for core utilization metrics and watch node conditions:

     ```sql
     SELECT average(cpuUsedCores), average(memoryUsedBytes), average(fsUsedBytes)
     FROM K8sNodeSample FACET nodeName SINCE 1 hour AGO TIMESERIES
     ```

     Set alerts on high utilization or on adverse node conditions like **`NodeDiskPressure`** or **`NodeMemoryPressure`**, which precede pod evictions.

     **[⬆ Back to Top](#table-of-contents)**

111. ### How do you monitor namespaces?

     Query `K8sPodSample` (or container samples) and **facet by `namespace`** to attribute resource usage to teams or applications:

     ```sql
     SELECT average(cpuUsedCores), average(memoryUsedBytes)
     FROM K8sPodSample FACET namespace SINCE 1 hour AGO TIMESERIES
     ```

     This is the basis for **chargeback/showback** dashboards that report each team's footprint.

     **[⬆ Back to Top](#table-of-contents)**

112. ### How do you analyze container resource consumption?

     Use `K8sContainerSample` metrics and compare **actual usage against requests/limits** to spot over- or under-provisioning:

     ```sql
     SELECT average(cpuUsedCores), average(cpuLimitCores),
            average(memoryUsedBytes), average(memoryLimitBytes), latest(restartCount)
     FROM K8sContainerSample FACET containerName SINCE 1 hour AGO
     ```

     A container consistently using far below its requests is wasting cluster capacity; one bumping against its limits will get throttled (CPU) or OOMKilled (memory).

     **[⬆ Back to Top](#table-of-contents)**

113. ### What is Cluster Explorer?

     **Cluster Explorer** is New Relic's visual tool for Kubernetes. It displays the cluster hierarchy — **clusters → nodes → namespaces → deployments → pods** — and overlays performance metrics and health indicators on each level. You can **drill down from a node into its pods and then into pod logs and traces**, making it a single pane for navigating from a cluster-wide symptom down to a specific container's logs.

     **[⬆ Back to Top](#table-of-contents)**

114. ### How do you monitor deployments and ReplicaSets?

     `K8sDeploymentSample` and `K8sReplicaSetSample` expose **`availableReplicas`, `desiredReplicas`, and deployment status**. The key health check is **available < desired**, which means the deployment isn't fully rolled out (pods failing to start, insufficient resources):

     ```sql
     SELECT latest(podsAvailable), latest(podsDesired)
     FROM K8sDeploymentSample
     WHERE podsAvailable < podsDesired
     FACET deploymentName, namespace SINCE 10 minutes AGO
     ```

     Alert when available replicas drop below desired for a sustained window.

     **[⬆ Back to Top](#table-of-contents)**

115. ### How do you correlate Kubernetes issues with application traces?

     Link **Kubernetes attributes** (pod name, container ID, namespace) onto trace and log data — the agent does this automatically when both K8s and APM are instrumented. Then use **distributed tracing** to see how a pod restart or a node's high CPU impacted application latency, and **logs-in-context** to pivot from a slow trace to the exact container logs for that request. This is the payoff of a unified platform: infra symptom → app impact → log evidence in a few clicks.

     **[⬆ Back to Top](#table-of-contents)**


## Logs Management

116. ### What is New Relic Logs?

     **New Relic Logs** is a log-management solution that **ingests, parses, and indexes** logs and stores them in the same platform as metrics and traces. Its differentiator is **correlation** — logs are automatically tied to APM transactions and infrastructure entities, enabling logs-in-context so you read the relevant log lines right inside a trace.

     **[⬆ Back to Top](#table-of-contents)**

117. ### How are logs ingested into New Relic?

     Logs can be forwarded several ways:

     - **Infrastructure agent** — its logging feature tails files (e.g., `/var/log/syslog`) and forwards them with host metadata.
     - **Fluent Bit / Fluentd / Logstash** — popular log shippers with New Relic output plugins.
     - **Log API** — direct HTTP POST to `https://log-api.newrelic.com/log/v1`.
     - **APM agent log forwarding** — the language agent forwards application logs and auto-injects trace context.

     **[⬆ Back to Top](#table-of-contents)**

118. ### What log forwarding options are available?

     - The **Infrastructure agent** `logs` configuration block.
     - The dedicated **`newrelic-logging` Helm chart** (Fluent Bit) for Kubernetes.
     - The **Log API** endpoint (`https://log-api.newrelic.com/log/v1`).
     - **Cloud-native integrations** — AWS CloudWatch Logs (via Lambda/Firehose), Azure Monitor, and GCP logging.

     **[⬆ Back to Top](#table-of-contents)**

119. ### What is log parsing?

     **Log parsing** extracts structured fields from raw log lines — pulling out `timestamp`, `level`, `message`, `requestId`, etc. — so they become queryable attributes rather than opaque text. New Relic provides **built-in parsers** for common formats (JSON, Nginx, Apache, Syslog) and supports **custom Grok patterns** for proprietary formats. Parsing happens at ingest based on rules you can scope by attribute.

     **[⬆ Back to Top](#table-of-contents)**

120. ### What are structured logs?

     **Structured logs** are encoded as JSON or key–value pairs, giving each field an explicit name and value. They're trivial to parse and query because the structure is already present:

     ```json
     {"timestamp":"2026-06-13T10:15:00Z","level":"INFO","service":"order-service","orderId":123,"trace.id":"abc123","message":"Order processed"}
     ```

     Emitting structured logs (e.g., with Logback's JSON encoder in a Spring Boot app) is the single biggest improvement you can make to log usability.

     **[⬆ Back to Top](#table-of-contents)**

121. ### What are unstructured logs?

     **Unstructured logs** are plain-text lines with no defined schema:

     ```
     2026-06-13 10:15:00 INFO  Order processed: 123
     ```

     To make these queryable by field, you must apply a **parser** (Grok or regex) at ingest to extract the timestamp, level, and message. Unstructured logs are harder to work with at scale, which is why structured logging is recommended for new applications.

     **[⬆ Back to Top](#table-of-contents)**

122. ### How do you correlate logs with traces?

     Include the **`trace.id`** and **`span.id`** in every log line. In Java with SLF4J/Logback, use the **MDC (Mapped Diagnostic Context)** to inject them into the log pattern — the New Relic agent populates these MDC keys automatically when log forwarding is enabled:

     ```java
     // The New Relic agent auto-populates MDC with trace.id and span.id.
     // Reference them in logback.xml:
     ```

     ```xml
     <pattern>%d{ISO8601} %-5level [trace.id=%X{trace.id} span.id=%X{span.id}] %logger - %msg%n</pattern>
     ```

     New Relic then automatically correlates any log containing a valid `trace.id` with its span, powering logs-in-context.

     **[⬆ Back to Top](#table-of-contents)**

123. ### What is logs-in-context?

     **Logs-in-context** is the ability to view log lines **directly within the context of a trace or transaction**. Instead of switching to a separate log tool and manually searching by timestamp, you open a span in New Relic and see the exact log output emitted during that request. It dramatically shortens debugging because the logs and the trace that produced them sit side by side.

     **[⬆ Back to Top](#table-of-contents)**

124. ### How do you search logs efficiently?

     Use the **Logs UI** for full-text search and filtering, or NRQL for precise queries:

     ```sql
     SELECT message, level, hostname FROM Log
     WHERE level = 'ERROR' AND service = 'order-service'
     SINCE 1 hour AGO LIMIT 100
     ```

     Use **facets** to group logs by service, host, or error type, narrow the **time range**, and filter on parsed attributes rather than relying solely on full-text matching, which is slower at scale.

     **[⬆ Back to Top](#table-of-contents)**

125. ### What are log patterns?

     **Log patterns** are templates used to extract fields from unstructured logs, typically via **Grok patterns** or regular expressions. For example, an Nginx access-log pattern extracts the request method, path, status code, and response time into named attributes. New Relic's **Patterns** feature also automatically clusters similar log messages so you can see the dominant log "shapes" without reading every line.

     **[⬆ Back to Top](#table-of-contents)**

126. ### How do you detect anomalies in logs?

     Use **New Relic AI** and NRQL anomaly conditions to detect unexpected spikes in error-log volume or unusual patterns. A common approach is to convert log volume into a metric and alert when it deviates from the learned baseline:

     ```sql
     -- Baseline/anomaly condition source query
     SELECT count(*) FROM Log WHERE level = 'ERROR' FACET service
     ```

     Sudden error-rate increases relative to the seasonal baseline trigger the alert without you hand-tuning a static threshold.

     **[⬆ Back to Top](#table-of-contents)**

127. ### How do you create log alerts?

     Create an **alert condition on the `Log` event type** with an NRQL query and threshold:

     ```sql
     SELECT count(*) FROM Log
     WHERE level = 'ERROR' AND service = 'order-service'
     SINCE 5 minutes AGO
     ```

     Set the condition to trigger when the result exceeds, say, 10 over 5 minutes. For dynamic behavior, use an **NRQL anomaly condition** instead of a static threshold so the alert adapts to normal daily variation.

     **[⬆ Back to Top](#table-of-contents)**

128. ### What are common log ingestion challenges?

     - **High attribute cardinality** — too many distinct values bloat storage and slow queries.
     - **Data volume / cost** — verbose logging is expensive at ingest-based pricing.
     - **Parsing failures** — malformed lines that don't match the parser.
     - **Timestamp inconsistencies** — wrong time zones or formats causing misordered logs.
     - **Incomplete metadata** — logs lacking service/trace context, breaking correlation.

     Mitigate by emitting **structured logs**, dropping unnecessary fields, and standardizing timestamps to UTC/ISO-8601.

     **[⬆ Back to Top](#table-of-contents)**

129. ### How do you reduce log costs?

     - **Convert high-volume logs to metrics** — if you only need counts/rates, aggregate at ingest.
     - **Exclude noisy sources** — health-check and debug logs rarely need long-term storage.
     - **Sample or drop** — use New Relic **drop filters** to discard low-value log types before they're billed.
     - **Trim fields** — remove redundant or oversized attributes.
     - **Tune retention** — reserve longer (Data Plus) retention only for logs that need it.

     ```sql
     -- A drop rule's matching query: drop DEBUG logs from a chatty service
     SELECT * FROM Log WHERE level = 'DEBUG' AND service = 'verbose-service'
     ```

     **[⬆ Back to Top](#table-of-contents)**

130. ### What log retention options are available?

     The **free tier** retains logs for roughly **8 days**. Paid plans extend retention (commonly **30–90 days**), and **Data Plus** offers longer retention (up to 90+ days) and additional compliance features at higher cost. Retention is a key cost lever — keep verbose logs short and only extend retention for the data you must keep for audit or compliance.

     > *Retention windows and tiers change over time — confirm current numbers in New Relic's documentation.*

     **[⬆ Back to Top](#table-of-contents)**


## NRQL (New Relic Query Language)

131. ### What is NRQL?

     **NRQL (New Relic Query Language)** is a SQL-like language for querying everything stored in New Relic — metrics, events, logs, and traces. It supports filtering (`WHERE`), aggregation (`average`, `count`, `percentile`), grouping (`FACET`), and time bucketing (`TIMESERIES`). NRQL powers dashboards, alert conditions, and ad-hoc investigation.

     ```sql
     SELECT count(*) FROM Transaction WHERE appName = 'order-service' SINCE 1 hour AGO
     ```

     **[⬆ Back to Top](#table-of-contents)**

132. ### How is NRQL different from SQL?

     | | SQL | NRQL |
     | --- | --- | --- |
     | **Data model** | Relational tables | Event/time-series records |
     | **`FROM`** | A table | An event type or metric name |
     | **Joins** | Supported | **Not supported** |
     | **Time** | Manual date filters | Built-in `SINCE`/`UNTIL`/`TIMESERIES` |
     | **Aggregation** | `GROUP BY` | `FACET` |

     The biggest practical difference is the **lack of joins** — you work within a single event type per query and use nested functions or multiple `SELECT` clauses instead.

     **[⬆ Back to Top](#table-of-contents)**

133. ### What are Events in NRQL?

     **Events** are discrete, timestamped records — `Transaction`, `Span`, `Log`, `K8sPodSample`, `PageView`. Each event has **attributes** (fields) you can filter and aggregate on. NRQL queries events to compute aggregations or retrieve raw records. Events are stored at full fidelity (subject to sampling for some types).

     ```sql
     SELECT * FROM Transaction WHERE duration > 2 SINCE 30 minutes AGO LIMIT 50
     ```

     **[⬆ Back to Top](#table-of-contents)**

134. ### What are Metrics in NRQL?

     **Metrics** are pre-aggregated time-series data points, optimized for **high cardinality and long retention** at low query cost. They're queried with `FROM Metric` and identified by `metricName`. Metrics are stored separately from events and are ideal for high-frequency data where you don't need every individual sample.

     ```sql
     SELECT average(newrelic.timeslice.value) FROM Metric
     WHERE metricName = 'apm.service.transaction.duration'
     AND appName = 'order-service' TIMESERIES SINCE 1 hour AGO
     ```

     **[⬆ Back to Top](#table-of-contents)**

135. ### What are Facets in NRQL?

     **`FACET`** groups results by one or more attributes, like SQL's `GROUP BY`. It returns a separate aggregate per group:

     ```sql
     SELECT average(duration) FROM Transaction
     FACET appName SINCE 1 hour AGO
     ```

     You can facet by multiple attributes (`FACET appName, host`) and control the number of groups with `LIMIT`. Facet on **low-cardinality** fields to keep results meaningful and performant.

     **[⬆ Back to Top](#table-of-contents)**

136. ### What is TIMESERIES?

     **`TIMESERIES`** splits an aggregate into time buckets, returning a series (a line chart) instead of a single number:

     ```sql
     SELECT average(duration) FROM Transaction
     WHERE appName = 'order-service' TIMESERIES 1 minute SINCE 1 hour AGO
     ```

     You can specify the bucket width (`TIMESERIES 5 minutes`) or let New Relic choose (`TIMESERIES AUTO`).

     **[⬆ Back to Top](#table-of-contents)**

137. ### What are SINCE and UNTIL?

     **`SINCE`** sets the start of the query window and **`UNTIL`** sets the end. They accept relative or absolute times:

     ```sql
     SELECT count(*) FROM Transaction
     SINCE 1 hour AGO UNTIL 10 minutes AGO

     -- Compare to the same window last week
     SELECT count(*) FROM Transaction SINCE 1 week AGO UNTIL 6 days AGO
     ```

     Combine with `COMPARE WITH` to overlay a prior period.

     **[⬆ Back to Top](#table-of-contents)**

138. ### How do you aggregate data in NRQL?

     NRQL provides aggregation functions: `average()`, `count()`, `sum()`, `max()`, `min()`, `latest()`, `percentile()`, `histogram()`, `rate()`, `uniqueCount()`, and `percentage()`. Combine them with `WHERE` filters and `FACET` grouping:

     ```sql
     SELECT count(*), average(duration), percentile(duration, 95), max(duration)
     FROM Transaction WHERE appName = 'order-service'
     FACET name SINCE 1 hour AGO
     ```

     **[⬆ Back to Top](#table-of-contents)**

139. ### How do you calculate average response time using NRQL?

     ```sql
     SELECT average(duration) FROM Transaction
     WHERE appName = 'order-service' SINCE 5 minutes AGO
     ```

     Facet by endpoint for a breakdown:

     ```sql
     SELECT average(duration) FROM Transaction
     WHERE appName = 'order-service'
     FACET name SINCE 5 minutes AGO ORDER BY average(duration) DESC
     ```

     **[⬆ Back to Top](#table-of-contents)**

140. ### How do you calculate error percentage using NRQL?

     Divide the error count by the total count. The cleanest way is `percentage()`:

     ```sql
     SELECT percentage(count(*), WHERE error IS true) AS 'Error %'
     FROM Transaction WHERE appName = 'order-service' SINCE 1 hour AGO
     ```

     Equivalent using `filter()`:

     ```sql
     SELECT (filter(count(*), WHERE error IS true) / count(*)) * 100 AS 'Error %'
     FROM Transaction WHERE appName = 'order-service' SINCE 1 hour AGO
     ```

     **[⬆ Back to Top](#table-of-contents)**

141. ### How do you filter data using WHERE clauses?

     `WHERE` filters on attribute values with comparison and logical operators, plus `IN`, `NOT`, `LIKE`, and `IS NULL`:

     ```sql
     SELECT count(*) FROM Transaction
     WHERE appName = 'order-service'
       AND httpResponseCode >= 500
       AND name LIKE '%/checkout%'
       AND host IN ('host-1','host-2')
     SINCE 1 hour AGO
     ```

     **[⬆ Back to Top](#table-of-contents)**

142. ### What is FACET in NRQL?

     `FACET` groups results by one or more attributes and returns an aggregate per group — the basis of most bar charts and tables:

     ```sql
     SELECT count(*) FROM Log
     FACET level, service SINCE 1 hour AGO
     ```

     This shows the log count broken down by level **and** service. Limit cardinality with `LIMIT` and prefer low-cardinality facet fields.

     **[⬆ Back to Top](#table-of-contents)**

143. ### How do you query logs using NRQL?

     Logs are stored as `Log` events:

     ```sql
     SELECT message, level, hostname FROM Log
     WHERE message LIKE '%timeout%'
     SINCE 30 minutes AGO LIMIT 100
     ```

     Use `LIMIT` to cap returned lines, `FACET` to group by attributes, and parsed fields (`level`, `service`, `trace.id`) for precise filtering.

     **[⬆ Back to Top](#table-of-contents)**

144. ### What are nested aggregations?

     **Nested aggregations** apply an inner filter or function before an outer aggregate — for example, computing a percentile only over successful requests:

     ```sql
     SELECT percentile(filter(duration, WHERE httpResponseCode = 200), 95)
     FROM Transaction WHERE appName = 'order-service' SINCE 1 hour AGO
     ```

     The inner `filter()` narrows the data set, then `percentile()` aggregates the result.

     **[⬆ Back to Top](#table-of-contents)**

145. ### What are subqueries in NRQL?

     NRQL does **not** support SQL-style subqueries (a `SELECT` inside a `FROM`). Instead you achieve similar results with **nested functions** (`filter`, `percentile(filter(...))`), **multi-select** queries (`SELECT count(*), average(duration)`), or by orchestrating multiple queries via the **NerdGraph GraphQL API** for more complex manipulation.

     **[⬆ Back to Top](#table-of-contents)**

146. ### What is rate() in NRQL?

     **`rate()`** computes the rate of a value over a specified time unit — useful for turning counts into per-second/per-minute rates:

     ```sql
     SELECT rate(count(*), 1 minute) AS 'Requests per minute'
     FROM Transaction WHERE appName = 'order-service' TIMESERIES SINCE 1 hour AGO
     ```

     **[⬆ Back to Top](#table-of-contents)**

147. ### What is percentile() in NRQL?

     **`percentile(attribute, n)`** returns the nth-percentile value — essential for understanding tail latency that averages hide:

     ```sql
     SELECT percentile(duration, 50, 95, 99)
     FROM Transaction WHERE appName = 'order-service' SINCE 1 hour AGO
     ```

     This returns p50, p95, and p99 response times in a single query.

     **[⬆ Back to Top](#table-of-contents)**

148. ### What is uniqueCount()?

     **`uniqueCount(attribute)`** counts the number of distinct values of an attribute:

     ```sql
     SELECT uniqueCount(userId) AS 'Unique Users'
     FROM Transaction WHERE appName = 'order-service' SINCE 1 day AGO
     ```

     Use with care — computing unique counts over very **high-cardinality** attributes can be expensive and slow.

     **[⬆ Back to Top](#table-of-contents)**

149. ### How do you optimize NRQL queries?

     - **Restrict the time range** with `SINCE` — smaller windows scan less data.
     - **Filter early** on indexed/common attributes in `WHERE`.
     - **Facet on low-cardinality fields** and cap with `LIMIT`.
     - **Avoid `uniqueCount()` on high-cardinality attributes** unless necessary.
     - **Prefer `Metric` over events** for high-frequency, long-range queries.
     - **Avoid large `LIMIT` values** when you only need aggregates.

     **[⬆ Back to Top](#table-of-contents)**

150. ### How do you build custom dashboards using NRQL?

     In New Relic One, create a dashboard and add **widgets**, each backed by an NRQL query and a chosen visualization. Use `FACET` and `TIMESERIES` to shape the data, then save and share:

     ```sql
     -- Widget 1: throughput over time
     SELECT rate(count(*), 1 minute) FROM Transaction
     WHERE appName = 'order-service' TIMESERIES SINCE 3 hours AGO

     -- Widget 2: error rate
     SELECT percentage(count(*), WHERE error IS true)
     FROM Transaction WHERE appName = 'order-service' TIMESERIES SINCE 3 hours AGO
     ```

     **[⬆ Back to Top](#table-of-contents)**


## Dashboards & Visualization

151. ### What types of visualizations are available in New Relic?

     New Relic supports **line, bar, area, and pie charts, tables, heatmaps, histograms, single-value (billboard) numbers, and gauges**, plus **markdown** widgets for documentation and **custom visualizations** built with the New Relic One SDK (NR1). The visualization is chosen per widget to best fit the query's output (e.g., billboard for a single KPI, line for a time series).

     **[⬆ Back to Top](#table-of-contents)**

152. ### How do you create custom dashboards?

     In New Relic One, go to **Dashboards → Create a dashboard**. Add widgets, choose a data source (NRQL or metrics), write the query (or start from a quickstart chart), pick a visualization, then arrange and resize the widgets. Set the dashboard time range, save, and share. Dashboards can also be defined as code via the NerdGraph API for version control.

     **[⬆ Back to Top](#table-of-contents)**

153. ### What is a dashboard widget?

     A **widget** is a single component on a dashboard tied to one NRQL query and one visualization type. Widgets can be **resized, rearranged, and duplicated**, and clicking into one opens the underlying query for editing or deeper exploration. A dashboard is essentially a curated collection of widgets.

     **[⬆ Back to Top](#table-of-contents)**

154. ### How do you share dashboards?

     Dashboards can be shared **within your organization** by URL, made viewable to specific users/teams, or **embedded** in internal portals via a live iframe/public-sharing link. You can also export the dashboard's underlying data via the API. Permission controls determine who can view versus edit.

     **[⬆ Back to Top](#table-of-contents)**

155. ### What are dashboard permissions?

     Dashboard permissions control access at levels like **View Only, Edit, and Owner**, and can be assigned to individual users or teams. You can also scope a dashboard to specific **accounts**. This governance prevents accidental edits to shared executive dashboards while still letting teams build their own.

     **[⬆ Back to Top](#table-of-contents)**

156. ### How do you create executive dashboards?

     Executive dashboards focus on **high-level KPIs** — availability, latency, error rate, and SLA adherence — rather than low-level detail. Use **billboard widgets with large fonts** for headline numbers, combine multiple services into summary charts, and use **wider `TIMESERIES` intervals** (e.g., 1 hour) for a big-picture trend rather than minute-by-minute noise.

     ```sql
     SELECT percentage(count(*), WHERE error IS false) AS 'Availability %'
     FROM Transaction WHERE appName IN ('checkout','payments','inventory')
     SINCE 1 day AGO
     ```

     **[⬆ Back to Top](#table-of-contents)**

157. ### How do you visualize SLA metrics?

     Build a dashboard showing **Apdex, error rate, and uptime per service**, using **threshold colors** (green/yellow/red) so violations are obvious at a glance. Compute SLO attainment with NRQL — for instance, the percentage of requests under a latency threshold:

     ```sql
     SELECT percentage(count(*), WHERE duration < 0.5) AS 'Under 500ms %'
     FROM Transaction WHERE appName = 'checkout' SINCE 7 days AGO
     ```

     **[⬆ Back to Top](#table-of-contents)**

158. ### How do you visualize business KPIs?

     Instrument **custom events** (e.g., `OrderPlaced`, `PaymentFailed`) from your application, then query them with NRQL and build time-series charts for order volume, revenue, conversion rate, and failure counts. Facet by region or user segment for insight:

     ```sql
     SELECT count(*) AS 'Orders', sum(amount) AS 'Revenue'
     FROM OrderPlaced FACET region SINCE 1 day AGO TIMESERIES
     ```

     ```java
     // Emit a custom event from the application via the agent API
     Map<String, Object> attrs = new HashMap<>();
     attrs.put("orderId", order.getId());
     attrs.put("amount", order.getAmount());
     attrs.put("region", order.getRegion());
     NewRelic.getAgent().getInsights().recordCustomEvent("OrderPlaced", attrs);
     ```

     **[⬆ Back to Top](#table-of-contents)**

159. ### How do you create service health dashboards?

     Create widgets for the core health signals **per service** — response time, error rate, throughput, plus CPU/memory of the underlying hosts. Use **threshold lines and color coding** to highlight anomalies, and group services so an on-call engineer sees the whole platform's health on one screen.

     ```sql
     SELECT average(duration), percentage(count(*), WHERE error IS true), rate(count(*), 1 minute)
     FROM Transaction FACET appName SINCE 1 hour AGO TIMESERIES
     ```

     **[⬆ Back to Top](#table-of-contents)**

160. ### What are golden signals dashboards?

     A **golden signals** dashboard tracks the four signals Google's SRE book identifies as the minimal set for any service: **Latency, Traffic, Errors, and Saturation**. It shows response time, request rate, error rate, and resource utilization for critical services, giving an at-a-glance read on system health that generalizes across very different services.

     **[⬆ Back to Top](#table-of-contents)**


## Alerting & Incident Management

161. ### What are alert policies?

     An **alert policy** is a container that groups one or more **conditions** together with **notification settings** and **incident preferences**. Policies define when incidents are created, how violations are grouped into incidents, and who is notified. Organizing conditions into policies (e.g., one per team or workload) keeps alerting manageable.

     **[⬆ Back to Top](#table-of-contents)**

162. ### What are alert conditions?

     An **alert condition** specifies the **signal to monitor** (a metric or NRQL query), the **threshold**, and the **evaluation criteria** (duration, comparison). Examples: error rate > 5% for 5 minutes; CPU > 90%; a NRQL anomaly on log volume. A condition belongs to a policy and produces violations when its criteria are met.

     **[⬆ Back to Top](#table-of-contents)**

163. ### What is baseline alerting?

     **Baseline alerting** uses **historical data to compute a dynamic, self-adjusting threshold**. The condition triggers when the metric deviates significantly (by a configurable number of standard deviations) from its learned normal range. This automatically accounts for daily/weekly seasonality, so you don't manually retune thresholds — ideal for metrics with predictable cyclical patterns like traffic.

     **[⬆ Back to Top](#table-of-contents)**

164. ### What is static threshold alerting?

     **Static threshold alerting** triggers when a metric crosses a **fixed value** (e.g., CPU > 80%, error rate > 5%). It's simple and predictable, best for metrics with clear, stable limits. Its weakness is that a single fixed value may produce false positives during expected peaks or miss problems during quiet periods, requiring careful tuning.

     **[⬆ Back to Top](#table-of-contents)**

165. ### What is anomaly detection?

     **Anomaly detection** uses **machine learning** to identify deviations from normal behavior in metrics or log volumes, automatically adapting to seasonality and trend. New Relic AI provides anomaly conditions that flag the unusual without a hand-set threshold — catching, for example, an error-rate climb that's abnormal for a Tuesday afternoon even if it hasn't yet crossed any static line.

     **[⬆ Back to Top](#table-of-contents)**

166. ### What are NRQL alerts?

     **NRQL alert conditions** trigger based on the result of an arbitrary NRQL query, giving you the full power of the language — complex filtering, aggregation, and math — for alert logic:

     ```sql
     SELECT percentile(duration, 95) FROM Transaction
     WHERE appName = 'checkout' FACET name
     ```

     For example, alert when the p95 response time exceeds 2 seconds for 3 consecutive minutes. NRQL alerts are the most flexible condition type.

     **[⬆ Back to Top](#table-of-contents)**

167. ### How do you configure incident preferences?

     **Incident preferences** govern how violations roll up into incidents. Options range from **one incident per condition** (noisier, more granular) to **one incident per policy** (fewer, broader incidents) to **per target/entity**. Setting this correctly balances signal against noise — too granular pages on every blip; too coarse hides distinct problems behind one incident.

     **[⬆ Back to Top](#table-of-contents)**

168. ### What is alert aggregation?

     **Alert aggregation** combines multiple related violations into a **single notification** to cut noise. If ten services breach a CPU threshold during the same infrastructure event, aggregation can deliver one incident rather than ten pages, so responders see a coherent problem instead of an alert storm.

     **[⬆ Back to Top](#table-of-contents)**

169. ### How do you reduce alert fatigue?

     - Prefer **baseline/anomaly** conditions over brittle static thresholds.
     - Set **meaningful thresholds** grounded in historical data and business impact.
     - **Group related conditions** and tune incident preferences.
     - Use **muting rules** during deployments and maintenance windows.
     - Route notifications to the **right channels** and people.
     - **Review alert history** regularly and prune conditions that produce false positives.

     **[⬆ Back to Top](#table-of-contents)**

170. ### What are muting rules?

     **Muting rules** suppress **notifications** (while still recording violations) for specified conditions or time windows. They can be **scheduled** (nightly maintenance) or **event-driven** (triggered by a deployment tag). Muting prevents predictable, expected alerts from paging anyone during known-noisy periods without disabling the underlying monitoring.

     **[⬆ Back to Top](#table-of-contents)**

171. ### How do you configure escalation policies?

     Integrate New Relic with an incident-management tool (**PagerDuty, Opsgenie**) and define **escalation policies** there: notify the primary on-call first, then escalate to secondary responders if the incident isn't acknowledged within a timeout. New Relic sends the incident via a notification channel (PagerDuty, Slack, email, webhook), and the downstream tool handles the escalation chain.

     **[⬆ Back to Top](#table-of-contents)**

172. ### How do you integrate New Relic with PagerDuty?

     1. In **PagerDuty**, create a service and obtain its **integration key**.
     2. In **New Relic**, add a **PagerDuty notification destination/channel** and paste the integration key.
     3. **Associate** that channel with the relevant alert policy (via a workflow).

     New Relic incidents then automatically create PagerDuty incidents, which follow PagerDuty's escalation and on-call schedules.

     **[⬆ Back to Top](#table-of-contents)**

173. ### How do you integrate New Relic with Slack?

     1. Add the **New Relic app** to your Slack workspace (OAuth authorization).
     2. Create a **Slack notification destination** in New Relic, choosing the target channel or user.
     3. **Link** it to your alert policies via a workflow.

     Incidents then post to Slack with details and a deep link back to the incident in New Relic, so responders can triage from chat.

     **[⬆ Back to Top](#table-of-contents)**

174. ### What are workflows in New Relic?

     **Workflows** are automations that act on alert events — they decide **which issues** (by filter) trigger **which actions** (notify a channel, create a ticket, run an integration). They connect alert policies to notification destinations and support **ITSM integrations** like ServiceNow and Jira, enabling automatic ticket creation and enrichment when incidents fire.

     **[⬆ Back to Top](#table-of-contents)**

175. ### What are issue intelligence capabilities?

     **Issue intelligence** (part of New Relic AI / AIOps) **correlates related incidents** across signals, applies machine learning to **suppress noise**, and **suggests probable root causes**. It surfaces related issues together and links them to the relevant traces and logs, so responders spend less time connecting dots and more time fixing the problem.

     **[⬆ Back to Top](#table-of-contents)**

176. ### How do you monitor SLO violations?

     Define **SLIs** as NRQL queries (e.g., percentage of requests under 500 ms), create an **SLO** with a target (e.g., 99.9%) and a measurement window, then alert on **error-budget burn rate**:

     ```sql
     -- SLI: success ratio (good events / valid events)
     SELECT percentage(count(*), WHERE duration < 0.5 AND error IS false)
     FROM Transaction WHERE appName = 'checkout' SINCE 28 days AGO
     ```

     Dashboards track SLO attainment over time and burn-rate alerts page you when the budget is being consumed too quickly.

     **[⬆ Back to Top](#table-of-contents)**

177. ### What is alert noise reduction?

     **Alert noise reduction** is the combined use of **muting rules, alert aggregation, dynamic (baseline/anomaly) thresholds, and ML-based correlation** to keep notifications meaningful. New Relic AI filters out transient spikes and groups related symptoms so responders aren't drowned in low-value pages — the goal is high signal-to-noise so every page is actionable.

     **[⬆ Back to Top](#table-of-contents)**

178. ### How do you troubleshoot missing alerts?

     1. **Check the condition's evaluation window** and thresholds — too long a window can delay or suppress firing.
     2. **Confirm data is actually being ingested** — if the NRQL query returns no data, the condition may not evaluate (check the "loss of signal" setting).
     3. **Verify the policy is enabled** and associated with the right entities/workflow.
     4. **Review incident preferences** — aggregation may have folded it into an existing incident.
     5. **Test the NRQL query** in the query builder to confirm it returns results.

     **[⬆ Back to Top](#table-of-contents)**

179. ### What is incident correlation?

     **Incident correlation** groups related incidents that share attributes — same host, service, or error type — treating multiple symptom alerts as manifestations of **one underlying problem**. Instead of five separate pages for one root cause, correlation presents a single, richer incident, reducing noise and speeding diagnosis.

     **[⬆ Back to Top](#table-of-contents)**

180. ### How do you create actionable alerts?

     - Alert on metrics that **directly affect customer experience** (latency, error rate) rather than proxy metrics.
     - Choose thresholds from **historical data and business objectives**, not guesses.
     - Include **context in the notification** — service name, environment, and a **runbook link**.
     - Add **deep links** to the relevant dashboard and traces so the responder starts investigating immediately.
     - Ensure each alert maps to **a clear action** — if there's nothing to do, it shouldn't page.

     **[⬆ Back to Top](#table-of-contents)**


## SRE & Reliability Engineering

181. ### What are the Four Golden Signals?

     The **Four Golden Signals** (from Google's SRE book) are the minimal set of metrics to monitor any user-facing system:

     - **Latency** — how long requests take (distinguish successful vs. failed latency).
     - **Traffic** — demand on the system (requests per second).
     - **Errors** — rate of failing requests.
     - **Saturation** — how "full" the service or its resources are (CPU, memory, queue depth).

     Together they answer "is it slow, is it busy, is it failing, is it full?"

     **[⬆ Back to Top](#table-of-contents)**

182. ### How do you measure availability using New Relic?

     Use **synthetic monitors** or uptime checks to probe endpoints and measure success rate, and/or compute availability from transaction data. Availability is the ratio of successful checks (or requests) to total over a window:

     ```sql
     SELECT percentage(count(*), WHERE result = 'SUCCESS') AS 'Availability %'
     FROM SyntheticCheck WHERE monitorName = 'checkout-ping' SINCE 7 days AGO
     ```

     Alert when availability drops below the SLA target.

     **[⬆ Back to Top](#table-of-contents)**

183. ### What is an SLI?

     A **Service Level Indicator (SLI)** is a **measurable attribute** of a service that reflects its performance or reliability — request latency, error rate, throughput, availability. It's typically expressed as a ratio of good events to valid events and computed via NRQL or metrics. The SLI is the *measurement* on which SLOs and SLAs are built.

     **[⬆ Back to Top](#table-of-contents)**

184. ### What is an SLO?

     A **Service Level Objective (SLO)** is a **target value** for an SLI over a period — e.g., "99.5% of requests must complete in under 400 ms over 28 days." The complement of the SLO target is the **error budget** (the allowable failure). SLOs are internal goals that drive engineering priorities and alerting.

     **[⬆ Back to Top](#table-of-contents)**

185. ### What is an SLA?

     A **Service Level Agreement (SLA)** is a **formal, contractual commitment** to customers, specifying performance targets and the **penalties** for missing them. SLAs are external and legally meaningful; they're usually set **less stringent than internal SLOs** so that breaching an SLO (an early warning) doesn't immediately mean breaching the SLA (a contractual penalty).

     **[⬆ Back to Top](#table-of-contents)**

186. ### How do you create SLOs in New Relic?

     Use New Relic's **Service Level Management**. Define the **SLI as an NRQL query** (good events vs. valid events), choose a **target percentage** and a **rolling window**, and New Relic tracks **error-budget consumption** and integrates with alerts:

     ```sql
     -- "Valid" events
     FROM Transaction SELECT count(*) WHERE appName = 'checkout'
     -- "Good" events (success and fast)
     FROM Transaction SELECT count(*) WHERE appName = 'checkout' AND error IS false AND duration < 0.4
     ```

     **[⬆ Back to Top](#table-of-contents)**

187. ### What is error budget?

     The **error budget** is the **allowable amount of failure** within an SLO period — the inverse of the SLO target. For a 99.9% uptime SLO, the budget is **0.1% downtime** (≈43 minutes per 30 days). The error budget reframes reliability as a resource: as long as budget remains, teams can ship features; when it's exhausted, focus shifts to reliability work.

     **[⬆ Back to Top](#table-of-contents)**

188. ### How do you track error budget burn rates?

     **Burn rate** is how fast the error budget is being consumed relative to the time elapsed. A burn rate of 1 means you'll exactly exhaust the budget by period end; a burn rate of 10 means you'll exhaust it 10× too fast. New Relic's **SLO reporting** shows burn-rate graphs, and you set **multi-window burn-rate alerts** (e.g., fast burn over 1 hour and slow burn over 6 hours) to catch both acute and gradual reliability regressions.

     **[⬆ Back to Top](#table-of-contents)**

189. ### How do you monitor reliability trends?

     Build dashboards for **SLI metrics and error-budget consumption over time**, using **moving averages** and **`COMPARE WITH`** to contrast against previous periods. Trending these week-over-week reveals whether reliability is improving or regressing, informing where to invest engineering effort.

     ```sql
     SELECT percentage(count(*), WHERE error IS false)
     FROM Transaction WHERE appName = 'checkout'
     SINCE 1 week AGO COMPARE WITH 1 week AGO TIMESERIES 1 day
     ```

     **[⬆ Back to Top](#table-of-contents)**

190. ### How do you perform root cause analysis?

     **Correlate anomalies across metrics, logs, and traces.** Use distributed tracing to identify **which service** introduced the latency or error, examine **logs around the same timestamp** for stack traces or error messages, and check for **deployment or config-change markers** that coincide with the onset. Document findings and update runbooks so the next occurrence is faster to resolve.

     **[⬆ Back to Top](#table-of-contents)**

191. ### How do you use observability for incident management?

     Observability surfaces the signals needed to **detect, triage, and resolve** incidents quickly. New Relic's dashboards, traces, and logs give on-call engineers immediate context; **alert routing** (PagerDuty/Slack) gets the right people involved; and **issue intelligence** correlates symptoms to a likely cause. The unified data means responders move from "something's wrong" to "here's the failing span and its logs" in minutes.

     **[⬆ Back to Top](#table-of-contents)**

192. ### How do you measure service health?

     Monitor the key signals — **latency, error rate, throughput, CPU/memory, and capacity** — and roll them into a **health score or SLO attainment** per service. Dashboards and alerts should reflect this composite health so a single indicator tells you whether a service is healthy, degraded, or failing.

     **[⬆ Back to Top](#table-of-contents)**

193. ### How do you identify reliability bottlenecks?

     Analyze metrics, traces, and logs to find services or resources that produce **latency spikes or errors**. Look for high **saturation** (CPU, memory, disk, thread pools) and **external dependencies that time out**. Distributed traces are especially powerful here — they show exactly which hop in a multi-service request consistently dominates latency.

     **[⬆ Back to Top](#table-of-contents)**

194. ### How do you monitor customer experience?

     Use **Real User Monitoring (RUM)** (Browser agent) and **Mobile monitoring** to capture page-load time, interaction delays, JavaScript errors, and crash rates from actual end-user devices. Correlate this front-end data with backend APM metrics to determine whether poor experience originates in the browser, the network, or the server — closing the loop from user pain to backend cause.

     **[⬆ Back to Top](#table-of-contents)**

195. ### How do you establish observability maturity?

     Assess current capabilities across **telemetry coverage, tracing, SLOs, alerting, and incident response**. Then advance deliberately: instrument **all** services (ideally via OpenTelemetry for portability), adopt **distributed tracing** everywhere, define **SLOs and error budgets** for critical paths, implement **logs-in-context**, and **automate runbooks**. Maturity progresses from reactive monitoring toward proactive, predictive observability with strong cultural adoption.

     **[⬆ Back to Top](#table-of-contents)**


## Cloud Monitoring

196. ### How does New Relic integrate with AWS?

     Through the **AWS integration** (CloudWatch Metric Streams or API polling) and **AWS Lambda layers**. Use New Relic's AWS integration wizard to link your account; metrics for **EC2, RDS, Lambda, DynamoDB, SQS, SNS**, and 50+ services then flow in. Lambda functions use the **`newrelic-lambda` layer** to capture invocation metrics, cold starts, and traces. **CloudWatch Metric Streams** (via Kinesis Firehose) is the recommended low-latency ingestion path.

     **[⬆ Back to Top](#table-of-contents)**

197. ### How does New Relic integrate with Azure?

     Use the **Azure Monitor integration**. Link your Azure subscription in the New Relic portal, and metrics for **Azure VMs, App Services, Azure Functions, AKS, and SQL databases** flow into New Relic. Azure Functions can be instrumented with the New Relic **.NET agent** (or the Azure Functions monitor) for code-level detail beyond platform metrics.

     **[⬆ Back to Top](#table-of-contents)**

198. ### How does New Relic integrate with GCP?

     Integrate via the **GCP integration** (built on the Operations Suite / formerly Stackdriver). Connect your GCP project, and metrics for **Compute Engine, GKE, Cloud Functions, Cloud Run, and BigQuery** are collected. Logs and traces can additionally be exported from GCP to New Relic via the **OTLP exporter** for full correlation.

     **[⬆ Back to Top](#table-of-contents)**

199. ### What AWS services can be monitored?

     New Relic's AWS integration supports **50+ services**, including **EC2, ECS/EKS, RDS, DynamoDB, ElastiCache, Lambda, S3 (usage metrics), CloudFront, ELB/ALB/NLB, SQS, SNS, Kinesis, API Gateway, CloudWatch Logs, IAM, and Billing**. This breadth lets you monitor an entire AWS estate alongside the application code running on it.

     **[⬆ Back to Top](#table-of-contents)**

200. ### How do you monitor Azure AKS clusters?

     Use the **Kubernetes integration** (the `nri-bundle` Helm chart) on the AKS cluster for pod/node/container metrics, and additionally enable the **Azure Monitor integration** to capture Azure-platform metrics (node VM CPU/memory, managed control-plane metrics). Combining both gives a complete picture from the Azure infrastructure layer up through the workloads.

     **[⬆ Back to Top](#table-of-contents)**

201. ### How do you monitor Azure App Services?

     Install the appropriate **language agent** (.NET, Java, Node.js) in the App Service for code-level APM, and use the **Azure integration** to collect platform metrics (HTTP queue length, CPU, memory). Together they show both application internals and the hosting platform's health.

     **[⬆ Back to Top](#table-of-contents)**

202. ### How do you monitor AWS Lambda functions?

     Use the **`newrelic-lambda` layer**. For Java, the layer plus the New Relic Lambda extension captures **cold starts, duration, invocation errors, and traces**. Configure the license key and account ID via the function's **environment variables**, and enable log ingestion through the extension or a CloudWatch subscription.

     ```yaml
     # serverless.yml (Java Lambda)
     functions:
       processOrder:
         handler: com.example.OrderHandler::handleRequest
         layers:
           - arn:aws:lambda:us-east-1:451483290750:layer:NewRelicJava17:XX
         environment:
           NEW_RELIC_ACCOUNT_ID: ${env:NEW_RELIC_ACCOUNT_ID}
           NEW_RELIC_LAMBDA_HANDLER: com.example.OrderHandler::handleRequest
     ```

     **[⬆ Back to Top](#table-of-contents)**

203. ### What cloud-native metrics are collected?

     Cloud integrations collect **service-specific** metrics: read/write throughput and throttles for **DynamoDB**, CPU credit balance for **T-family EC2**, request count and latency for **load balancers** and **API Gateway**, queue depth for **SQS**, memory/CPU for **containers**, and storage/connection metrics for managed databases. Each service exposes the metrics its provider publishes.

     **[⬆ Back to Top](#table-of-contents)**

204. ### How do you monitor managed databases?

     Use the database **integrations** for RDS, Azure SQL, Cloud SQL, or BigQuery. These collect **CPU utilization, disk I/O, connection counts, queries per second, read/write latency, and storage usage**. Combine the infrastructure-level database metrics with **APM instrumentation of the client code** to see both the database's own health and how the application's queries perform against it.

     **[⬆ Back to Top](#table-of-contents)**

205. ### How do you correlate cloud infrastructure with application performance?

     Use **tags** (`region`, `instanceId`, `resourceGroup`) to link infrastructure metrics with APM data, then build NRQL queries or dashboards that line up `SystemSample`/cloud-integration metrics against `Transaction` events for the same entities. **Distributed tracing** further pinpoints which specific Lambda or App Service instance handled a given slow request, tying the cloud resource directly to the user-facing impact.

     **[⬆ Back to Top](#table-of-contents)**


## Advanced & Scenario-Based Questions

206. ### A Spring Boot application's response time suddenly increases. How would you troubleshoot using New Relic?

     1. **Open the APM summary** for the service and confirm *when* response time spiked and whether **throughput** or **error rate** changed at the same time (a throughput surge points to load; flat throughput points to a downstream slowdown).
     2. **Use the transaction breakdown** to see whether time shifted into app code, the database, or external calls.
     3. **Inspect slow transaction traces** to find the exact slow segment or query.
     4. **Check JVM/infrastructure metrics** — GC time, heap, CPU — for resource pressure.
     5. **Correlate with logs and deployment markers** — a recent deploy is a frequent culprit.

     ```sql
     SELECT average(duration), rate(count(*), 1 minute), percentage(count(*), WHERE error IS true)
     FROM Transaction WHERE appName = 'order-service'
     SINCE 2 hours AGO TIMESERIES
     ```

     **[⬆ Back to Top](#table-of-contents)**

207. ### Users report intermittent API failures. How would you identify the root cause?

     Use **error analytics** to filter by endpoint and error class, then open **error traces and correlated logs** for stack traces and HTTP status codes. Check **infrastructure metrics** for resource spikes that coincide with the failures, and use **distributed tracing** to find which downstream dependency is failing intermittently. Finally, review **recent deployments or config changes** that align with the onset.

     ```sql
     SELECT count(*) FROM TransactionError
     WHERE appName = 'order-service'
     FACET error.class, httpResponseCode SINCE 3 hours AGO TIMESERIES
     ```

     **[⬆ Back to Top](#table-of-contents)**

208. ### How would you investigate a memory leak using New Relic?

     1. Look for **steadily increasing heap usage** (especially Old Gen) that never recovers after GC — the signature of a leak.
     2. Check **GC frequency and pause times** climbing as the heap fills.
     3. Use the **Thread Profiler** to find threads accumulating objects.
     4. **Capture a heap dump** when memory is high and analyze it with Eclipse MAT to find the dominant retained objects.
     5. Optionally track suspect **object counts via custom metrics**.

     ```sql
     SELECT average(`apm.service.memory.heap.used`) FROM Metric
     WHERE appName = 'order-service' TIMESERIES SINCE 6 hours AGO
     ```

     **[⬆ Back to Top](#table-of-contents)**

209. ### How would you analyze high GC pauses in production?

     Monitor **GC time and pause durations** via JVM metrics and check whether pauses correlate with response-time or throughput degradation. If they do, consider **tuning heap sizes** or switching **GC algorithm** (e.g., to G1 or ZGC for lower pause times). Use transaction traces to find **allocation spikes** and optimize code to reduce object churn (object pooling, avoiding unnecessary allocations in hot paths).

     ```sql
     SELECT average(`apm.service.gc.pause.duration`), rate(count(*), 1 minute)
     FROM Metric WHERE appName = 'order-service'
     AND metricName LIKE 'apm.service.gc%' TIMESERIES SINCE 3 hours AGO
     ```

     **[⬆ Back to Top](#table-of-contents)**

210. ### How would you identify a slow database query impacting application performance?

     Open the APM **Databases** tab and sort queries by **response time** and **call count** to find the offender. Use a **transaction trace** to see the context in which the query runs (and whether it's an N+1 pattern firing many times). Then **optimize the query or add an index**, and verify the improvement in New Relic afterward.

     ```sql
     SELECT average(duration), count(*), max(duration)
     FROM Transaction WHERE appName = 'order-service'
     FACET name WHERE name LIKE 'Datastore%'
     SINCE 1 hour AGO ORDER BY average(duration) DESC
     ```

     **[⬆ Back to Top](#table-of-contents)**

211. ### How would you troubleshoot Kafka consumer lag using New Relic?

     Monitor **consumer lag per topic/partition** and compare it against the **producer rate** — lag grows when consumption can't keep up with production. Check the **consumer's CPU and memory** for resource starvation, and use **distributed tracing** to see whether **downstream processing** (a slow DB write or external call inside the consumer) is the real bottleneck. Remediate by **scaling consumers** to the partition count, tuning **poll batch sizes**, or optimizing the processing logic.

     ```sql
     SELECT latest(consumer.lag) FROM Metric
     WHERE consumerGroup = 'order-processing-group'
     FACET topic, partition SINCE 30 minutes AGO TIMESERIES
     ```

     **[⬆ Back to Top](#table-of-contents)**

212. ### How would you detect a dependency service outage?

     Watch the APM **External Services** tab for rising **error rates or response times** to a specific host. **Distributed tracing** shows exactly where spans fail in the call chain, and **logs** typically reveal connection errors (timeouts, refused connections). Set **alerts on error rates for critical external services** so an outage is caught proactively rather than via user complaints.

     ```sql
     SELECT percentage(count(*), WHERE error IS true), average(duration)
     FROM Span WHERE category = 'http' AND service.name = 'order-service'
     FACET http.url SINCE 30 minutes AGO TIMESERIES
     ```

     **[⬆ Back to Top](#table-of-contents)**

213. ### How would you monitor a microservices architecture with 100+ services?

     **Organize into workloads** by business function and **tag** services by team/domain so you can navigate at scale. Build **golden-signals dashboards** per workload, use the **Service Map** to understand dependencies, and rely on **distributed tracing** to follow cross-service requests. Define **SLOs only for critical services** so attention focuses where it matters, and lean on **issue intelligence** to correlate the inevitable alert volume.

     **[⬆ Back to Top](#table-of-contents)**

214. ### How would you implement observability for an AKS-hosted Spring Boot platform?

     1. Install the **New Relic Kubernetes bundle** on the AKS cluster (DaemonSet + KSM).
     2. Instrument the Spring Boot apps with the **New Relic Java agent** or **OpenTelemetry**.
     3. Forward container logs via **New Relic Logs** (Fluent Bit Helm chart), with `trace.id` in the log pattern for logs-in-context.
     4. Define **SLOs and alerts** for latency and error rate on the critical services.
     5. Use **Cluster Explorer** to monitor nodes/pods and correlate restarts with application latency.

     **[⬆ Back to Top](#table-of-contents)**

215. ### How would you create a dashboard for business transactions and technical metrics?

     **Instrument custom events** for business moments (`Checkout`, `PaymentSuccess`) and query them alongside APM metrics. Build a single dashboard that pairs **business throughput, success/failure rates, and revenue** with **technical signals** like response time and error rate, so business and engineering stakeholders share one view.

     ```sql
     -- Business
     SELECT count(*) AS 'Checkouts', percentage(count(*), WHERE status = 'SUCCESS') AS 'Success %'
     FROM Checkout SINCE 1 day AGO TIMESERIES

     -- Technical (same dashboard)
     SELECT average(duration), percentage(count(*), WHERE error IS true) AS 'Error %'
     FROM Transaction WHERE appName = 'checkout' SINCE 1 day AGO TIMESERIES
     ```

     **[⬆ Back to Top](#table-of-contents)**

216. ### How would you monitor a payment processing workflow end-to-end?

     **Instrument every microservice** in the flow (auth → capture → settlement) with APM and **distributed tracing**, and attach **custom attributes** like `orderId` and `paymentId` to spans so a single payment can be followed across services. Enable **logs-in-context** to capture per-stage logs, build a **dashboard showing each stage's success/failure counts**, and **alert on error rates** at each stage. Span enrichment makes it possible to query "all failed settlements for a given merchant".

     ```java
     @Trace(dispatcher = true)
     public void settle(Payment payment) {
         NewRelic.addCustomParameter("paymentId", payment.getId());
         NewRelic.addCustomParameter("orderId", payment.getOrderId());
         NewRelic.addCustomParameter("stage", "settlement");
         // settlement logic
     }
     ```

     **[⬆ Back to Top](#table-of-contents)**

217. ### How would you reduce monitoring costs while maintaining observability?

     - **Prioritize high-value telemetry** and drop noisy/redundant data with **drop filters**.
     - **Sample high-volume traces** (tail-based to keep the interesting ones).
     - **Convert verbose logs to metrics** where only counts/rates are needed.
     - Reserve **Data Plus / extended retention** only for data that requires it.
     - **Monitor ingest usage** continuously and tune retention per data type.

     The aim is to cut volume on low-information data while preserving the signals you actually use for diagnosis and SLOs.

     **[⬆ Back to Top](#table-of-contents)**

218. ### How would you design alerting for a high-volume e-commerce platform?

     - Define **SLOs** for checkout latency and error rate, and alert on **error-budget burn rate**.
     - Use **baseline/anomaly alerts** for traffic so seasonal peaks don't false-positive.
     - Add **NRQL alerts** on key endpoints (cart, checkout, payment).
     - **Group alerts by service** and tune incident preferences to avoid storms.
     - Integrate with **PagerDuty** and set **escalation policies**.
     - Use **anomaly detection** to catch unusual patterns like bot/fraud traffic surges.

     **[⬆ Back to Top](#table-of-contents)**

219. ### How would you implement OpenTelemetry with New Relic in a cloud-native environment?

     Deploy the **OpenTelemetry Collector** as a sidecar or DaemonSet, instrument services with the **OTel SDK or auto-instrumentation**, and configure the Collector's **OTLP exporter** to send to New Relic. Set **resource attributes** (`service.name`, `deployment.environment`) so entities are named correctly, validate the data lands in New Relic, and **tune sampling** to balance cost against trace completeness.

     ```yaml
     exporters:
       otlp:
         endpoint: otlp.nr-data.net:4317
         headers: { api-key: ${NEW_RELIC_LICENSE_KEY} }
     service:
       pipelines:
         traces:  { receivers: [otlp], processors: [batch], exporters: [otlp] }
         metrics: { receivers: [otlp], processors: [batch], exporters: [otlp] }
     ```

     **[⬆ Back to Top](#table-of-contents)**

220. ### How would you establish an observability strategy for a large enterprise migrating to microservices?

     1. **Assess** existing instrumentation and identify coverage gaps.
     2. **Standardize on a telemetry framework** — OpenTelemetry — and roll out agents/SDKs across services.
     3. **Define SLOs and error budgets** for critical services first.
     4. **Invest in distributed tracing and logs-in-context** so cross-service requests are debuggable.
     5. Create **shared dashboards and runbooks** and establish naming/tagging conventions.
     6. **Educate teams** on using the tooling and reviewing their own SLOs.
     7. **Iterate** — regularly review metrics and refine instrumentation as the architecture evolves toward proactive, predictive observability.

     **[⬆ Back to Top](#table-of-contents)**

---

### Disclaimer

The questions and answers in this document are a curated summary of commonly asked New Relic interview questions. They cover concepts from foundational through advanced and scenario-based depth. There is no guarantee that these exact questions will appear in any given interview — the purpose is to help you rapidly review key concepts and build deep understanding. Product details, pricing, and retention windows change over time, so always verify current specifics against New Relic's official documentation. Contributions and corrections are welcome.

Good luck with your interview 😊

---
