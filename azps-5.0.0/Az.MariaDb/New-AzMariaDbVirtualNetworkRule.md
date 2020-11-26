---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 77a89dec96e0e9b7ca7bd003f8368274edf6acdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271874"
---
# <span data-ttu-id="fb3b1-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fb3b1-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="fb3b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3b1-103">Skapar eller uppdaterar en befintlig virtuell nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="fb3b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb3b1-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fb3b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb3b1-105">DESCRIPTION</span></span>
<span data-ttu-id="fb3b1-106">Skapar eller uppdaterar en befintlig virtuell nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="fb3b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb3b1-107">EXAMPLES</span></span>

### <span data-ttu-id="fb3b1-108">Exempel 1: skapa en virtuell nätverks regel för en MariaDB</span><span class="sxs-lookup"><span data-stu-id="fb3b1-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="fb3b1-109">Det här kommandot skapar en virtuell nätverks regel för en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="fb3b1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb3b1-110">PARAMETERS</span></span>

### <span data-ttu-id="fb3b1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb3b1-111">-AsJob</span></span>
<span data-ttu-id="fb3b1-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="fb3b1-112">Run the command as a job</span></span>

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

### <span data-ttu-id="fb3b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3b1-113">-DefaultProfile</span></span>
<span data-ttu-id="fb3b1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb3b1-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb3b1-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="fb3b1-116">Skapa brand Väggs regel innan slut punkts tjänst för virtuellt nätverk har Aktiver ATS för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="fb3b1-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb3b1-117">-Name</span></span>
<span data-ttu-id="fb3b1-118">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3b1-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="fb3b1-119">-NoWait</span></span>
<span data-ttu-id="fb3b1-120">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="fb3b1-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fb3b1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb3b1-121">-PassThru</span></span>
<span data-ttu-id="fb3b1-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="fb3b1-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fb3b1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb3b1-123">-ResourceGroupName</span></span>
<span data-ttu-id="fb3b1-124">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fb3b1-125">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fb3b1-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fb3b1-126">-ServerName</span></span>
<span data-ttu-id="fb3b1-127">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-127">The name of the server.</span></span>

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

### <span data-ttu-id="fb3b1-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="fb3b1-128">-SubnetId</span></span>
<span data-ttu-id="fb3b1-129">ARM-resurs-ID för det virtuella nätverkets undernät.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="fb3b1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb3b1-130">-SubscriptionId</span></span>
<span data-ttu-id="fb3b1-131">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="fb3b1-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb3b1-132">-Confirm</span></span>
<span data-ttu-id="fb3b1-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb3b1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb3b1-134">-WhatIf</span></span>
<span data-ttu-id="fb3b1-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb3b1-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb3b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3b1-137">CommonParameters</span></span>
<span data-ttu-id="fb3b1-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb3b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3b1-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb3b1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3b1-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb3b1-140">INPUTS</span></span>

## <span data-ttu-id="fb3b1-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb3b1-141">OUTPUTS</span></span>

### <span data-ttu-id="fb3b1-142">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fb3b1-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="fb3b1-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb3b1-143">NOTES</span></span>

<span data-ttu-id="fb3b1-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fb3b1-144">ALIASES</span></span>

## <span data-ttu-id="fb3b1-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb3b1-145">RELATED LINKS</span></span>
