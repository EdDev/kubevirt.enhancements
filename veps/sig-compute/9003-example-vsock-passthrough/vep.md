---
title: VSOCK device passthrough for VirtualMachines
vep-number: 5
creation-date: "2026-09-24"
status: implementable
authors:
  - "@EdDev"
owning-sig: sig-compute
reviewers:
  - TBD
approvers:
  - TBD
feature-gate: VSOCKPassthrough
stage: alpha
milestone:
  alpha: "v1.11"
---

# VEP #5: VSOCK device passthrough for VirtualMachines

## Overview

Expose a host VSOCK device to a VirtualMachine for host<->guest
communication without a network device.

## Motivation

Some guest agents and management tools prefer VSOCK over a virtual NIC for
control-plane communication, since it does not require IP configuration
inside the guest.

## Goals

- Allow a VirtualMachine to request a VSOCK device.

## Non Goals

- Replacing existing virtio-net based communication channels.

## Definition of Users

- Guest agent developers who need a network-independent communication channel.

## User Stories

- As a guest agent developer, I want a VSOCK device available in the guest so
  that my agent can talk to the host without depending on guest network
  configuration.

## Repos

- kubevirt/kubevirt

## Design

This is a demonstration VEP created solely to validate VEP-282's governance
tooling on a fork. It intentionally sets `status: implementable` while
leaving `reviewers` and `approvers` as `TBD`, to demonstrate that the
front matter validator correctly blocks this: a VEP cannot be marked
implementable until named reviewers and approvers have committed to it.

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
