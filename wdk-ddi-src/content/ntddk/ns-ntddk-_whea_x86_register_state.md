---
UID : NS:ntddk._WHEA_X86_REGISTER_STATE
title : _WHEA_X86_REGISTER_STATE
author : windows-driver-content
description : The WHEA_X86_REGISTER_STATE structure describes the state of an x86 processor's registers.
old-location : whea\whea_x86_register_state.htm
old-project : whea
ms.assetid : 64079b03-9771-4940-a19e-a29389cbf2fe
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : _WHEA_X86_REGISTER_STATE, WHEA_X86_REGISTER_STATE, *PWHEA_X86_REGISTER_STATE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ntddk.h
req.include-header : Ntddk.h
req.target-type : Windows
req.target-min-winverclnt : Supported in Windows Server 2008, Windows Vista SP1, and later versions of Windows.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : WHEA_X86_REGISTER_STATE
req.alt-loc : ntddk.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : WHEA_X86_REGISTER_STATE, *PWHEA_X86_REGISTER_STATE
---

# _WHEA_X86_REGISTER_STATE structure
The WHEA_X86_REGISTER_STATE structure describes the state of an x86 processor's registers.

## Syntax
````
typedef struct _WHEA_X86_REGISTER_STATE {
  ULONG     Eax;
  ULONG     Ebx;
  ULONG     Ecx;
  ULONG     Edx;
  ULONG     Esi;
  ULONG     Edi;
  ULONG     Ebp;
  ULONG     Esp;
  USHORT    Cs;
  USHORT    Ds;
  USHORT    Ss;
  USHORT    Es;
  USHORT    Fs;
  USHORT    Gs;
  ULONG     Eflags;
  ULONG     Eip;
  ULONG     Cr0;
  ULONG     Cr1;
  ULONG     Cr2;
  ULONG     Cr3;
  ULONG     Cr4;
  ULONGLONG Gdtr;
  ULONGLONG Idtr;
  USHORT    Ldtr;
  USHORT    Tr;
} WHEA_X86_REGISTER_STATE, *PWHEA_X86_REGISTER_STATE;
````

## Members

        
            `Cr0`

            The control register 0.
        
            `Cr1`

            The control register 1.
        
            `Cr2`

            The control register 2.
        
            `Cr3`

            The control register 3.
        
            `Cr4`

            The control register 4.
        
            `Cs`

            The code segment register.
        
            `Ds`

            The data segment register.
        
            `Eax`

            The accumulator register.
        
            `Ebp`

            The base pointer register.
        
            `Ebx`

            The base register.
        
            `Ecx`

            The count register.
        
            `Edi`

            The destination index register.
        
            `Edx`

            The data register.
        
            `Eflags`

            The flags register.
        
            `Eip`

            The instruction pointer register.
        
            `Es`

            The extra segment register.
        
            `Esi`

            The source index register.
        
            `Esp`

            The stack pointer register.
        
            `Fs`

            The general purpose segment register FS.
        
            `Gdtr`

            The global descriptor table register.
        
            `Gs`

            The general purpose segment register GS.
        
            `Idtr`

            The interrupt descriptor table register.
        
            `Ldtr`

            The local descriptor table register.
        
            `Ss`

            The stack segment register.
        
            `Tr`

            The task register.

    ## Remarks
        If the <b>RegisterContextType</b> member of a <a href="..\ntddk\ns-ntddk-_whea_xpf_context_info.md">WHEA_XPF_CONTEXT_INFO</a> structure is set to XPF_CONTEXT_INFO_32BITCONTEXT, the <b>RegisterData</b> member of that structure contains a WHEA_X86_REGISTER_STATE structure.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddk.h (include Ntddk.h) |

    ## See Also

        <dl>
<dt>
<a href="..\ntddk\ns-ntddk-_whea_xpf_context_info.md">WHEA_XPF_CONTEXT_INFO</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [whea\whea]:%20WHEA_X86_REGISTER_STATE structure%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>