---
UID : NN:dbgeng.IDebugControl3
title : IDebugControl3
author : windows-driver-content
description : IDebugControl3 interface
old-location : debugger\idebugcontrol3.htm
old-project : debugger
ms.assetid : 95e714b4-4167-41a1-ab2c-b088dbaf5fe2
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : IDebugSystemObjects4, IDebugSystemObjects4::SetImplicitThreadDataOffset, SetImplicitThreadDataOffset
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : interface
req.header : dbgeng.h
req.include-header : Dbgeng.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IDebugControl3
req.alt-loc : dbgeng.h
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
req.typenames : "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugControl3 interface



## Methods

<p>The <b>IDebugControl3</b> interface has these methods.</p>

| Method | Description |
| ---- |:---- |
| [dbgeng.IDebugControl3.AddAssemblyOptions](nf-dbgeng-idebugcontrol3-addassemblyoptions.md) | The AddAssemblyOptions method turns on some of the assembly and disassembly options. |
| [dbgeng.IDebugControl3.AddBreakpoint](nf-dbgeng-idebugcontrol3-addbreakpoint.md) | The AddBreakpoint method creates a new breakpoint for the current target. |
| [dbgeng.IDebugControl3.AddEngineOptions](nf-dbgeng-idebugcontrol3-addengineoptions.md) | The AddEngineOptions method turns on some of the debugger engine's options. |
| [dbgeng.IDebugControl3.AddExtension](nf-dbgeng-idebugcontrol3-addextension.md) | The AddExtension method loads an extension library into the debugger engine. |
| [dbgeng.IDebugControl3.Assemble](nf-dbgeng-idebugcontrol3-assemble.md) | The Assemble method assembles a single processor instruction. The assembled instruction is placed in the target's memory. |
| [dbgeng.IDebugControl3.CallExtension](nf-dbgeng-idebugcontrol3-callextension.md) | The CallExtension method calls a debugger extension. |
| [dbgeng.IDebugControl3.CloseLogFile](nf-dbgeng-idebugcontrol3-closelogfile.md) | The CloseLogFile method closes the currently-open log file. |
| [dbgeng.IDebugControl3.CoerceValue](nf-dbgeng-idebugcontrol3-coercevalue.md) | The CoerceValue method converts a value of one type into a value of another type. |
| [dbgeng.IDebugControl3.CoerceValues](nf-dbgeng-idebugcontrol3-coercevalues.md) | The CoerceValues method converts an array of values into an array of values of different types. |
| [dbgeng.IDebugControl3.ControlledOutput](nf-dbgeng-idebugcontrol3-controlledoutput.md) | The ControlledOutput method formats a string and sends the result to output callbacks that were registered with some of the engine's clients. |
| [dbgeng.IDebugControl3.ControlledOutputVaList](nf-dbgeng-idebugcontrol3-controlledoutputvalist.md) | The ControlledOutputVaList method formats a string and sends the result to output callbacks that were registered with some of the engine's clients. |
| [dbgeng.IDebugControl3.Disassemble](nf-dbgeng-idebugcontrol3-disassemble.md) | The Disassemble method disassembles a processor instruction in the target's memory. |
| [dbgeng.IDebugControl3.Evaluate](nf-dbgeng-idebugcontrol3-evaluate.md) | The Evaluate method evaluates an expression, returning the result. |
| [dbgeng.IDebugControl3.Execute](nf-dbgeng-idebugcontrol3-execute.md) | The Execute method executes the specified debugger commands. |
| [dbgeng.IDebugControl3.ExecuteCommandFile](nf-dbgeng-idebugcontrol3-executecommandfile.md) | The ExecuteCommandFile method opens the specified file and executes the debugger commands that are contained within. |
| [dbgeng.IDebugControl3.GetActualProcessorType](nf-dbgeng-idebugcontrol3-getactualprocessortype.md) | The GetActualProcessorType method returns the processor type of the physical processor of the computer that is running the target. |
| [dbgeng.IDebugControl3.GetAssemblyOptions](nf-dbgeng-idebugcontrol3-getassemblyoptions.md) | The GetAssemblyOptions method returns the assembly and disassembly options that affect how the debugger engine assembles and disassembles processor instructions for the target. |
| [dbgeng.IDebugControl3.GetBreakpointById](nf-dbgeng-idebugcontrol3-getbreakpointbyid.md) | The GetBreakpointById method returns the breakpoint with the specified breakpoint ID. |
| [dbgeng.IDebugControl3.GetBreakpointByIndex](nf-dbgeng-idebugcontrol3-getbreakpointbyindex.md) | The GetBreakpointByIndex method returns the breakpoint located at the specified index. |
| [dbgeng.IDebugControl3.GetBreakpointParameters](nf-dbgeng-idebugcontrol3-getbreakpointparameters.md) | The GetBreakpointParameters method returns the parameters of one or more breakpoints. |
| [dbgeng.IDebugControl3.GetCodeLevel](nf-dbgeng-idebugcontrol3-getcodelevel.md) | The GetCodeLevel method returns the current code level and is mainly used when stepping through code. |
| [dbgeng.IDebugControl3.GetCurrentEventIndex](nf-dbgeng-idebugcontrol3-getcurrenteventindex.md) | The GetCurrentEventIndex method returns the index of the current event within the current list of events for the current target, if such a list exists. |
| [dbgeng.IDebugControl3.GetCurrentSystemUpTime](nf-dbgeng-idebugcontrol3-getcurrentsystemuptime.md) | The GetCurrentSystemUpTime method returns the number of seconds the current target's computer has been running since it was last started. |
| [dbgeng.IDebugControl3.GetCurrentTimeDate](nf-dbgeng-idebugcontrol3-getcurrenttimedate.md) | The GetCurrentTimeDate method returns the time of the current target. |
| [dbgeng.IDebugControl3.GetDebuggeeType](nf-dbgeng-idebugcontrol3-getdebuggeetype.md) | The GetDebuggeeType method describes the nature of the current target. |
| [dbgeng.IDebugControl3.GetDisassembleEffectiveOffset](nf-dbgeng-idebugcontrol3-getdisassembleeffectiveoffset.md) | The GetDisassembleEffectiveOffset method returns the address of the last instruction disassembled using Disassemble. |
| [dbgeng.IDebugControl3.GetDumpFormatFlags](nf-dbgeng-idebugcontrol3-getdumpformatflags.md) | The GetDumpFormatFlags method returns the flags that describe what information is available in a dump file target. |
| [dbgeng.IDebugControl3.GetEffectiveProcessorType](nf-dbgeng-idebugcontrol3-geteffectiveprocessortype.md) | The GetEffectiveProcessorType method returns the effective processor type of the processor of the computer that is running the target. |
| [dbgeng.IDebugControl3.GetEngineOptions](nf-dbgeng-idebugcontrol3-getengineoptions.md) | The GetEngineOptions method returns the engine's options. |
| [dbgeng.IDebugControl3.GetEventFilterCommand](nf-dbgeng-idebugcontrol3-geteventfiltercommand.md) | The GetEventFilterCommand method returns the debugger command that the engine will execute when a specified event occurs. |
| [dbgeng.IDebugControl3.GetEventFilterText](nf-dbgeng-idebugcontrol3-geteventfiltertext.md) | The GetEventFilterText method returns a short description of an event for a specific filter. |
| [dbgeng.IDebugControl3.GetEventIndexDescription](nf-dbgeng-idebugcontrol3-geteventindexdescription.md) | The GetEventIndexDescription method describes the specified event in a static list of events for the current target. |
| [dbgeng.IDebugControl3.GetExceptionFilterParameters](nf-dbgeng-idebugcontrol3-getexceptionfilterparameters.md) | The GetExceptionFilterParameters method returns the parameters for exception filters specified by exception codes or by index. |
| [dbgeng.IDebugControl3.GetExceptionFilterSecondCommand](nf-dbgeng-idebugcontrol3-getexceptionfiltersecondcommand.md) | The GetExceptionFilterSecondCommand method returns the command that will be executed by the debugger engine upon the second chance of a specified exception. |
| [dbgeng.IDebugControl3.GetExecutingProcessorType](nf-dbgeng-idebugcontrol3-getexecutingprocessortype.md) | The GetExecutingProcessorType method returns the executing processor type for the processor for which the last event occurred. |
| [dbgeng.IDebugControl3.GetExecutionStatus](nf-dbgeng-idebugcontrol3-getexecutionstatus.md) | The GetExecutionStatus method returns information about the execution status of the debugger engine. |
| [dbgeng.IDebugControl3.GetExpressionSyntax](nf-dbgeng-idebugcontrol3-getexpressionsyntax.md) | The GetExpressionSyntax method returns the current syntax that the engine is using for evaluating expressions. |
| [dbgeng.IDebugControl3.GetExpressionSyntaxNames](nf-dbgeng-idebugcontrol3-getexpressionsyntaxnames.md) | The GetExpressionSyntaxNames method returns the full and abbreviated names of an expression syntax. |
| [dbgeng.IDebugControl3.GetExtensionByPath](nf-dbgeng-idebugcontrol3-getextensionbypath.md) | The GetExtensionByPath method returns the handle for an already loaded extension library. |
| [dbgeng.IDebugControl3.GetExtensionFunction](nf-dbgeng-idebugcontrol3-getextensionfunction.md) | The GetExtensionFunction method returns a pointer to an extension function from an extension library. |
| [dbgeng.IDebugControl3.GetInterrupt](nf-dbgeng-idebugcontrol3-getinterrupt.md) | The GetInterrupt method checks whether a user interrupt was issued. |
| [dbgeng.IDebugControl3.GetInterruptTimeout](nf-dbgeng-idebugcontrol3-getinterrupttimeout.md) | The GetInterruptTimeout method returns the number of seconds that the engine will wait when requesting a break into the debugger. |
| [dbgeng.IDebugControl3.GetLastEventInformation](nf-dbgeng-idebugcontrol3-getlasteventinformation.md) | The GetLastEventInformation method returns information about the last event that occurred in a target. |
| [dbgeng.IDebugControl3.GetLogFile](nf-dbgeng-idebugcontrol3-getlogfile.md) | The GetLogFile method returns the name of the currently open log file. |
| [dbgeng.IDebugControl3.GetLogMask](nf-dbgeng-idebugcontrol3-getlogmask.md) | The GetLogMask method returns the output mask for the currently open log file. |
| [dbgeng.IDebugControl3.GetNearInstruction](nf-dbgeng-idebugcontrol3-getnearinstruction.md) | The GetNearInstruction method returns the location of a processor instruction relative to a given location. |
| [dbgeng.IDebugControl3.GetNotifyEventHandle](nf-dbgeng-idebugcontrol3-getnotifyeventhandle.md) | The GetNotifyEventHandle method receives the handle of the event that will be signaled after the next exception in a target. |
| [dbgeng.IDebugControl3.GetNumberBreakpoints](nf-dbgeng-idebugcontrol3-getnumberbreakpoints.md) | The GetNumberBreakpoints method returns the number of breakpoints for the current process. |
| [dbgeng.IDebugControl3.GetNumberEventFilters](nf-dbgeng-idebugcontrol3-getnumbereventfilters.md) | The GetNumberEventFilters method returns the number of event filters currently used by the engine. |
| [dbgeng.IDebugControl3.GetNumberEvents](nf-dbgeng-idebugcontrol3-getnumberevents.md) | The GetNumberEvents method returns the number of events for the current target, if the number of events is fixed. |
| [dbgeng.IDebugControl3.GetNumberExpressionSyntaxes](nf-dbgeng-idebugcontrol3-getnumberexpressionsyntaxes.md) | The GetNumberExpressionSyntaxes method returns the number of expression syntaxes that are supported by the engine. |
| [dbgeng.IDebugControl3.GetNumberPossibleExecutingProcessorTypes](nf-dbgeng-idebugcontrol3-getnumberpossibleexecutingprocessortypes.md) | The GetNumberPossibleExecutingProcessorTypes method returns the number of processor types that are supported by the computer running the current target. |
| [dbgeng.IDebugControl3.GetNumberProcessors](nf-dbgeng-idebugcontrol3-getnumberprocessors.md) | The GetNumberProcessors method returns the number of processors on the computer running the current target. |
| [dbgeng.IDebugControl3.GetNumberSupportedProcessorTypes](nf-dbgeng-idebugcontrol3-getnumbersupportedprocessortypes.md) | The GetNumberSupportedProcessorTypes method returns the number of processor types supported by the engine. |
| [dbgeng.IDebugControl3.GetNumberTextReplacements](nf-dbgeng-idebugcontrol3-getnumbertextreplacements.md) | The GetNumberTextReplacements method returns the number of currently defined user-named and automatic aliases. |
| [dbgeng.IDebugControl3.GetPageSize](nf-dbgeng-idebugcontrol3-getpagesize.md) | The GetPageSize method returns the page size for the effective processor mode. |
| [dbgeng.IDebugControl3.GetPossibleExecutingProcessorTypes](nf-dbgeng-idebugcontrol3-getpossibleexecutingprocessortypes.md) | The GetPossibleExecutingProcessorTypes method returns the processor types that are supported by the computer running the current target. |
| [dbgeng.IDebugControl3.GetProcessorTypeNames](nf-dbgeng-idebugcontrol3-getprocessortypenames.md) | The GetProcessorTypeNames method returns the full name and abbreviated name of the specified processor type. |
| [dbgeng.IDebugControl3.GetPromptText](nf-dbgeng-idebugcontrol3-getprompttext.md) | The GetPromptText method returns the standard prompt text that will be prepended to the formatted output specified in the OutputPrompt and OutputPromptVaList methods. |
| [dbgeng.IDebugControl3.GetRadix](nf-dbgeng-idebugcontrol3-getradix.md) | The GetRadix method returns the default radix (number base) used by the debugger engine when it evaluates and displays MASM expressions, and when it displays symbol information. |
| [dbgeng.IDebugControl3.GetReturnOffset](nf-dbgeng-idebugcontrol3-getreturnoffset.md) | The GetReturnOffset method returns the return address for the current function. |
| [dbgeng.IDebugControl3.GetSpecificFilterArgument](nf-dbgeng-idebugcontrol3-getspecificfilterargument.md) | The GetSpecificFilterArgument method returns the value of filter argument for thespecific filters that have an argument. |
| [dbgeng.IDebugControl3.GetSpecificFilterParameters](nf-dbgeng-idebugcontrol3-getspecificfilterparameters.md) | The GetSpecificFilterParameters method returns the parameters for specific event filters. |
| [dbgeng.IDebugControl3.GetStackTrace](nf-dbgeng-idebugcontrol3-getstacktrace.md) | The GetStackTrace method returns the frames at the top of the specified call stack. |
| [dbgeng.IDebugControl3.GetSupportedProcessorTypes](nf-dbgeng-idebugcontrol3-getsupportedprocessortypes.md) | The GetSupportedProcessorTypes method returns the processor types supported by the debugger engine. |
| [dbgeng.IDebugControl3.GetSystemErrorControl](nf-dbgeng-idebugcontrol3-getsystemerrorcontrol.md) | The GetSystemErrorControl method returns the control values for handling system errors. |
| [dbgeng.IDebugControl3.GetSystemVersion](nf-dbgeng-idebugcontrol3-getsystemversion.md) | The GetSystemVersion method returns information that identifies the operating system on the computer that is running the current target. |
| [dbgeng.IDebugControl3.GetTextMacro](nf-dbgeng-idebugcontrol3-gettextmacro.md) | The GetTextMacro method returns the value of a fixed-name alias. |
| [dbgeng.IDebugControl3.GetTextReplacement](nf-dbgeng-idebugcontrol3-gettextreplacement.md) | The GetTextReplacement method returns the value of a user-named alias or an automatic alias. |
| [dbgeng.IDebugControl3.GetWindbgExtensionApis32](nf-dbgeng-idebugcontrol3-getwindbgextensionapis32.md) | The GetWindbgExtensionApis32 method returns a structure that facilitates using the WdbgExts API. |
| [dbgeng.IDebugControl3.GetWindbgExtensionApis64](nf-dbgeng-idebugcontrol3-getwindbgextensionapis64.md) | The GetWindbgExtensionApis64 method returns a structure that facilitates using the WdbgExts API. |
| [dbgeng.IDebugControl3.IsPointer64Bit](nf-dbgeng-idebugcontrol3-ispointer64bit.md) | The IsPointer64Bit method determines if the effective processor uses 64-bit pointers. |
| [dbgeng.IDebugControl3.OpenLogFile](nf-dbgeng-idebugcontrol3-openlogfile.md) | The OpenLogFile method opens a log file that will receive output from the client objects. |
| [dbgeng.IDebugControl3.Output](nf-dbgeng-idebugcontrol3-output.md) | The Output method formats a string and send the result to output callbacks that have been registered with the engine's clients. |
| [dbgeng.IDebugControl3.OutputCurrentState](nf-dbgeng-idebugcontrol3-outputcurrentstate.md) | The OutputCurrentState method prints the current state of the current target to the debugger console. |
| [dbgeng.IDebugControl3.OutputDisassembly](nf-dbgeng-idebugcontrol3-outputdisassembly.md) | The OutputDisassembly method disassembles a processor instruction and sends the disassembly to the output callbacks. |
| [dbgeng.IDebugControl3.OutputDisassemblyLines](nf-dbgeng-idebugcontrol3-outputdisassemblylines.md) | The OutputDisassemblyLines method disassembles several processor instructions and sends the resulting assembly instructions to the output callbacks. |
| [dbgeng.IDebugControl3.OutputPrompt](nf-dbgeng-idebugcontrol3-outputprompt.md) | The OutputPrompt method formats and sends a user prompt to the output callback objects. |
| [dbgeng.IDebugControl3.OutputPromptVaList](nf-dbgeng-idebugcontrol3-outputpromptvalist.md) | The OutputPromptVaList method formats and sends a user prompt to the output callback objects. |
| [dbgeng.IDebugControl3.OutputStackTrace](nf-dbgeng-idebugcontrol3-outputstacktrace.md) | The OutputStackTrace method outputs either the supplied stack frame or the current stack frames. |
| [dbgeng.IDebugControl3.OutputTextReplacements](nf-dbgeng-idebugcontrol3-outputtextreplacements.md) | The OutputTextReplacements method prints all the currently defined user-named aliases to the debugger's output stream. |
| [dbgeng.IDebugControl3.OutputVaList](nf-dbgeng-idebugcontrol3-outputvalist.md) | The OutputVaList method formats a string and sends the result to the output callbacks that are registered with the engine's clients. |
| [dbgeng.IDebugControl3.OutputVersionInformation](nf-dbgeng-idebugcontrol3-outputversioninformation.md) | The OutputVersionInformation method prints version information about the debugger engine to the debugger console. |
| [dbgeng.IDebugControl3.ReadBugCheckData](nf-dbgeng-idebugcontrol3-readbugcheckdata.md) | The ReadBugCheckData method reads the kernel bug check code and related parameters. |
| [dbgeng.IDebugControl3.RemoveAssemblyOptions](nf-dbgeng-idebugcontrol3-removeassemblyoptions.md) | The RemoveAssemblyOptions method turns off some of the assembly and disassembly options. |
| [dbgeng.IDebugControl3.RemoveBreakpoint](nf-dbgeng-idebugcontrol3-removebreakpoint.md) | The RemoveBreakpoint method removes a breakpoint. |
| [dbgeng.IDebugControl3.RemoveEngineOptions](nf-dbgeng-idebugcontrol3-removeengineoptions.md) | The RemoveEngineOptions method turns off some of the engine's options. |
| [dbgeng.IDebugControl3.RemoveExtension](nf-dbgeng-idebugcontrol3-removeextension.md) | The RemoveExtension method unloads an extension library. |
| [dbgeng.IDebugControl3.RemoveTextReplacements](nf-dbgeng-idebugcontrol3-removetextreplacements.md) | The RemoveTextReplacements method removes all user-named aliases. |
| [dbgeng.IDebugControl3.ReturnInput](nf-dbgeng-idebugcontrol3-returninput.md) | The ReturnInput method is used by IDebugInputCallbacks objects to send an input string to the engine following a request for input. |
| [dbgeng.IDebugControl3.SetAssemblyOptions](nf-dbgeng-idebugcontrol3-setassemblyoptions.md) | The SetAssemblyOptions method sets the assembly and disassembly options that affect how the debugger engine assembles and disassembles processor instructions for the target. |
| [dbgeng.IDebugControl3.SetCodeLevel](nf-dbgeng-idebugcontrol3-setcodelevel.md) | The SetCodeLevel method sets the current code level and is mainly used when stepping through code. |
| [dbgeng.IDebugControl3.SetEffectiveProcessorType](nf-dbgeng-idebugcontrol3-seteffectiveprocessortype.md) | The SetEffectiveProcessorType method sets the effective processor type of the processor of the computer that is running the target. |
| [dbgeng.IDebugControl3.SetEngineOptions](nf-dbgeng-idebugcontrol3-setengineoptions.md) | The SetEngineOptions method changes the engine's options. |
| [dbgeng.IDebugControl3.SetEventFilterCommand](nf-dbgeng-idebugcontrol3-seteventfiltercommand.md) | The SetEventFilterCommand method sets a debugger command for the engine to execute when a specified event occurs. |
| [dbgeng.IDebugControl3.SetExceptionFilterParameters](nf-dbgeng-idebugcontrol3-setexceptionfilterparameters.md) | The SetExceptionFilterParameters method changes the break status and handling status for some exception filters. |
| [dbgeng.IDebugControl3.SetExceptionFilterSecondCommand](nf-dbgeng-idebugcontrol3-setexceptionfiltersecondcommand.md) | The SetExceptionFilterSecondCommand method sets the command that will be executed by the debugger engine on the second chance of a specified exception. |
| [dbgeng.IDebugControl3.SetExecutionStatus](nf-dbgeng-idebugcontrol3-setexecutionstatus.md) | The SetExecutionStatus method requests that the debugger engine enter an executable state. Actual execution will not occur until the next time WaitForEvent is called. |
| [dbgeng.IDebugControl3.SetExpressionSyntax](nf-dbgeng-idebugcontrol3-setexpressionsyntax.md) | The SetExpressionSyntax method sets the syntax that the engine will use to evaluate expressions. |
| [dbgeng.IDebugControl3.SetExpressionSyntaxByName](nf-dbgeng-idebugcontrol3-setexpressionsyntaxbyname.md) | The SetExpressionSyntaxByName method sets the syntax that the engine will use to evaluate expressions. |
| [dbgeng.IDebugControl3.SetInterrupt](nf-dbgeng-idebugcontrol3-setinterrupt.md) | The SetInterrupt method registers a user interrupt or breaks into the debugger. |
| [dbgeng.IDebugControl3.SetInterruptTimeout](nf-dbgeng-idebugcontrol3-setinterrupttimeout.md) | The SetInterruptTimeout method sets the number of seconds that the debugger engine should wait when requesting a break into the debugger. |
| [dbgeng.IDebugControl3.SetLogMask](nf-dbgeng-idebugcontrol3-setlogmask.md) | The SetLogMask method sets the output mask for the currently open log file. |
| [dbgeng.IDebugControl3.SetNextEventIndex](nf-dbgeng-idebugcontrol3-setnexteventindex.md) | The SetNextEventIndex method sets the next event for the current target by selecting the event from the static list of events for the target, if such a list exists. |
| [dbgeng.IDebugControl3.SetNotifyEventHandle](nf-dbgeng-idebugcontrol3-setnotifyeventhandle.md) | The SetNotifyEventHandle method sets the event that will be signaled after the next exception in a target. |
| [dbgeng.IDebugControl3.SetRadix](nf-dbgeng-idebugcontrol3-setradix.md) | The SetRadix method sets the default radix (number base) used by the debugger engine when it evaluates and displays MASM expressions, and when it displays symbol information. |
| [dbgeng.IDebugControl3.SetSpecificFilterArgument](nf-dbgeng-idebugcontrol3-setspecificfilterargument.md) | The SetSpecificFilterArgument method sets the value of filter argument for the specific filters that can have an argument. |
| [dbgeng.IDebugControl3.SetSpecificFilterParameters](nf-dbgeng-idebugcontrol3-setspecificfilterparameters.md) | The SetSpecificFilterParameters method changes the break status and handling status for some specific event filters. |
| [dbgeng.IDebugControl3.SetSystemErrorControl](nf-dbgeng-idebugcontrol3-setsystemerrorcontrol.md) | The SetSystemErrorControl method sets the control values for handling system errors. |
| [dbgeng.IDebugControl3.SetTextMacro](nf-dbgeng-idebugcontrol3-settextmacro.md) | The SetTextMacro method sets the value of a fixed-name alias. |
| [dbgeng.IDebugControl3.SetTextReplacement](nf-dbgeng-idebugcontrol3-settextreplacement.md) | The SetTextReplacement method sets the value of a user-named alias. |
| [dbgeng.IDebugControl3.WaitForEvent](nf-dbgeng-idebugcontrol3-waitforevent.md) | The WaitForEvent method waits for an event that breaks into the debugger engine application. |

## Remarks



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum UMDF version** |  |
| **Header** | dbgeng.h (include Dbgeng.h) |
| **DLL** |  |

    ## See Also

        <dl>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugcontrol.md">IDebugControl</a>
</dt>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugcontrol2.md">IDebugControl2</a>
</dt>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugcontrol4.md">IDebugControl4</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugControl3 interface%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>