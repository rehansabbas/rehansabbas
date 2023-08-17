apiVersion: mutations.gatekeeper.sh/v1
kind: Assign
metadata:
  name: job-params-ttl-after-finished
spec:
  applyTo:
  - groups: [""]
    kinds: ["Pod"]
    versions: ["v1"]
  match:
    scope: Namespaced
    kinds:
    - apiGroups: ["*"]
      kinds: ["Pod"]
    namespaces: ["elis-demolive","elis-demomock","elis-demomocklockbox","elis-demomyuscis","elis-demosith","elis-dt","elis-dtperf","elis-ft","elis-pt","elis-sky","elis-smktest","elis-trn","elis-trn2"]
  location: "spec.initContainers[name:*].securityContext.ttlSecondsAfterFinished"
  parameters:
    assign:
      value: 600
    pathTests:
      - subPath: "spec.initContainers[name:*].securityContext.ttlSecondsAfterFinished"
        condition: MustNotExist
