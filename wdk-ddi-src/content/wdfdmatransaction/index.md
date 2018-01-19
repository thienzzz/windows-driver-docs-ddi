---
UID : NA:wdfdmatransaction
ms.assetid : 09e21580-15ec-3bb5-835c-b303aad3067a
ms.author : windowsdriverdev
ms.date : 01/18/18
ms.keywords : 
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : portal
---

# wdfdmatransaction.h header



wdfdmatransaction.h contains the following programming interfaces:





## Functions
| Title | Description |
| ---- |:---- |
| [EVT_WDF_DMA_TRANSACTION_CONFIGURE_DMA_CHANNEL](nc-wdfdmatransaction-evt_wdf_dma_transaction_configure_dma_channel.md) | A driver's EvtDmaTransactionConfigureDmaChannel event callback function configures the DMA adapter for a system-mode DMA enabler. |
| [EVT_WDF_DMA_TRANSACTION_DMA_TRANSFER_COMPLETE](nc-wdfdmatransaction-evt_wdf_dma_transaction_dma_transfer_complete.md) | A driver's EvtDmaTransactionDmaTransferComplete event callback function is called when the system-mode controller has completed the current DMA transfer. |
| [EVT_WDF_RESERVE_DMA](nc-wdfdmatransaction-evt_wdf_reserve_dma.md) | The EvtReserveDma event callback function is called when the framework has reserved resources to execute and release a transaction. Reserved resources include map registers and the WDM DMA adapter's lock. |
| [WdfDmaTransactionAllocateResources](nf-wdfdmatransaction-wdfdmatransactionallocateresources.md) | The WdfDmaTransactionAllocateResources method reserves a single-packet or system-mode DMA enabler for exclusive (and repeated) use with the specified transaction object. |
| [WdfDmaTransactionCancel](nf-wdfdmatransaction-wdfdmatransactioncancel.md) | The WdfDmaTransactionCancel method attempts to cancel a DMA transaction that is waiting for the allocation of map registers. |
| [WdfDmaTransactionCreate](nf-wdfdmatransaction-wdfdmatransactioncreate.md) | The WdfDmaTransactionCreate method creates a DMA transaction. |
| [WdfDmaTransactionDmaCompleted](nf-wdfdmatransaction-wdfdmatransactiondmacompleted.md) | The WdfDmaTransactionDmaCompleted method notifies the framework that a device's DMA transfer operation is completed. |
| [WdfDmaTransactionDmaCompletedFinal](nf-wdfdmatransaction-wdfdmatransactiondmacompletedfinal.md) | The WdfDmaTransactionDmaCompletedFinal method notifies the framework that a device's DMA transfer operation has completed with an underrun condition and supplies the length of the completed transfer. |
| [WdfDmaTransactionDmaCompletedWithLength](nf-wdfdmatransaction-wdfdmatransactiondmacompletedwithlength.md) | The WdfDmaTransactionDmaCompletedWithLength method notifies the framework that a device's DMA transfer operation is complete and supplies the length of the completed transfer. |
| [WdfDmaTransactionExecute](nf-wdfdmatransaction-wdfdmatransactionexecute.md) | The WdfDmaTransactionExecute method begins the execution of a specified DMA transaction. |
| [WdfDmaTransactionFreeResources](nf-wdfdmatransaction-wdfdmatransactionfreeresources.md) | The WdfDmaTransactionFreeResources method releases DMA resources that the driver previously allocated by calling WdfDmaTransactionAllocateResources. |
| [WdfDmaTransactionGetBytesTransferred](nf-wdfdmatransaction-wdfdmatransactiongetbytestransferred.md) | The WdfDmaTransactionGetBytesTransferred method returns the total number of bytes that have been transferred for a specified DMA transaction. |
| [WdfDmaTransactionGetCurrentDmaTransferLength](nf-wdfdmatransaction-wdfdmatransactiongetcurrentdmatransferlength.md) | The WdfDmaTransactionGetCurrentDmaTransferLength method returns the size of the current DMA transfer. |
| [WdfDmaTransactionGetDevice](nf-wdfdmatransaction-wdfdmatransactiongetdevice.md) | The WdfDmaTransactionGetDevice method returns a handle to the framework device object that is associated with a specified DMA transaction. |
| [WdfDmaTransactionGetRequest](nf-wdfdmatransaction-wdfdmatransactiongetrequest.md) | The WdfDmaTransactionGetRequest method retrieves a handle to the framework request object that is associated with a specified DMA transaction. |
| [WdfDmaTransactionGetTransferInfo](nf-wdfdmatransaction-wdfdmatransactiongettransferinfo.md) | The WdfDmaTransactionGetTransferInfo method returns the number of map registers and scatter/gather list entries required for an initialized DMA transaction. |
| [WdfDmaTransactionInitialize](nf-wdfdmatransaction-wdfdmatransactioninitialize.md) | The WdfDmaTransactionInitialize method initializes a specified DMA transaction. |
| [WdfDmaTransactionInitializeUsingOffset](nf-wdfdmatransaction-wdfdmatransactioninitializeusingoffset.md) | The WdfDmaTransactionInitializeUsingOffset method initializes a specified DMA transaction by using a byte offset into an MDL chain. |
| [WdfDmaTransactionInitializeUsingRequest](nf-wdfdmatransaction-wdfdmatransactioninitializeusingrequest.md) | The WdfDmaTransactionInitializeUsingRequest method initializes a specified DMA transaction by using the parameters of a specified I/O request. |
| [WdfDmaTransactionRelease](nf-wdfdmatransaction-wdfdmatransactionrelease.md) | The WdfDmaTransactionRelease method terminates a specified DMA transaction without deleting the associated DMA transaction object. |
| [WdfDmaTransactionSetChannelConfigurationCallback](nf-wdfdmatransaction-wdfdmatransactionsetchannelconfigurationcallback.md) | The WdfDmaTransactionSetChannelConfigurationCallback method registers a channel configuration event callback function for a system-mode DMA transaction. |
| [WdfDmaTransactionSetDeviceAddressOffset](nf-wdfdmatransaction-wdfdmatransactionsetdeviceaddressoffset.md) | The WdfDmaTransactionSetDeviceAddressOffset method specifies the offset of the register that the system DMA controller will access when performing the DMA operation. |
| [WdfDmaTransactionSetImmediateExecution](nf-wdfdmatransaction-wdfdmatransactionsetimmediateexecution.md) | The WdfDmaTransactionSetImmediateExecution method marks the specified DMA transaction so that calls to WdfDmaTransactionExecute and WdfDmaTransactionAllocateResources initiate the transaction immediately or fail. |
| [WdfDmaTransactionSetMaximumLength](nf-wdfdmatransaction-wdfdmatransactionsetmaximumlength.md) | The WdfDmaTransactionSetMaximumLength method sets the maximum length for the DMA transfers that are associated with a specified DMA transaction. |
| [WdfDmaTransactionSetSingleTransferRequirement](nf-wdfdmatransaction-wdfdmatransactionsetsingletransferrequirement.md) | The WdfDmaTransactionSetSingleTransferRequirement method specifies that a DMA transaction must complete in a single transfer. |
| [WdfDmaTransactionSetTransferCompleteCallback](nf-wdfdmatransaction-wdfdmatransactionsettransfercompletecallback.md) | The WdfDmaTransactionSetTransferCompleteCallback method registers a transfer completion event callback function for a system-mode DMA transaction. |
| [WdfDmaTransactionStopSystemTransfer](nf-wdfdmatransaction-wdfdmatransactionstopsystemtransfer.md) | The WdfDmaTransactionStopSystemTransfer method attempts to stop a system-mode DMA transfer after the framework has called EvtProgramDma. |
| [WdfDmaTransactionWdmGetTransferContext](nf-wdfdmatransaction-wdfdmatransactionwdmgettransfercontext.md) | The WdfDmaTransactionWdmGetTransferContext method retrieves the WDM transfer context that is associated with a DMA transaction. |