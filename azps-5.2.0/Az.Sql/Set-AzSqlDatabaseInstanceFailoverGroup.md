---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: f8ac83b684718a6a2698fd1b304b85ffa1ae5d45
ms.sourcegitcommit: a6d92493a8d1b81b85f4db2a38f271134be5e6c5
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/12/2020
ms.locfileid: "98418760"
---
# <span data-ttu-id="8c1b1-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8c1b1-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="8c1b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c1b1-102">SYNOPSIS</span></span>
<span data-ttu-id="8c1b1-103">Ändrar konfigurationen för en instans av en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="8c1b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c1b1-104">SYNTAX</span></span>

### <span data-ttu-id="8c1b1-105">SetInstanceFailoverGroupDefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8c1b1-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c1b1-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8c1b1-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c1b1-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="8c1b1-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c1b1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c1b1-108">DESCRIPTION</span></span>
<span data-ttu-id="8c1b1-109">Det här kommandot ändrar konfigurationen för en instans av en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="8c1b1-110">Det primära området för instansens failover-grupp ska användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="8c1b1-111">Vid förhands granskning av funktionen för failover-grupper kan endast värden som är större än eller lika med 1 timme användas för parametern "-GracePeriodWithDataLossHours".</span><span class="sxs-lookup"><span data-stu-id="8c1b1-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="8c1b1-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c1b1-112">EXAMPLES</span></span>

### <span data-ttu-id="8c1b1-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8c1b1-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Manual
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
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="8c1b1-114">Ställer in en auktoriseringsprincip för en failover-redundansrelation till "Manual" i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="8c1b1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c1b1-115">PARAMETERS</span></span>

### <span data-ttu-id="8c1b1-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="8c1b1-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="8c1b1-117">Om avbrott på den sekundära servern ska utlösa automatisk redundans av den skrivskyddade slut punkten.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="8c1b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c1b1-118">-DefaultProfile</span></span>
<span data-ttu-id="8c1b1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c1b1-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="8c1b1-120">-FailoverPolicy</span></span>
<span data-ttu-id="8c1b1-121">Redundanskonfiguration för gruppen instance failover.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-121">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8c1b1-122">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="8c1b1-122">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="8c1b1-123">Intervallet innan automatisk redundans initieras om det uppstår ett avbrott på den primära servern och redundansväxlingen inte kan slutföras utan data förlust.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-123">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1b1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c1b1-124">-InputObject</span></span>
<span data-ttu-id="8c1b1-125">Grupp objekt för förekomst av redundans</span><span class="sxs-lookup"><span data-stu-id="8c1b1-125">The Instance Failover Group object to set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1b1-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="8c1b1-126">-Location</span></span>
<span data-ttu-id="8c1b1-127">Namnet på det lokala området som du vill hämta instans failover-gruppen från.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet, SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1b1-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="8c1b1-128">-Name</span></span>
<span data-ttu-id="8c1b1-129">Namnet på den failover-gruppen för instansen.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-129">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1b1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c1b1-130">-ResourceGroupName</span></span>
<span data-ttu-id="8c1b1-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1b1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c1b1-132">-ResourceId</span></span>
<span data-ttu-id="8c1b1-133">Resurs-ID för den instans failover-grupp som ska anges.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-133">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1b1-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8c1b1-134">-Confirm</span></span>
<span data-ttu-id="8c1b1-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c1b1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c1b1-136">-WhatIf</span></span>
<span data-ttu-id="8c1b1-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c1b1-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c1b1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c1b1-139">CommonParameters</span></span>
<span data-ttu-id="8c1b1-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c1b1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c1b1-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c1b1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c1b1-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c1b1-142">INPUTS</span></span>

### <span data-ttu-id="8c1b1-143">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8c1b1-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="8c1b1-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8c1b1-144">System.String</span></span>

## <span data-ttu-id="8c1b1-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c1b1-145">OUTPUTS</span></span>

### <span data-ttu-id="8c1b1-146">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8c1b1-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="8c1b1-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c1b1-147">NOTES</span></span>

## <span data-ttu-id="8c1b1-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c1b1-148">RELATED LINKS</span></span>
