---
title: Advanced Security Audit Policy Settings
ms.custom: na
ms.prod: windows-server-2012
ms.reviewer: na
ms.suite: na
ms.technology: 
  - techgroup-security
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0ac32135-3eba-474d-ae55-7cef0e92761f
---
# Advanced Security Audit Policy Settings
This reference for the IT professional provides information about  the Advanced Audit policy settings that are available in Windows operating systems and the audit events that they generate.

The 53 security audit policy settings under **Security Settings\\Advanced Audit Policy Configuration** can help your organization audit compliance with important business\-related and security\-related rules by tracking precisely defined activities, such as:

-   A group administrator has modified settings or data on servers that contain finance information.

-   An employee within a defined group has accessed an important file.

-   The correct system access control list \(SACL\) is applied to every file and folder or registry key on a computer or file share as a verifiable safeguard against undetected access.

You can access these audit policy settings through the Local Security Policy snap\-in \(secpol.msc\) on the local computer or by using Group Policy.

These Advanced Audit policy settings allow you to select only the behaviors that you want to monitor. You can exclude audit results for behaviors that are of little or no concern to you, or behaviors that create an excessive number of log entries. In addition, because security audit policies can be applied by using domain Group Policy Objects, audit policy settings can be modified, tested, and deployed to selected users and groups with relative simplicity.

When Advanced Security Audit policy settings are configured, events appear on computers running the supported versions of the Windows operating system as designated in the **Applies to** list at the beginning of this topic, in addition to Windows Server 2008 and Windows Vista.

Audit policy settings under **Security Settings\\Advanced Audit Policy Configuration** are available in the following categories:

-   **Account Logon**

    Configuring policy settings in this category can help you document attempts to authenticate account data on a domain controller or on a local Security Accounts Manager \(SAM\). Unlike Logon and Logoff policy settings and events, which track attempts to access a particular computer, settings and events in this category focus on the account database that is used. This category includes the following subcategories:

    -   [Audit Credential Validation](advanced-security-audit-policy-settings/Audit-Credential-Validation.md)

    -   [Audit Kerberos Authentication Service](advanced-security-audit-policy-settings/Audit-Kerberos-Authentication-Service.md)

    -   [Audit Kerberos Service Ticket Operations](advanced-security-audit-policy-settings/Audit-Kerberos-Service-Ticket-Operations.md)

    -   [Audit Other Logon - Logoff Events](advanced-security-audit-policy-settings/Audit-Other-Logon---Logoff-Events.md)

-   **Account Management**

    The security audit policy settings in this category can be used to monitor changes to user and computer accounts and groups. This category includes the following subcategories:

    -   [Audit Application Group Management](advanced-security-audit-policy-settings/Audit-Application-Group-Management.md)

    -   [Audit Computer Account Management](advanced-security-audit-policy-settings/Audit-Computer-Account-Management.md)

    -   [Audit Distribution Group Management](advanced-security-audit-policy-settings/Audit-Distribution-Group-Management.md)

    -   [Audit Other Account Management Events](advanced-security-audit-policy-settings/Audit-Other-Account-Management-Events.md)

    -   [Audit Security Group Management](advanced-security-audit-policy-settings/Audit-Security-Group-Management.md)

    -   [Audit User Account Management](advanced-security-audit-policy-settings/Audit-User-Account-Management.md)

-   **Detailed Tracking**

    Detailed Tracking security policy settings and audit events can be used to monitor the activities of individual applications and users on that computer, and to understand how a computer is being used. This category includes the following subcategories:

    -   [Audit DPAPI Activity](advanced-security-audit-policy-settings/Audit-DPAPI-Activity.md)

    -   [Audit Process Creation](advanced-security-audit-policy-settings/Audit-Process-Creation.md)

    -   [Audit Process Termination](advanced-security-audit-policy-settings/Audit-Process-Termination.md)

    -   [Audit RPC Events](advanced-security-audit-policy-settings/Audit-RPC-Events.md)

-   **DS Access**

    DS Access security audit policy settings provide a detailed audit trail of attempts to access and modify objects in Active Directory Domain Services \(AD DS\). These audit events are logged only on domain controllers. This category includes the following subcategories:

    -   [Audit Detailed Directory Service Replication](advanced-security-audit-policy-settings/Audit-Detailed-Directory-Service-Replication.md)

    -   [Audit Directory Service Access](advanced-security-audit-policy-settings/Audit-Directory-Service-Access.md)

    -   [Audit Directory Service Changes](advanced-security-audit-policy-settings/Audit-Directory-Service-Changes.md)

    -   [Audit Directory Service Replication](advanced-security-audit-policy-settings/Audit-Directory-Service-Replication.md)

-   **Logon\/Logoff**

    Logon\/Logoff security policy settings and audit events allow you to track attempts to log on to a computer interactively or over a network. These events are particularly useful for tracking user activity and identifying potential attacks on network resources. This category includes the following subcategories:

    -   [Audit Account Lockout](advanced-security-audit-policy-settings/Audit-Account-Lockout.md)

    -   [Audit IPsec Extended Mode](advanced-security-audit-policy-settings/Audit-IPsec-Extended-Mode.md)

    -   [Audit IPsec Main Mode](advanced-security-audit-policy-settings/Audit-IPsec-Main-Mode.md)

    -   [Audit IPsec Quick Mode](advanced-security-audit-policy-settings/Audit-IPsec-Quick-Mode.md)

    -   [Audit Logoff](advanced-security-audit-policy-settings/Audit-Logoff.md)

    -   [Audit Logon](advanced-security-audit-policy-settings/Audit-Logon.md)

    -   [Audit Network Policy Server](advanced-security-audit-policy-settings/Audit-Network-Policy-Server.md)

    -   [Audit Other Logon - Logoff Events](advanced-security-audit-policy-settings/Audit-Other-Logon---Logoff-Events.md)

    -   [Audit Special Logon](advanced-security-audit-policy-settings/Audit-Special-Logon.md)

-   **Object Access**

    Object Access policy settings and audit events allow you to track attempts to access specific objects or types of objects on a network or computer. To audit attempts to access a file, directory, registry key, or any other object, you must enable the appropriate Object Access auditing subcategory for success and\/or failure events. For example, the File System subcategory needs to be enabled to audit file operations, and the Registry subcategory needs to be enabled to audit registry accesses.

    Proving that these audit policies are in effect to an external auditor is more difficult. There is no easy way to verify that the proper SACLs are set on all inherited objects. To address this issue, see [Global Object Access Auditing](#BKMK_GlobalObjectAccess).

    This category includes the following subcategories:

    -   [Audit Application Generated](advanced-security-audit-policy-settings/Audit-Application-Generated.md)

    -   [Audit Certification Services](advanced-security-audit-policy-settings/Audit-Certification-Services.md)

    -   [Audit Detailed File Share](advanced-security-audit-policy-settings/Audit-Detailed-File-Share.md)

    -   [Audit File Share](advanced-security-audit-policy-settings/Audit-File-Share.md)

    -   [Audit File System](advanced-security-audit-policy-settings/Audit-File-System.md)

    -   [Audit Filtering Platform Connection](advanced-security-audit-policy-settings/Audit-Filtering-Platform-Connection.md)

    -   [Audit Filtering Platform Packet Drop](advanced-security-audit-policy-settings/Audit-Filtering-Platform-Packet-Drop.md)

    -   [Audit Handle Manipulation](advanced-security-audit-policy-settings/Audit-Handle-Manipulation.md)

    -   [Audit Kernel Object](advanced-security-audit-policy-settings/Audit-Kernel-Object.md)

    -   [Audit Other Object Access Events](advanced-security-audit-policy-settings/Audit-Other-Object-Access-Events.md)

    -   [Audit Registry](advanced-security-audit-policy-settings/Audit-Registry.md)

    -   [Audit SAM](advanced-security-audit-policy-settings/Audit-SAM.md)

-   **Policy Change**

    Policy Change audit events allow you to track changes to important security policies on a local system or network. Because policies are typically established by administrators to help secure network resources, monitoring changes or attempts to change these policies can be an important aspect of security management for a network. This category includes the following subcategories:

    -   [Audit Audit Policy Change](advanced-security-audit-policy-settings/Audit-Audit-Policy-Change.md)

    -   [Audit Authentication Policy Change](advanced-security-audit-policy-settings/Audit-Authentication-Policy-Change.md)

    -   [Audit Authorization Policy Change](advanced-security-audit-policy-settings/Audit-Authorization-Policy-Change.md)

    -   [Audit Filtering Platform Policy Change](advanced-security-audit-policy-settings/Audit-Filtering-Platform-Policy-Change.md)

    -   [Audit MPSSVC Rule-Level Policy Change](advanced-security-audit-policy-settings/Audit-MPSSVC-Rule-Level-Policy-Change.md)

    -   [Audit Other Policy Change Events](advanced-security-audit-policy-settings/Audit-Other-Policy-Change-Events.md)

-   **Privilege Use**

    Permissions on a network are granted for users or computers to complete defined tasks. Privilege Use security policy settings and audit events allow you to track the use of certain permissions on one or more systems. This category includes the following subcategories:

    -   [Audit Non-Sensitive Privilege Use](advanced-security-audit-policy-settings/Audit-Non-Sensitive-Privilege-Use.md)

    -   [Audit Sensitive Privilege Use](advanced-security-audit-policy-settings/Audit-Sensitive-Privilege-Use.md)

    -   [Audit Other Privilege Use Events](advanced-security-audit-policy-settings/Audit-Other-Privilege-Use-Events.md)

-   **System**

    System security policy settings and audit events allow you to track system\-level changes to a computer that are not included in other categories and that have potential security implications. This category includes the following subcategories:

    -   [Audit IPsec Driver](advanced-security-audit-policy-settings/Audit-IPsec-Driver.md)

    -   [Audit Other System Events](advanced-security-audit-policy-settings/Audit-Other-System-Events.md)

    -   [Audit Security State Change](advanced-security-audit-policy-settings/Audit-Security-State-Change.md)

    -   [Audit Security System Extension](advanced-security-audit-policy-settings/Audit-Security-System-Extension.md)

    -   [Audit System Integrity](advanced-security-audit-policy-settings/Audit-System-Integrity.md)

-   **Global Object Access**

    Global Object Access Auditing policy settings allow administrators to define computer system access control lists \(SACLs\) per object type for the file system or for the registry. The specified SACL is then automatically applied to every object of that type.

    Auditors will be able to prove that every resource in the system is protected by an audit policy by viewing the contents of the Global Object Access Auditing policy settings. For example, if auditors see a policy setting called "Track all changes made by group administrators," they know that this policy is in effect.

    Resource SACLs are also useful for diagnostic scenarios. For example, setting the Global Object Access Auditing policy to log all the activity for a specific user and enabling the policy to track "Access denied" events for the file system or registry can help administrators quickly identify which object in a system is denying a user access.

    > [!NOTE]
    > If a file or folder SACL and a Global Object Access Auditing policy setting \(or a single registry setting SACL and a Global Object Access Auditing policy setting\) are configured on a computer, the effective SACL is derived from combining the file or folder SACL and the Global Object Access Auditing policy. This means that an audit event is generated if an activity matches the file or folder SACL or the Global Object Access Auditing policy.

    This category includes the following subcategories:

    -   [File System &#40;Global Object Access Auditing&#41;](advanced-security-audit-policy-settings/File-System--Global-Object-Access-Auditing-.md)

    -   [Registry &#40;Global Object Access Auditing&#41;](advanced-security-audit-policy-settings/Registry--Global-Object-Access-Auditing-.md)

