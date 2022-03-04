## carvel
Nginx Package  
|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|pullPolicy|NGINX image pull policy|string|IfNotPresent|
|debug|Set to true if you would like to see extra information on logs|string|false|
|Replicas|Number of NGINX replicas to deploy|integer|1|
|containerPorts.http|Sets http port inside NGINX  container|integer|8080|
|containerPorts.https|Sets https port inside NGINX container|string|Empty|
|livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe|integer|30|
|livenessProbe.periodSeconds|Period seconds for livenessProbe|integer|10|
|livenessProbe.timeoutSeconds|Timeout seconds for livenessProbe|integer|5|
|livenessProbe.successThreshold|Success threshold for livenessProbe|integer|1|
|livenessProbe.failureThreshold|Failure threshold for livenessProbe|integer|6|
|readinessProbe.initialDelaySeconds|Initial delay seconds for readinessProbe|integer|5|
|readinessProbe.periodSeconds|Period seconds for readinessProbe|integer|5|
|readinessProbe.timeoutSeconds|Timeout seconds for readinessProbe|integer|3|
|readinessProbe.successThreshold|Success threshold for readinessProbe|integer|1|
|readinessProbe.failureThreshold|Failure threshold for readinessProbe|integer|3|
|automountServiceAccountToken|Auto-mount the service account token in the pod|string|false|
|podSecurityContext.fsGroup|Set NGINX pod's Security Context fsGroup|integer|1001|
|containerSecurityContext.runAsUser|Set NGINX container's Security Context runAsUser|integer|1001|
|containerSecurityContext.runAsNonRoot|Set NGINX container's Security Context runAsNonRoot|string|true|
|autoscaling.minReplicas|Minimum number of replicas to scale back|integer|1|
|autoscaling.maxReplicas|Maximum number of replicas to scale out|integer|1|
|autoscaling.targetCPU|Target CPU utilization percentage|string|“ ”|
|autoscaling.targetMemory|Target Memory utilization percentage|string|“ ”|
|ingress.pathType|Ingress path type|strin|ImplementationSpecific|
|ingress.apiVersion|Force Ingress API version|string|“ ”|
|ingress.hostname|Default host for the ingress resource|string|nginx.local|
|ingress.path|The Path to Nginx. You may need to set this to '/*' in order to use this with ALB ingress controllers|string|/|
|ingress.annotations|Additional annotations for the Ingress resource. To enable certificate autogeneration, place here your cert-manager annotations|string|{}|
|ingress.tls|Create TLS Secret|string|false|
|metrics.port|NGINX Container Status Port scraped by Prometheus Exporter|string|“ “|
|securityContext.runAsUser|Set NGINX Exporter container's Security Context runAsUser|integer|1001|
|serviceMonitor.namespace|Namespace in which Prometheus is running|string|“ “|
|serviceMonitor.interval|Interval at which metrics should be scraped|string|“ “|
|serviceMonitor.scrapeTimeout|Timeout after which the scrape is ended|string|“ “|
|serviceMonitor.selector|Prometheus instance selector labels|string|{}|
|serviceMonitor.additionalLabels|Additional labels that can be used so PodMonitor will be discovered by Prometheus|string|{}|
|healthIngress.pathType|Ingress path type|string|ImplementationSpecific|
|healthIngress.hostname|When the health ingress is enabled, a host pointing to this will be created|string|example.local|
|healthIngress.pathType|Additional annotations for the Ingress resource. To enable certificate autogeneration, place here your cert-manager annotations.|string|{}|
|healthIngress.tls|Enable TLS configuration for the hostname|string|false|
|prometheusRule.namespace|Namespace for the PrometheusRule Resource|string|“ “|
|prometheusRule.additionalLabels|Additional labels that can be used so PrometheusRule will be discovered by Prometheus|string|{}|
