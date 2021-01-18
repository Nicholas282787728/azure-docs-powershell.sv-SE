---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 3b660f5db14e1197c1e262a10f8225e4e9a82b81
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527744"
---
# <span data-ttu-id="c31f8-101">New-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c31f8-101">New-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="c31f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c31f8-102">SYNOPSIS</span></span>
<span data-ttu-id="c31f8-103">Skapar eller uppdaterar en befintlig virtuell nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="c31f8-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="c31f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c31f8-104">SYNTAX</span></span>

```
New-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c31f8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c31f8-105">DESCRIPTION</span></span>
<span data-ttu-id="c31f8-106">Skapar eller uppdaterar en befintlig virtuell nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="c31f8-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="c31f8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c31f8-107">EXAMPLES</span></span>

### <span data-ttu-id="c31f8-108">Exempel 1: skapa en ny regel för en virtuell nätverks server för MySql</span><span class="sxs-lookup"><span data-stu-id="c31f8-108">Example 1: Create a new MySql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> New-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="c31f8-109">Dessa cmdletar skapar en regel för ett virtuellt nätverk med MySql Server.</span><span class="sxs-lookup"><span data-stu-id="c31f8-109">These cmdlets create a MySql server Virtual Network Rule.</span></span>

## <span data-ttu-id="c31f8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c31f8-110">PARAMETERS</span></span>

### <span data-ttu-id="c31f8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c31f8-111">-AsJob</span></span>
<span data-ttu-id="c31f8-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="c31f8-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c31f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c31f8-113">-DefaultProfile</span></span>
<span data-ttu-id="c31f8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c31f8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c31f8-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c31f8-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="c31f8-116">Skapa brand Väggs regel innan slut punkts tjänst för virtuellt nätverk har Aktiver ATS för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c31f8-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="c31f8-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c31f8-117">-Name</span></span>
<span data-ttu-id="c31f8-118">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="c31f8-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="c31f8-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c31f8-119">-NoWait</span></span>
<span data-ttu-id="c31f8-120">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="c31f8-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c31f8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c31f8-121">-PassThru</span></span>
<span data-ttu-id="c31f8-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="c31f8-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c31f8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c31f8-123">-ResourceGroupName</span></span>
<span data-ttu-id="c31f8-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c31f8-124">The name of the resource group.</span></span>
<span data-ttu-id="c31f8-125">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="c31f8-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c31f8-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c31f8-126">-ServerName</span></span>
<span data-ttu-id="c31f8-127">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="c31f8-127">The name of the server.</span></span>

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

### <span data-ttu-id="c31f8-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c31f8-128">-SubnetId</span></span>
<span data-ttu-id="c31f8-129">ARM-resurs-ID för det virtuella nätverkets undernät.</span><span class="sxs-lookup"><span data-stu-id="c31f8-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="c31f8-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c31f8-130">-SubscriptionId</span></span>
<span data-ttu-id="c31f8-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c31f8-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c31f8-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c31f8-132">-Confirm</span></span>
<span data-ttu-id="c31f8-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c31f8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c31f8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c31f8-134">-WhatIf</span></span>
<span data-ttu-id="c31f8-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c31f8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c31f8-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c31f8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c31f8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c31f8-137">CommonParameters</span></span>
<span data-ttu-id="c31f8-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c31f8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c31f8-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c31f8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c31f8-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c31f8-140">INPUTS</span></span>

## <span data-ttu-id="c31f8-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c31f8-141">OUTPUTS</span></span>

### <span data-ttu-id="c31f8-142">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c31f8-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="c31f8-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c31f8-143">NOTES</span></span>

<span data-ttu-id="c31f8-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c31f8-144">ALIASES</span></span>

## <span data-ttu-id="c31f8-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c31f8-145">RELATED LINKS</span></span>

