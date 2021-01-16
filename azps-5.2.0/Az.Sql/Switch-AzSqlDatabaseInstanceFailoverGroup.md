---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 9f82c8a50cba86fed394d55692d03eeec2ef97ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402856"
---
# <span data-ttu-id="729e3-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="729e3-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="729e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="729e3-102">SYNOPSIS</span></span>
<span data-ttu-id="729e3-103">Kör en redundans för en instans av en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="729e3-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="729e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="729e3-104">SYNTAX</span></span>

### <span data-ttu-id="729e3-105">SwitchInstanceFailoverGroupDefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="729e3-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="729e3-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="729e3-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="729e3-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="729e3-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="729e3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="729e3-108">DESCRIPTION</span></span>
<span data-ttu-id="729e3-109">Det här kommandot byter plats på de hanterade instansernas roller i en failover-grupp för redundans genom att gå över till det angivna sekundära området, vilket gör den till det nya primära området.</span><span class="sxs-lookup"><span data-stu-id="729e3-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="729e3-110">Alla nya TDS-sessioner som ansluter till den primära slut punkten omdirigeras automatiskt till det nya primära området.</span><span class="sxs-lookup"><span data-stu-id="729e3-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="729e3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="729e3-111">EXAMPLES</span></span>

### <span data-ttu-id="729e3-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="729e3-112">Example 1</span></span>
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

<span data-ttu-id="729e3-113">Problem med en redundansväxling som möjliggör förlust av data i en instans av failover-gruppen.</span><span class="sxs-lookup"><span data-stu-id="729e3-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="729e3-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="729e3-114">Example 2</span></span>
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

<span data-ttu-id="729e3-115">Få en failover-åtgärd som fungerar bäst utan att förlora data eller Miss lyckas och återställa.</span><span class="sxs-lookup"><span data-stu-id="729e3-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="729e3-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="729e3-116">PARAMETERS</span></span>

### <span data-ttu-id="729e3-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="729e3-117">-AllowDataLoss</span></span>
<span data-ttu-id="729e3-118">Slutför redundans trots att det kan leda till data förlust.</span><span class="sxs-lookup"><span data-stu-id="729e3-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="729e3-119">Detta gör att redundansväxlingen kan fortsätta även om en primär databas inte är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="729e3-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="729e3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="729e3-120">-DefaultProfile</span></span>
<span data-ttu-id="729e3-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="729e3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729e3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="729e3-122">-InputObject</span></span>
<span data-ttu-id="729e3-123">Grupp objekt för förekomst av redundans för att växla</span><span class="sxs-lookup"><span data-stu-id="729e3-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SwitchInstanceFailoverGroupByInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="729e3-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="729e3-124">-Location</span></span>
<span data-ttu-id="729e3-125">Namnet på det lokala området som du vill hämta instans failover-gruppen från.</span><span class="sxs-lookup"><span data-stu-id="729e3-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet, SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729e3-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="729e3-126">-Name</span></span>
<span data-ttu-id="729e3-127">Namnet på den failover-gruppen för instansen.</span><span class="sxs-lookup"><span data-stu-id="729e3-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729e3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="729e3-128">-ResourceGroupName</span></span>
<span data-ttu-id="729e3-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="729e3-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729e3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="729e3-130">-ResourceId</span></span>
<span data-ttu-id="729e3-131">Resurs-ID för instansens failover-grupp att växla.</span><span class="sxs-lookup"><span data-stu-id="729e3-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="729e3-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="729e3-132">-Confirm</span></span>
<span data-ttu-id="729e3-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="729e3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="729e3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="729e3-134">-WhatIf</span></span>
<span data-ttu-id="729e3-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="729e3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="729e3-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="729e3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="729e3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="729e3-137">CommonParameters</span></span>
<span data-ttu-id="729e3-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="729e3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="729e3-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="729e3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="729e3-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="729e3-140">INPUTS</span></span>

### <span data-ttu-id="729e3-141">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="729e3-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="729e3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="729e3-142">System.String</span></span>

## <span data-ttu-id="729e3-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="729e3-143">OUTPUTS</span></span>

### <span data-ttu-id="729e3-144">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="729e3-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="729e3-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="729e3-145">NOTES</span></span>

## <span data-ttu-id="729e3-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="729e3-146">RELATED LINKS</span></span>
