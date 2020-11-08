---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: 95a9e996612827b355b141165231651e17c78f6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262243"
---
# <span data-ttu-id="cedb8-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="cedb8-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="cedb8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cedb8-102">SYNOPSIS</span></span>
<span data-ttu-id="cedb8-103">Skapar en SAP-Monitor för angiven prenumeration, resurs grupp och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="cedb8-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="cedb8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cedb8-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cedb8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cedb8-105">DESCRIPTION</span></span>
<span data-ttu-id="cedb8-106">Skapar en SAP-Monitor för angiven prenumeration, resurs grupp och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="cedb8-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="cedb8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cedb8-107">EXAMPLES</span></span>

### <span data-ttu-id="cedb8-108">Exempel 1: ny SAP-bildskärm</span><span class="sxs-lookup"><span data-stu-id="cedb8-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="cedb8-109">Det här kommandot skapar en SAP-skärm.</span><span class="sxs-lookup"><span data-stu-id="cedb8-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="cedb8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cedb8-110">PARAMETERS</span></span>

### <span data-ttu-id="cedb8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cedb8-111">-AsJob</span></span>
<span data-ttu-id="cedb8-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="cedb8-112">Run the command as a job</span></span>

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

### <span data-ttu-id="cedb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cedb8-113">-DefaultProfile</span></span>
<span data-ttu-id="cedb8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cedb8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cedb8-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="cedb8-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="cedb8-116">Värdet som anger om analys ska skickas till Microsoft</span><span class="sxs-lookup"><span data-stu-id="cedb8-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="cedb8-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="cedb8-117">-Location</span></span>
<span data-ttu-id="cedb8-118">Den Geo-plats där resursen bor</span><span class="sxs-lookup"><span data-stu-id="cedb8-118">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cedb8-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="cedb8-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="cedb8-120">Arbets ytans ID för den logganalys-arbetsyta som ska användas för övervakning</span><span class="sxs-lookup"><span data-stu-id="cedb8-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

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

### <span data-ttu-id="cedb8-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="cedb8-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="cedb8-122">ARM-ID för den logganalys-arbetsyta som används för övervakning</span><span class="sxs-lookup"><span data-stu-id="cedb8-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="cedb8-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="cedb8-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="cedb8-124">Den delade knappen i den logganalys-arbetsyta som används för övervakning</span><span class="sxs-lookup"><span data-stu-id="cedb8-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="cedb8-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="cedb8-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="cedb8-126">Det undernät som SAP-övervakaren ska distribueras till.</span><span class="sxs-lookup"><span data-stu-id="cedb8-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="cedb8-127">Det ska vara samma undernät i HANA-databasen.</span><span class="sxs-lookup"><span data-stu-id="cedb8-127">It should be the same subnet of HANA database.</span></span>

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

### <span data-ttu-id="cedb8-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="cedb8-128">-Name</span></span>
<span data-ttu-id="cedb8-129">Namnet på SAP Monitor-resursen.</span><span class="sxs-lookup"><span data-stu-id="cedb8-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cedb8-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cedb8-130">-NoWait</span></span>
<span data-ttu-id="cedb8-131">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="cedb8-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cedb8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cedb8-132">-ResourceGroupName</span></span>
<span data-ttu-id="cedb8-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cedb8-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cedb8-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cedb8-134">-SubscriptionId</span></span>
<span data-ttu-id="cedb8-135">Abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cedb8-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cedb8-136">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="cedb8-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cedb8-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cedb8-137">-Tag</span></span>
<span data-ttu-id="cedb8-138">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="cedb8-138">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cedb8-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cedb8-139">-Confirm</span></span>
<span data-ttu-id="cedb8-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cedb8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cedb8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cedb8-141">-WhatIf</span></span>
<span data-ttu-id="cedb8-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cedb8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cedb8-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cedb8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cedb8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cedb8-144">CommonParameters</span></span>
<span data-ttu-id="cedb8-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cedb8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cedb8-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cedb8-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cedb8-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cedb8-147">INPUTS</span></span>

## <span data-ttu-id="cedb8-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cedb8-148">OUTPUTS</span></span>

### <span data-ttu-id="cedb8-149">Microsoft. Azure. PowerShell. cmdletar. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="cedb8-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="cedb8-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cedb8-150">NOTES</span></span>

<span data-ttu-id="cedb8-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cedb8-151">ALIASES</span></span>

## <span data-ttu-id="cedb8-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cedb8-152">RELATED LINKS</span></span>

