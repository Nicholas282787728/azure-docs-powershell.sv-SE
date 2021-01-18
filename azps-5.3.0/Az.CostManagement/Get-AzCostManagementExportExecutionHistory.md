---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 7bb337837f9bd2be532c4eead8d8379b7cf04fe9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524284"
---
# <span data-ttu-id="da3ad-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="da3ad-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="da3ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="da3ad-103">Åtgärden för att hämta körnings historiken för en export för det definierade scopet och export namnet.</span><span class="sxs-lookup"><span data-stu-id="da3ad-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="da3ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da3ad-104">SYNTAX</span></span>

### <span data-ttu-id="da3ad-105">Skaffa (standard)</span><span class="sxs-lookup"><span data-stu-id="da3ad-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="da3ad-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="da3ad-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="da3ad-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da3ad-107">DESCRIPTION</span></span>
<span data-ttu-id="da3ad-108">Åtgärden för att hämta körnings historiken för en export för det definierade scopet och export namnet.</span><span class="sxs-lookup"><span data-stu-id="da3ad-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="da3ad-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da3ad-109">EXAMPLES</span></span>

### <span data-ttu-id="da3ad-110">Exempel 1: skaffa AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="da3ad-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="da3ad-111">Få AzCostManagementExportExecutionHistory via ExportName och omfattning</span><span class="sxs-lookup"><span data-stu-id="da3ad-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="da3ad-112">Exempel 2: get AzCostManagementExportExecutionHistory by InputObject</span><span class="sxs-lookup"><span data-stu-id="da3ad-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="da3ad-113">Få AzCostManagementExportExecutionHistory via InputObject</span><span class="sxs-lookup"><span data-stu-id="da3ad-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="da3ad-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da3ad-114">PARAMETERS</span></span>

### <span data-ttu-id="da3ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da3ad-115">-DefaultProfile</span></span>
<span data-ttu-id="da3ad-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da3ad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3ad-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="da3ad-117">-ExportName</span></span>
<span data-ttu-id="da3ad-118">Exportera namn.</span><span class="sxs-lookup"><span data-stu-id="da3ad-118">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3ad-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da3ad-119">-InputObject</span></span>
<span data-ttu-id="da3ad-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="da3ad-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da3ad-121">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="da3ad-121">-Scope</span></span>
<span data-ttu-id="da3ad-122">Den här parametern definierar omfattningen av costmanagement från olika perspektiv, "ResourceGroup" och "tillhandahåller tjänst".</span><span class="sxs-lookup"><span data-stu-id="da3ad-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3ad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da3ad-123">CommonParameters</span></span>
<span data-ttu-id="da3ad-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da3ad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da3ad-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da3ad-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da3ad-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da3ad-126">INPUTS</span></span>

### <span data-ttu-id="da3ad-127">Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="da3ad-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="da3ad-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da3ad-128">OUTPUTS</span></span>

### <span data-ttu-id="da3ad-129">Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. Api20200601. IExportExecution</span><span class="sxs-lookup"><span data-stu-id="da3ad-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="da3ad-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da3ad-130">NOTES</span></span>

<span data-ttu-id="da3ad-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="da3ad-131">ALIASES</span></span>

<span data-ttu-id="da3ad-132">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="da3ad-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="da3ad-133">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="da3ad-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da3ad-134">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="da3ad-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="da3ad-135">INPUTOBJECT <ICostManagementIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="da3ad-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="da3ad-136">`[AlertId <String>]`: ID</span><span class="sxs-lookup"><span data-stu-id="da3ad-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="da3ad-137">`[ExportName <String>]`: Exportera namn.</span><span class="sxs-lookup"><span data-stu-id="da3ad-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="da3ad-138">`[ExternalCloudProviderId <String>]`: Det kan vara ' {externalSubscriptionId} ' för det länkade kontot eller ' {externalBillingAccountId} ' för det konsoliderade kontot som används med dimension/frågor.</span><span class="sxs-lookup"><span data-stu-id="da3ad-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="da3ad-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typen av extern moln leverantör som är associerad med dimension/frågor.</span><span class="sxs-lookup"><span data-stu-id="da3ad-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="da3ad-140">Detta inkluderar ' externalSubscriptions ' för det länkade kontot och ' externalBillingAccounts ' för konsoliderat konto.</span><span class="sxs-lookup"><span data-stu-id="da3ad-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="da3ad-141">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="da3ad-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="da3ad-142">`[Scope <String>]`: Omfattningen som är associerad med vyn View.</span><span class="sxs-lookup"><span data-stu-id="da3ad-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="da3ad-143">Här ingår "prenumerationer/{subscriptionId}" för abonnemangs omfattningen, "prenumerationer/{subscriptionId}/resourceGroups/{resourceGroupName}" för resourceGroup omfattning "leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId} ' för fakturerings konto omfattning," leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/avdelningar/{departmentId} "för avdelningens omfattning," leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} "för EnrollmentAccount omfattning" providers/Microsoft. fakturering/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' for BillingProfile scope "providers/Microsoft. fakturering/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' för InvoiceSection omfattning" providers/Microsoft. Management/managementGroups/{managementGroupId} "for Management Group scope," providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName} "för externa scope för fakturerings konto och" leverantörer/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName} "för extern abonnemangs omfattning.</span><span class="sxs-lookup"><span data-stu-id="da3ad-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="da3ad-144">`[ViewName <String>]`: Vynamn</span><span class="sxs-lookup"><span data-stu-id="da3ad-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="da3ad-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da3ad-145">RELATED LINKS</span></span>

