---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: 269a58e57510f6b0945218645ec079b21b606e44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526379"
---
# <span data-ttu-id="9b886-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="9b886-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="9b886-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b886-102">SYNOPSIS</span></span>
<span data-ttu-id="9b886-103">Åtgärden för att hämta exporten för det definierade omfånget efter export namn.</span><span class="sxs-lookup"><span data-stu-id="9b886-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="9b886-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b886-104">SYNTAX</span></span>

### <span data-ttu-id="9b886-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="9b886-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b886-106">Lära</span><span class="sxs-lookup"><span data-stu-id="9b886-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b886-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9b886-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9b886-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b886-108">DESCRIPTION</span></span>
<span data-ttu-id="9b886-109">Åtgärden för att hämta exporten för det definierade omfånget efter export namn.</span><span class="sxs-lookup"><span data-stu-id="9b886-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="9b886-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b886-110">EXAMPLES</span></span>

### <span data-ttu-id="9b886-111">Exempel 1: Hämta alla AzCostManagementExports efter omfattning</span><span class="sxs-lookup"><span data-stu-id="9b886-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="9b886-112">Hämta alla AzCostManagementExports efter omfattning</span><span class="sxs-lookup"><span data-stu-id="9b886-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="9b886-113">Exempel 2: get AzCostManagementExport efter namn och omfattning</span><span class="sxs-lookup"><span data-stu-id="9b886-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="9b886-114">Få AzCostManagementExport via namn och omfattning</span><span class="sxs-lookup"><span data-stu-id="9b886-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="9b886-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b886-115">PARAMETERS</span></span>

### <span data-ttu-id="9b886-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b886-116">-DefaultProfile</span></span>
<span data-ttu-id="9b886-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b886-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b886-118">-Expandera</span><span class="sxs-lookup"><span data-stu-id="9b886-118">-Expand</span></span>
<span data-ttu-id="9b886-119">Kan användas för att visa egenskaperna i en export.</span><span class="sxs-lookup"><span data-stu-id="9b886-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="9b886-120">För närvarande är bara ' runHistory ' stöd för och returnerar information för de senaste 10 körningarna av exporten.</span><span class="sxs-lookup"><span data-stu-id="9b886-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b886-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b886-121">-InputObject</span></span>
<span data-ttu-id="9b886-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9b886-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9b886-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b886-123">-Name</span></span>
<span data-ttu-id="9b886-124">Exportera namn.</span><span class="sxs-lookup"><span data-stu-id="9b886-124">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b886-125">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="9b886-125">-Scope</span></span>
<span data-ttu-id="9b886-126">Den här parametern definierar omfattningen av costmanagement från olika perspektiv, "ResourceGroup" och "tillhandahåller tjänst".</span><span class="sxs-lookup"><span data-stu-id="9b886-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b886-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b886-127">CommonParameters</span></span>
<span data-ttu-id="9b886-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b886-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b886-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b886-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b886-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b886-130">INPUTS</span></span>

### <span data-ttu-id="9b886-131">Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="9b886-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="9b886-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b886-132">OUTPUTS</span></span>

### <span data-ttu-id="9b886-133">Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. Api20200601. IExport</span><span class="sxs-lookup"><span data-stu-id="9b886-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="9b886-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b886-134">NOTES</span></span>

<span data-ttu-id="9b886-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9b886-135">ALIASES</span></span>

<span data-ttu-id="9b886-136">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="9b886-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9b886-137">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="9b886-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9b886-138">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9b886-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9b886-139">INPUTOBJECT <ICostManagementIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="9b886-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9b886-140">`[AlertId <String>]`: ID</span><span class="sxs-lookup"><span data-stu-id="9b886-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="9b886-141">`[ExportName <String>]`: Exportera namn.</span><span class="sxs-lookup"><span data-stu-id="9b886-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="9b886-142">`[ExternalCloudProviderId <String>]`: Det kan vara ' {externalSubscriptionId} ' för det länkade kontot eller ' {externalBillingAccountId} ' för det konsoliderade kontot som används med dimension/frågor.</span><span class="sxs-lookup"><span data-stu-id="9b886-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="9b886-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typen av extern moln leverantör som är associerad med dimension/frågor.</span><span class="sxs-lookup"><span data-stu-id="9b886-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="9b886-144">Detta inkluderar ' externalSubscriptions ' för det länkade kontot och ' externalBillingAccounts ' för konsoliderat konto.</span><span class="sxs-lookup"><span data-stu-id="9b886-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="9b886-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="9b886-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9b886-146">`[Scope <String>]`: Omfattningen som är associerad med vyn View.</span><span class="sxs-lookup"><span data-stu-id="9b886-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="9b886-147">Här ingår "prenumerationer/{subscriptionId}" för abonnemangs omfattningen, "prenumerationer/{subscriptionId}/resourceGroups/{resourceGroupName}" för resourceGroup omfattning "leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId} ' för fakturerings konto omfattning," leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/avdelningar/{departmentId} "för avdelningens omfattning," leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} "för EnrollmentAccount omfattning" providers/Microsoft. fakturering/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' for BillingProfile scope "providers/Microsoft. fakturering/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' för InvoiceSection omfattning" providers/Microsoft. Management/managementGroups/{managementGroupId} "for Management Group scope," providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName} "för externa scope för fakturerings konto och" leverantörer/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName} "för extern abonnemangs omfattning.</span><span class="sxs-lookup"><span data-stu-id="9b886-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="9b886-148">`[ViewName <String>]`: Vynamn</span><span class="sxs-lookup"><span data-stu-id="9b886-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="9b886-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b886-149">RELATED LINKS</span></span>

