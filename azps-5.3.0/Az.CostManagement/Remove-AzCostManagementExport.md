---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: 75c1f01730d4dfe3e9769a430f874887fd2d2090
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524277"
---
# <span data-ttu-id="0ad5a-101">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="0ad5a-101">Remove-AzCostManagementExport</span></span>

## <span data-ttu-id="0ad5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ad5a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad5a-103">Åtgärden att ta bort en export.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-103">The operation to delete a export.</span></span>

## <span data-ttu-id="0ad5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ad5a-104">SYNTAX</span></span>

### <span data-ttu-id="0ad5a-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="0ad5a-105">Delete (Default)</span></span>
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0ad5a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0ad5a-106">DeleteViaIdentity</span></span>
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ad5a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ad5a-107">DESCRIPTION</span></span>
<span data-ttu-id="0ad5a-108">Åtgärden att ta bort en export.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-108">The operation to delete a export.</span></span>

## <span data-ttu-id="0ad5a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ad5a-109">EXAMPLES</span></span>

### <span data-ttu-id="0ad5a-110">Exempel 1: ta bort AzCostManagementExport efter omfattning och namn</span><span class="sxs-lookup"><span data-stu-id="0ad5a-110">Example 1: Delete the AzCostManagementExport by Scope and Name</span></span>
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

<span data-ttu-id="0ad5a-111">Ta bort AzCostManagementExport efter omfattning och ExportName</span><span class="sxs-lookup"><span data-stu-id="0ad5a-111">Delete the AzCostManagementExport By Scope and ExportName</span></span>

### <span data-ttu-id="0ad5a-112">Exempel 2: ta bort AzCostManagementExport efter Exportera-objekt</span><span class="sxs-lookup"><span data-stu-id="0ad5a-112">Example 2: Delete the AzCostManagementExport by Export Object</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

<span data-ttu-id="0ad5a-113">Ta bort AzCostManagementExport med InputObject</span><span class="sxs-lookup"><span data-stu-id="0ad5a-113">Delete the AzCostManagementExport By InputObject</span></span>

## <span data-ttu-id="0ad5a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ad5a-114">PARAMETERS</span></span>

### <span data-ttu-id="0ad5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad5a-115">-DefaultProfile</span></span>
<span data-ttu-id="0ad5a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ad5a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ad5a-117">-InputObject</span></span>
<span data-ttu-id="0ad5a-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad5a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ad5a-119">-Name</span></span>
<span data-ttu-id="0ad5a-120">Exportera namn.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-120">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad5a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ad5a-121">-PassThru</span></span>
<span data-ttu-id="0ad5a-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="0ad5a-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad5a-123">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="0ad5a-123">-Scope</span></span>
<span data-ttu-id="0ad5a-124">Den här parametern definierar omfattningen av costmanagement från olika perspektiv, "ResourceGroup" och "tillhandahåller tjänst".</span><span class="sxs-lookup"><span data-stu-id="0ad5a-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad5a-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0ad5a-125">-Confirm</span></span>
<span data-ttu-id="0ad5a-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad5a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ad5a-127">-WhatIf</span></span>
<span data-ttu-id="0ad5a-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ad5a-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad5a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad5a-130">CommonParameters</span></span>
<span data-ttu-id="0ad5a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad5a-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ad5a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad5a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ad5a-133">INPUTS</span></span>

### <span data-ttu-id="0ad5a-134">Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="0ad5a-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="0ad5a-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ad5a-135">OUTPUTS</span></span>

### <span data-ttu-id="0ad5a-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0ad5a-136">System.Boolean</span></span>

## <span data-ttu-id="0ad5a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ad5a-137">NOTES</span></span>

<span data-ttu-id="0ad5a-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0ad5a-138">ALIASES</span></span>

<span data-ttu-id="0ad5a-139">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0ad5a-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0ad5a-140">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ad5a-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0ad5a-142">INPUTOBJECT <ICostManagementIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="0ad5a-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0ad5a-143">`[AlertId <String>]`: ID</span><span class="sxs-lookup"><span data-stu-id="0ad5a-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="0ad5a-144">`[ExportName <String>]`: Exportera namn.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="0ad5a-145">`[ExternalCloudProviderId <String>]`: Det kan vara ' {externalSubscriptionId} ' för det länkade kontot eller ' {externalBillingAccountId} ' för det konsoliderade kontot som används med dimension/frågor.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="0ad5a-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typen av extern moln leverantör som är associerad med dimension/frågor.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="0ad5a-147">Detta inkluderar ' externalSubscriptions ' för det länkade kontot och ' externalBillingAccounts ' för konsoliderat konto.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="0ad5a-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="0ad5a-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0ad5a-149">`[Scope <String>]`: Omfattningen som är associerad med vyn View.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="0ad5a-150">Här ingår "prenumerationer/{subscriptionId}" för abonnemangs omfattningen, "prenumerationer/{subscriptionId}/resourceGroups/{resourceGroupName}" för resourceGroup omfattning "leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId} ' för fakturerings konto omfattning," leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/avdelningar/{departmentId} "för avdelningens omfattning," leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} "för EnrollmentAccount omfattning" providers/Microsoft. fakturering/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' for BillingProfile scope "providers/Microsoft. fakturering/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' för InvoiceSection omfattning" providers/Microsoft. Management/managementGroups/{managementGroupId} "for Management Group scope," providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName} "för externa scope för fakturerings konto och" leverantörer/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName} "för extern abonnemangs omfattning.</span><span class="sxs-lookup"><span data-stu-id="0ad5a-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="0ad5a-151">`[ViewName <String>]`: Vynamn</span><span class="sxs-lookup"><span data-stu-id="0ad5a-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="0ad5a-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ad5a-152">RELATED LINKS</span></span>

