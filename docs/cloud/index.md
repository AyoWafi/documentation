---
id: index
title: Temporal Cloud documentation
sidebar_label: Temporal Cloud
description: Temporal Cloud documentation, including explanations and usage.
toc_max_heading_level: 4
---

<!-- THIS FILE IS GENERATED. DO NOT EDIT THIS FILE DIRECTLY -->

Temporal Cloud is a managed, hosted Temporal environment that provides a platform for [Temporal Applications](/temporal/#temporal-application)—an alternative to deploying and operating your own [Temporal Cluster](/clusters).

Temporal Cloud is offered in units of isolation known as [Namespaces](/namespaces). You can provision and use one or more Cloud Namespaces. A typical use case is to use separate Namespaces as development, testing, integration, staging, and production environments for an application.

:::note Join the Temporal Cloud waitlist

Access to Temporal Cloud is currently by invitation only.
You can [join the waitlist](https://pages.temporal.io/cloud-early-access).

:::

- [Get started with Temporal Cloud](/cloud/how-to-get-started-with-temporal-cloud)
- [Manage certificates in Temporal Cloud](/cloud/how-to-manage-certificates-in-temporal-cloud)
- [Manage Namespaces in Temporal Cloud](/cloud/how-to-manage-namespaces-in-temporal-cloud)
- [tcld (Temporal Cloud command-line interface)](/cloud/tcld)
- [Temporal Cloud release notes](/cloud/release-notes)

## Temporal Cloud Account Id

A Temporal Cloud Account Id is a unique identifier for a customer for the entire time they use Temporal Cloud.
Temporal Technologies assigns each Account Id, which is an opaque code of five or six alphanumeric characters, such as `f45a2`.

## Account-level Roles

When a Global Admin invites a user to join an account, the Global Admin selects one of the following Roles for that user:

- **Global Admin**
  - Has full administrative permissions across the account, including users and usage
  - Has Namespace Admin [permissions](/cloud/#namespace-level-permissions) on all [Namespaces](/namespaces) in the account
- **Developer**
  - Can create and update Namespaces; has full control over [Workflows](/workflows)
  - Has Namespace Admin permissions for each Namespace created by that user
- **Read-Only:** Can only read information

## Cloud Namespace Name

A Cloud Namespace Name is a customer-supplied name for a [Namespace](/namespaces) in Temporal Cloud.
Each Namespace Name, such as `accounting-production`, is unique within the scope of a customer's account.
It cannot be changed after the Namespace is provisioned.

Each Namespace Name must conform to the following rules:

- A Namespace Name must contain at least 2 characters and no more than 34 characters.
- A Namespace Name must begin with a letter, end with a letter or number, and contain only letters, numbers, and the hyphen (-) character.
- Each hyphen (-) character must be immediately preceded _and_ followed by a letter or number; consecutive hyphens are not permitted.
- All letters in a Namespace Name must be lowercase.

## Cloud Namespace Id

A Cloud Namespace Id is a globally unique identifier for a [Namespace](/namespaces) in Temporal Cloud.
A Namespace Id is formed by concatenating the following:

1. A [Namespace Name](#cloud-namespace-name)
1. A period (.)
1. The [Account Id](#temporal-cloud-account-id) to which the Namespace belongs

For example, for the Account Id `f45a2` and Namespace Name `accounting-production`, the Namespace Id is `accounting-production.f45a2`.

## Namespace-level permissions

A [Global Admin](/cloud/#account-level-roles) can assign permissions for any [Namespace](/namespaces) in an account.
A Developer can assign permissions for a Namespace they create.

For a Namespace, a user can have one of the following permissions:

- **Namespace Admin:** Can create and edit Namespaces; can create, rename, update, and delete [Workflows](/workflows)
- **Write:** Can create, rename, update, and delete Workflows within the Namespace
- **Read-Only:** Can only read information from the Namespace
