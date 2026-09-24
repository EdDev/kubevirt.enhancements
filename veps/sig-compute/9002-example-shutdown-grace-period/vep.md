---
title: Configurable VM shutdown grace period override
vep-number: 4
creation-date: "2026-09-24"
status: provisional
authors:
  - "@EdDev"
owning-sig: sig-compute
reviewers:
  - TBD
approvers:
  - TBD
feature-gate: VMShutdownGracePeriodOverride
stage: alpha
milestone:
  alpha: "v1.11"
---

# VEP #4: Configurable VM shutdown grace period override

## Overview

Allow a VirtualMachine to override the default shutdown grace period on a
per-VM basis, instead of relying solely on the cluster-wide default.

## Motivation

Some workloads need longer than the default grace period to shut down
cleanly (e.g. databases flushing to disk), while others benefit from a much
shorter period to speed up test/CI environments. Today this is not
configurable per VM.

## Goals

- Add an optional field to the VirtualMachine spec to override the shutdown
  grace period.

## Non Goals

- Changing the cluster-wide default grace period.

## Definition of Users

- VM owners who need workload-specific shutdown timing.

## User Stories

- As a VM owner, I want to set a longer grace period for my database VM so
  that it always has time to flush data before being force-stopped.

## Repos

- kubevirt/kubevirt

## Design

This is a demonstration VEP created solely to validate VEP-282's governance
tooling (front matter validator and VEP Freeze enforcer) on a fork. It is
not a real proposal and is not intended to be implemented.

## API Examples

N/A -- demonstration only.

## Alternatives

N/A -- demonstration only.

## Does it belong to core KubeVirt?

N/A -- demonstration only.

## Scalability

N/A -- demonstration only.

## Update/Rollback Compatibility

N/A -- demonstration only.

## Functional Testing Approach

N/A -- demonstration only.

## Implementation History

## Graduation Requirements

### Alpha

### Beta

### GA
