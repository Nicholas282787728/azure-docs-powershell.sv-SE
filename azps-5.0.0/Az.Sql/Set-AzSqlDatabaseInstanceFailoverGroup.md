---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 79d7482d51ffc7c03703dbf62e00fd9230f9976d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273010"
---
# <span data-ttu-id="81cc5-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="81cc5-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="81cc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="81cc5-103">Ändrar konfigurationen för en instans av en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="81cc5-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="81cc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81cc5-104">SYNTAX</span></span>

### <span data-ttu-id="81cc5-105">SetInstanceFailoverGroupDefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="81cc5-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81cc5-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="81cc5-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81cc5-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="81cc5-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81cc5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81cc5-108">DESCRIPTION</span></span>
<span data-ttu-id="81cc5-109">Det här kommandot ändrar konfigurationen för en instans av en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="81cc5-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="81cc5-110">Det primära området för instansens failover-grupp ska användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="81cc5-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="81cc5-111">Vid förhands granskning av funktionen för failover-grupper kan endast värden som är större än eller lika med 1 timme användas för parametern "-GracePeriodWithDataLossHours".</span><span class="sxs-lookup"><span data-stu-id="81cc5-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="81cc5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81cc5-112">EXAMPLES</span></span>

### <span data-ttu-id="81cc5-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="81cc5-113">Example 1</span></span>
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

<span data-ttu-id="81cc5-114">Ställer in en auktoriseringsprincip för en failover-redundansrelation till "Manual" i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="81cc5-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="81cc5-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81cc5-115">PARAMETERS</span></span>

### <span data-ttu-id="81cc5-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="81cc5-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="81cc5-117">Om avbrott på den sekundära servern ska utlösa automatisk redundans av den skrivskyddade slut punkten.</span><span class="sxs-lookup"><span data-stu-id="81cc5-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="81cc5-118">Den här funktionen stöds inte ännu.</span><span class="sxs-lookup"><span data-stu-id="81cc5-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="81cc5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81cc5-119">-DefaultProfile</span></span>
<span data-ttu-id="81cc5-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="81cc5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81cc5-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="81cc5-121">-FailoverPolicy</span></span>
<span data-ttu-id="81cc5-122">Redundanskonfiguration för gruppen instance failover.</span><span class="sxs-lookup"><span data-stu-id="81cc5-122">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="81cc5-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="81cc5-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="81cc5-124">Intervallet innan automatisk redundans initieras om det uppstår ett avbrott på den primära servern och redundansväxlingen inte kan slutföras utan data förlust.</span><span class="sxs-lookup"><span data-stu-id="81cc5-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="81cc5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81cc5-125">-InputObject</span></span>
<span data-ttu-id="81cc5-126">Grupp objekt för förekomst av redundans</span><span class="sxs-lookup"><span data-stu-id="81cc5-126">The Instance Failover Group object to set</span></span>

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

### <span data-ttu-id="81cc5-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="81cc5-127">-Location</span></span>
<span data-ttu-id="81cc5-128">Namnet på det lokala området som du vill hämta instans failover-gruppen från.</span><span class="sxs-lookup"><span data-stu-id="81cc5-128">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="81cc5-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="81cc5-129">-Name</span></span>
<span data-ttu-id="81cc5-130">Namnet på den failover-gruppen för instansen.</span><span class="sxs-lookup"><span data-stu-id="81cc5-130">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="81cc5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81cc5-131">-ResourceGroupName</span></span>
<span data-ttu-id="81cc5-132">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="81cc5-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="81cc5-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81cc5-133">-ResourceId</span></span>
<span data-ttu-id="81cc5-134">Resurs-ID för den instans failover-grupp som ska anges.</span><span class="sxs-lookup"><span data-stu-id="81cc5-134">The Resource ID of the Instance Failover Group to set.</span></span>

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

### <span data-ttu-id="81cc5-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="81cc5-135">-Confirm</span></span>
<span data-ttu-id="81cc5-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="81cc5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81cc5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81cc5-137">-WhatIf</span></span>
<span data-ttu-id="81cc5-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="81cc5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81cc5-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="81cc5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81cc5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81cc5-140">CommonParameters</span></span>
<span data-ttu-id="81cc5-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81cc5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81cc5-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81cc5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81cc5-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81cc5-143">INPUTS</span></span>

### <span data-ttu-id="81cc5-144">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="81cc5-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="81cc5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="81cc5-145">System.String</span></span>

## <span data-ttu-id="81cc5-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81cc5-146">OUTPUTS</span></span>

### <span data-ttu-id="81cc5-147">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="81cc5-147">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="81cc5-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81cc5-148">NOTES</span></span>

## <span data-ttu-id="81cc5-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81cc5-149">RELATED LINKS</span></span>
