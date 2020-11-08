---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: f617f853a8e9106ecb2d1268dfbe4e46a22efb45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271726"
---
# <span data-ttu-id="1fa69-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1fa69-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="1fa69-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1fa69-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa69-103">Skapar eller uppdaterar en befintlig virtuell nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="1fa69-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="1fa69-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1fa69-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1fa69-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1fa69-105">DESCRIPTION</span></span>
<span data-ttu-id="1fa69-106">Skapar eller uppdaterar en befintlig virtuell nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="1fa69-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="1fa69-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1fa69-107">EXAMPLES</span></span>

### <span data-ttu-id="1fa69-108">Exempel 1: skapa en ny regel för PostgreSql-Server</span><span class="sxs-lookup"><span data-stu-id="1fa69-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="1fa69-109">Dessa cmdletar skapar en PostgreSql för en server.</span><span class="sxs-lookup"><span data-stu-id="1fa69-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="1fa69-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1fa69-110">PARAMETERS</span></span>

### <span data-ttu-id="1fa69-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fa69-111">-AsJob</span></span>
<span data-ttu-id="1fa69-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="1fa69-112">Run the command as a job</span></span>

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

### <span data-ttu-id="1fa69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fa69-113">-DefaultProfile</span></span>
<span data-ttu-id="1fa69-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1fa69-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fa69-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1fa69-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="1fa69-116">Skapa brand Väggs regel innan slut punkts tjänst för virtuellt nätverk har Aktiver ATS för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1fa69-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="1fa69-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="1fa69-117">-Name</span></span>
<span data-ttu-id="1fa69-118">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="1fa69-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="1fa69-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1fa69-119">-NoWait</span></span>
<span data-ttu-id="1fa69-120">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="1fa69-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1fa69-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fa69-121">-PassThru</span></span>
<span data-ttu-id="1fa69-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="1fa69-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1fa69-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fa69-123">-ResourceGroupName</span></span>
<span data-ttu-id="1fa69-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1fa69-124">The name of the resource group.</span></span>
<span data-ttu-id="1fa69-125">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="1fa69-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1fa69-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1fa69-126">-ServerName</span></span>
<span data-ttu-id="1fa69-127">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="1fa69-127">The name of the server.</span></span>

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

### <span data-ttu-id="1fa69-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1fa69-128">-SubnetId</span></span>
<span data-ttu-id="1fa69-129">ARM-resurs-ID för det virtuella nätverkets undernät.</span><span class="sxs-lookup"><span data-stu-id="1fa69-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="1fa69-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1fa69-130">-SubscriptionId</span></span>
<span data-ttu-id="1fa69-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1fa69-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1fa69-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1fa69-132">-Confirm</span></span>
<span data-ttu-id="1fa69-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1fa69-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fa69-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fa69-134">-WhatIf</span></span>
<span data-ttu-id="1fa69-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1fa69-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fa69-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1fa69-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fa69-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa69-137">CommonParameters</span></span>
<span data-ttu-id="1fa69-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fa69-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa69-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fa69-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa69-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1fa69-140">INPUTS</span></span>

## <span data-ttu-id="1fa69-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1fa69-141">OUTPUTS</span></span>

### <span data-ttu-id="1fa69-142">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1fa69-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="1fa69-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1fa69-143">NOTES</span></span>

<span data-ttu-id="1fa69-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1fa69-144">ALIASES</span></span>

## <span data-ttu-id="1fa69-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1fa69-145">RELATED LINKS</span></span>

