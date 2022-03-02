# carvel
VMware project  
|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|pullPolicy|NGINX image pull policy|string|IfNotPresent|
|debug|Set to true if you would like to see extra information on logs|string|FALSE|
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
|automountServiceAccountToken|Auto-mount the service account token in the pod|string|FALSE|
