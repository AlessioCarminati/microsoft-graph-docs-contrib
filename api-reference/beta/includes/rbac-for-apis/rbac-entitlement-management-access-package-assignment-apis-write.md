---
author: markwahl-msft
ms.topic: include
---

<!-- Applies to:
- accessPackageAssignment
- accessPackageAssignmentPolicy
- accessPackageAssignmentRequest
- accessPackageAssignmentRequestWorkflowExtension
- accessPackageAssignmentWorkflowExtension
-->

In delegated scenarios with work or school accounts, the signed-in user must also be assigned an administrator role with supported role permissions through one of the following options:

- [A role in the Entitlement Management system](/entra/id-governance/entitlement-management-delegate) where the least privileged role is *AccessPackage assignment manager*. **This is the least privileged option.**
- A custom role with the `microsoft.directory/entitlementManagement/allProperties/allTasks` Microsoft Entra role permission.
- A [Microsoft Entra role](/entra/identity/role-based-access-control/permissions-reference?toc=%2Fgraph%2Ftoc.json), where the following least privileged roles are supported for this operation:
    - User Administrator
    - Identity Governance Administrator

In app-only scenarios, the calling app can be assigned one of the preceding supported roles instead of the `EntitlementManagement.ReadWrite.All` application permission. The *AccessPackage assignment manager* role is less privileged than the `EntitlementManagement.ReadWrite.All` application permission.

For more information, see [Delegation and roles in entitlement management](/entra/id-governance/entitlement-management-delegate) and [how to delegate access governance to access package managers in entitlement management](/entra/id-governance/entitlement-management-delegate-managers).
