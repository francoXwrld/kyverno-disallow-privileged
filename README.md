# Kyverno Policy - Disallow Privileged Containers

Blocks pods running with `privileged: true` - a common CIS Kubernetes benchmark failure.

## Why?
Privileged containers can access host resources and break container isolation. This policy enforces least privilege.

## How to use
kubectl apply -f policy.yaml
kubectl apply -f test-pod-bad.yaml # should FAIL
kubectl apply -f test-pod-good.yaml # should PASS

## Related to
K8s Pod Security Standards, CIS Benchmark, LFX CNCF projects
Author: Franco - K8s Security focus
