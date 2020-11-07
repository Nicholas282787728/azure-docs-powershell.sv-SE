---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 7d52c80bba03d0e88d6e5302647fd9e6de94675f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920727"
---
# <span data-ttu-id="751cf-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="751cf-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="751cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="751cf-102">SYNOPSIS</span></span>
<span data-ttu-id="751cf-103">Kör en redundans för en instans av en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="751cf-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="751cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="751cf-104">SYNTAX</span></span>

### <span data-ttu-id="751cf-105">SwitchIFGDefault (standard)</span><span class="sxs-lookup"><span data-stu-id="751cf-105">SwitchIFGDefault (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="751cf-106">Växla en failover-grupp från resurs-ID</span><span class="sxs-lookup"><span data-stu-id="751cf-106">Switch a Instance Failover Group from Resource Id</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="751cf-107">Växla en failover-grupp för en instans från AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="751cf-107">Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="751cf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="751cf-108">DESCRIPTION</span></span>
<span data-ttu-id="751cf-109">Det här kommandot byter plats på de hanterade instansernas roller i en failover-grupp för redundans genom att gå över till det angivna sekundära området, vilket gör den till det nya primära området.</span><span class="sxs-lookup"><span data-stu-id="751cf-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="751cf-110">Alla nya TDS-sessioner som ansluter till den primära slut punkten omdirigeras automatiskt till det nya primära området.</span><span class="sxs-lookup"><span data-stu-id="751cf-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="751cf-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="751cf-111">EXAMPLES</span></span>

### <span data-ttu-id="751cf-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="751cf-112">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup -AllowDataLoss
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="751cf-113">Problem med en redundansväxling som möjliggör förlust av data i en instans av failover-gruppen.</span><span class="sxs-lookup"><span data-stu-id="751cf-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="751cf-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="751cf-114">Example 2</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="751cf-115">Få en failover-åtgärd som fungerar bäst utan att förlora data eller Miss lyckas och återställa.</span><span class="sxs-lookup"><span data-stu-id="751cf-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="751cf-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="751cf-116">PARAMETERS</span></span>

### <span data-ttu-id="751cf-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="751cf-117">-AllowDataLoss</span></span>
<span data-ttu-id="751cf-118">Slutför redundans trots att det kan leda till data förlust.</span><span class="sxs-lookup"><span data-stu-id="751cf-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="751cf-119">Detta gör att redundansväxlingen kan fortsätta även om en primär databas inte är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="751cf-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="751cf-120">-DefaultProfile</span></span>
<span data-ttu-id="751cf-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="751cf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751cf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="751cf-122">-InputObject</span></span>
<span data-ttu-id="751cf-123">Grupp objekt för förekomst av redundans för att växla</span><span class="sxs-lookup"><span data-stu-id="751cf-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="751cf-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="751cf-124">-Location</span></span>
<span data-ttu-id="751cf-125">Namnet på det lokala området som du vill hämta instans failover-gruppen från.</span><span class="sxs-lookup"><span data-stu-id="751cf-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault, Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751cf-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="751cf-126">-Name</span></span>
<span data-ttu-id="751cf-127">Namnet på den failover-gruppen för instansen.</span><span class="sxs-lookup"><span data-stu-id="751cf-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751cf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="751cf-128">-ResourceGroupName</span></span>
<span data-ttu-id="751cf-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="751cf-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751cf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="751cf-130">-ResourceId</span></span>
<span data-ttu-id="751cf-131">Resurs-ID för instansens failover-grupp att växla.</span><span class="sxs-lookup"><span data-stu-id="751cf-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: String
Parameter Sets: Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="751cf-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="751cf-132">-Confirm</span></span>
<span data-ttu-id="751cf-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="751cf-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751cf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="751cf-134">-WhatIf</span></span>
<span data-ttu-id="751cf-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="751cf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="751cf-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="751cf-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="751cf-137">CommonParameters</span></span>
<span data-ttu-id="751cf-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="751cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="751cf-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="751cf-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="751cf-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="751cf-140">INPUTS</span></span>

### <span data-ttu-id="751cf-141">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="751cf-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="751cf-142">System. String</span><span class="sxs-lookup"><span data-stu-id="751cf-142">System.String</span></span>

## <span data-ttu-id="751cf-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="751cf-143">OUTPUTS</span></span>

### <span data-ttu-id="751cf-144">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="751cf-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="751cf-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="751cf-145">NOTES</span></span>

## <span data-ttu-id="751cf-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="751cf-146">RELATED LINKS</span></span>
