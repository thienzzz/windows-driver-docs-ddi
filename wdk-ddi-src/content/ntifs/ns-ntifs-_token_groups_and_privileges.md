---
UID : NS:ntifs._TOKEN_GROUPS_AND_PRIVILEGES
title : _TOKEN_GROUPS_AND_PRIVILEGES
author : windows-driver-content
description : TOKEN_GROUPS_AND_PRIVILEGES contains information about the group security identifiers (SIDs) and privileges in an access token.
old-location : ifsk\token_groups_and_privileges.htm
old-project : ifsk
ms.assetid : 27d4793d-bdb4-46c5-b6e4-a2136e899adc
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : _TOKEN_GROUPS_AND_PRIVILEGES, TOKEN_GROUPS_AND_PRIVILEGES, *PTOKEN_GROUPS_AND_PRIVILEGES
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ntifs.h
req.include-header : Ntifs.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : TOKEN_GROUPS_AND_PRIVILEGES
req.alt-loc : ntifs.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : 
req.typenames : TOKEN_GROUPS_AND_PRIVILEGES, *PTOKEN_GROUPS_AND_PRIVILEGES
---

# _TOKEN_GROUPS_AND_PRIVILEGES structure
TOKEN_GROUPS_AND_PRIVILEGES contains information about the group security identifiers (SIDs) and privileges in an access token.

## Syntax
````
typedef struct _TOKEN_GROUPS_AND_PRIVILEGES {
  ULONG                SidCount;
  ULONG                SidLength;
  PSID_AND_ATTRIBUTES  Sids;
  ULONG                RestrictedSidCount;
  ULONG                RestrictedSidLength;
  PSID_AND_ATTRIBUTES  RestrictedSids;
  ULONG                PrivilegeCount;
  ULONG                PrivilegeLength;
  PLUID_AND_ATTRIBUTES Privileges;
  LUID                 AuthenticationId;
} TOKEN_GROUPS_AND_PRIVILEGES, *PTOKEN_GROUPS_AND_PRIVILEGES;
````

## Members

        
            `AuthenticationId`

            The locally unique identifier (LUID) of the authenticator of the token.
        
            `PrivilegeCount`

            Specifies the number of privileges included in the access token.
        
            `PrivilegeLength`

            Specifies the length, in bytes, needed to hold all of the privileges.
        
            `Privileges`

            A pointer to <a href="..\wdm\ns-wdm-_luid_and_attributes.md">LUID_AND_ATTRIBUTES</a> structures that contain a set of privileges.
        
            `RestrictedSidCount`

            Specifies the number of the restricted SIDs included in the access token.
        
            `RestrictedSidLength`

            Specifies the length, in bytes, required to hold all of the restricted SIDs.
        
            `RestrictedSids`

            A pointer to <a href="..\ntifs\ns-ntifs-_sid_and_attributes.md">SID_AND_ATTRIBUTES</a> structures that contain a set of restricted SIDs and corresponding attributes.
        
            `SidCount`

            Specifies the number of SIDs in the access token.
        
            `SidLength`

            Specifies the length, in bytes, required to hold all of the user SIDs and the account SID for the group.
        
            `Sids`

            A pointer to SID_AND_ATTRIBUTES structures that contain a set of SIDs and corresponding attributes.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntifs.h (include Ntifs.h) |

    ## See Also

        <dl>
<dt>
<a href="..\wdm\ns-wdm-_acl.md">ACL</a>
</dt>
<dt>
<a href="..\wdm\ns-wdm-_luid_and_attributes.md">LUID_AND_ATTRIBUTES</a>
</dt>
<dt>
<a href="..\wudfddi\ne-wudfddi-_security_impersonation_level.md">SECURITY_IMPERSONATION_LEVEL</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-sefiltertoken.md">SeFilterToken</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-sequeryinformationtoken.md">SeQueryInformationToken</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-setokenisrestricted.md">SeTokenIsRestricted</a>
</dt>
<dt>
<a href="..\ntifs\ns-ntifs-_sid.md">SID</a>
</dt>
<dt>
<a href="..\ntifs\ns-ntifs-_sid_and_attributes.md">SID_AND_ATTRIBUTES</a>
</dt>
<dt>
<a href="..\ntifs\ns-ntifs-_token_default_dacl.md">TOKEN_DEFAULT_DACL</a>
</dt>
<dt>
<a href="..\ntifs\ne-ntifs-_token_information_class.md">TOKEN_INFORMATION_CLASS</a>
</dt>
<dt>
<a href="..\ntifs\ns-ntifs-_token_owner.md">TOKEN_OWNER</a>
</dt>
<dt>
<a href="..\ntifs\ns-ntifs-_token_primary_group.md">TOKEN_PRIMARY_GROUP</a>
</dt>
<dt>
<a href="..\ntifs\ns-ntifs-_token_privileges.md">TOKEN_PRIVILEGES</a>
</dt>
<dt>
<a href="..\ntifs\ns-ntifs-_token_source.md">TOKEN_SOURCE</a>
</dt>
<dt>
<a href="..\ntifs\ns-ntifs-_token_statistics.md">TOKEN_STATISTICS</a>
</dt>
<dt>
<a href="..\ntifs\ne-ntifs-_token_type.md">TOKEN_TYPE</a>
</dt>
<dt>
<a href="..\ntifs\ns-ntifs-_token_user.md">TOKEN_USER</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-zwqueryinformationtoken.md">ZwQueryInformationToken</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-zwsetinformationtoken.md">ZwSetInformationToken</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20TOKEN_GROUPS_AND_PRIVILEGES structure%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>