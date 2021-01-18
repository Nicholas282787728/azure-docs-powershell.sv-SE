---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementexecuteexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
ms.openlocfilehash: 752af43a72151296c4c90ecc32923a786c7b4081
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526375"
---
# <span data-ttu-id="5de22-101">Invoke-AzCostManagementExecuteExport</span><span class="sxs-lookup"><span data-stu-id="5de22-101">Invoke-AzCostManagementExecuteExport</span></span>

## <span data-ttu-id="5de22-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5de22-102">SYNOPSIS</span></span>
<span data-ttu-id="5de22-103">Operationen för att utföra en export.</span><span class="sxs-lookup"><span data-stu-id="5de22-103">The operation to execute an export.</span></span>

## <span data-ttu-id="5de22-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5de22-104">SYNTAX</span></span>

### <span data-ttu-id="5de22-105">Kör (standard)</span><span class="sxs-lookup"><span data-stu-id="5de22-105">Execute (Default)</span></span>
```
Invoke-AzCostManagementExecuteExport -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5de22-106">ExecuteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5de22-106">ExecuteViaIdentity</span></span>
```
Invoke-AzCostManagementExecuteExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5de22-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5de22-107">DESCRIPTION</span></span>
<span data-ttu-id="5de22-108">Operationen för att utföra en export.</span><span class="sxs-lookup"><span data-stu-id="5de22-108">The operation to execute an export.</span></span>

## <span data-ttu-id="5de22-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5de22-109">EXAMPLES</span></span>

### <span data-ttu-id="5de22-110">Exempel 1: Invoke export by ExportName och scope</span><span class="sxs-lookup"><span data-stu-id="5de22-110">Example 1: Invoke Export by ExportName and Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementExecuteExport -ExportName 'TestExport' -Scope 'subscriptions/**********'

```

<span data-ttu-id="5de22-111">Starta export via ExportName och omfattning</span><span class="sxs-lookup"><span data-stu-id="5de22-111">Invoke Export by ExportName and Scope</span></span>

### <span data-ttu-id="5de22-112">Exempel 2: starta export av InputObject</span><span class="sxs-lookup"><span data-stu-id="5de22-112">Example 2: Invoke Export by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Invoke-AzCostManagementExecuteExport -InputObject $getExport

```

<span data-ttu-id="5de22-113">Starta export via InputObject</span><span class="sxs-lookup"><span data-stu-id="5de22-113">Invoke Export by InputObject</span></span>

## <span data-ttu-id="5de22-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5de22-114">PARAMETERS</span></span>

### <span data-ttu-id="5de22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5de22-115">-DefaultProfile</span></span>
<span data-ttu-id="5de22-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5de22-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5de22-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="5de22-117">-ExportName</span></span>
<span data-ttu-id="5de22-118">Exportera namn.</span><span class="sxs-lookup"><span data-stu-id="5de22-118">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5de22-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5de22-119">-InputObject</span></span>
<span data-ttu-id="5de22-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5de22-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: ExecuteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5de22-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5de22-121">-PassThru</span></span>
<span data-ttu-id="5de22-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="5de22-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5de22-123">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="5de22-123">-Scope</span></span>
<span data-ttu-id="5de22-124">Den här parametern definierar omfattningen av costmanagement från olika perspektiv, "ResourceGroup" och "tillhandahåller tjänst".</span><span class="sxs-lookup"><span data-stu-id="5de22-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5de22-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5de22-125">-Confirm</span></span>
<span data-ttu-id="5de22-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5de22-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5de22-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5de22-127">-WhatIf</span></span>
<span data-ttu-id="5de22-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5de22-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5de22-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5de22-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5de22-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de22-130">CommonParameters</span></span>
<span data-ttu-id="5de22-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5de22-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de22-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5de22-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de22-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5de22-133">INPUTS</span></span>

### <span data-ttu-id="5de22-134">Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="5de22-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="5de22-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5de22-135">OUTPUTS</span></span>

### <span data-ttu-id="5de22-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5de22-136">System.Boolean</span></span>

## <span data-ttu-id="5de22-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5de22-137">NOTES</span></span>

<span data-ttu-id="5de22-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5de22-138">ALIASES</span></span>

<span data-ttu-id="5de22-139">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="5de22-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5de22-140">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="5de22-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5de22-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5de22-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5de22-142">INPUTOBJECT <ICostManagementIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5de22-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5de22-143">`[AlertId <String>]`: ID</span><span class="sxs-lookup"><span data-stu-id="5de22-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="5de22-144">`[ExportName <String>]`: Exportera namn.</span><span class="sxs-lookup"><span data-stu-id="5de22-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="5de22-145">`[ExternalCloudProviderId <String>]`: Det kan vara ' {externalSubscriptionId} ' för det länkade kontot eller ' {externalBillingAccountId} ' för det konsoliderade kontot som används med dimension/frågor.</span><span class="sxs-lookup"><span data-stu-id="5de22-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="5de22-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typen av extern moln leverantör som är associerad med dimension/frågor.</span><span class="sxs-lookup"><span data-stu-id="5de22-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="5de22-147">Detta inkluderar ' externalSubscriptions ' för det länkade kontot och ' externalBillingAccounts ' för konsoliderat konto.</span><span class="sxs-lookup"><span data-stu-id="5de22-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="5de22-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5de22-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5de22-149">`[Scope <String>]`: Omfattningen som är associerad med vyn View.</span><span class="sxs-lookup"><span data-stu-id="5de22-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="5de22-150">Här ingår "prenumerationer/{subscriptionId}" för abonnemangs omfattningen, "prenumerationer/{subscriptionId}/resourceGroups/{resourceGroupName}" för resourceGroup omfattning "leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId} ' för fakturerings konto omfattning," leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/avdelningar/{departmentId} "för avdelningens omfattning," leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} "för EnrollmentAccount omfattning" providers/Microsoft. fakturering/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' for BillingProfile scope "providers/Microsoft. fakturering/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' för InvoiceSection omfattning" providers/Microsoft. Management/managementGroups/{managementGroupId} "for Management Group scope," providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName} "för externa scope för fakturerings konto och" leverantörer/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName} "för extern abonnemangs omfattning.</span><span class="sxs-lookup"><span data-stu-id="5de22-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="5de22-151">`[ViewName <String>]`: Vynamn</span><span class="sxs-lookup"><span data-stu-id="5de22-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="5de22-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5de22-152">RELATED LINKS</span></span>

