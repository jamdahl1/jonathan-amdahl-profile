# Private-System Interface Examples

The underlying career-management application is private.

The examples below document the intended public-facing interaction model. They should
be treated as interface examples rather than a promise that every command shown here
is currently stable.

## Show the candidate profile

```bash
resume candidate-show jonathan_amdahl
```

Conceptual output:

```text
Jonathan D. Amdahl

Primary domains
  Cloud Engineering
  DevOps / Platform Engineering
  Automation Engineering

Supporting domains
  Observability / SRE
  Network Operations / Open RAN
  AI Infrastructure
  Electrical Engineering
```

## Show a target

```bash
resume target-show platform-engineer
```

Conceptual output:

```text
Platform Engineer

Core
  Linux
  Cloud
  Terraform
  Kubernetes
  CI/CD
  Python

Supporting
  Observability
  Networking
  Helm
```

## Assess candidate against a target

```bash
resume target-assess   --candidate jonathan_amdahl   --target platform-engineer
```

Conceptual output:

```text
Strong
  Linux
  Python
  Cloud
  CI/CD
  Observability

Demonstrated
  Terraform
  Kubernetes
  Docker

Developing
  Helm
  Ansible
```

## Build a targeted projection

```bash
resume build   --candidate jonathan_amdahl   --target platform-engineer
```

Conceptual result:

```text
Targeted resume/profile projection generated.
```

## Boundary

The public repository does not contain:

- private source code
- raw job descriptions
- recruiter correspondence
- internal assessment records
- private scoring logic
- local filesystem state
- confidential employer information
