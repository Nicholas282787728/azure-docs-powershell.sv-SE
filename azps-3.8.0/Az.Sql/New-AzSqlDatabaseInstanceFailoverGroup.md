---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 41032d2af506305f35197244bad3355f67185861
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090200"
---
# <span data-ttu-id="787cc-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="787cc-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="787cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="787cc-102">SYNOPSIS</span></span>
<span data-ttu-id="787cc-103">Det här kommandot skapar en ny failover-grupp för Azure SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="787cc-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="787cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="787cc-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="787cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="787cc-105">DESCRIPTION</span></span>
<span data-ttu-id="787cc-106">Skapar en ny failover-grupp för Azure SQL-serverinstansen mellan de angivna regionerna med det beskrivande paret.</span><span class="sxs-lookup"><span data-stu-id="787cc-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="787cc-107">Två slut punkter för Azure SQL-databasens TDS skapas på Name. SqlDatabaseDnsSuffix (till exempel Name.database.windows.net) och Name. Secondary. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="787cc-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="787cc-108">Dessa slut punkter kan användas för att ansluta till den primära och sekundära regionen i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="787cc-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="787cc-109">Om det primära området påverkas av ett avbrott utlöses automatisk redundans för slut punkterna och databaserna enligt failover-principen för redundansrelationen och Grace-perioden.</span><span class="sxs-lookup"><span data-stu-id="787cc-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="787cc-110">Vid förhands granskning av funktionen för failover-grupper kan endast värden som är större än eller lika med 1 timme användas för parametern "-GracePeriodWithDataLossHours".</span><span class="sxs-lookup"><span data-stu-id="787cc-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="787cc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="787cc-111">EXAMPLES</span></span>

### <span data-ttu-id="787cc-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="787cc-112">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
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

<span data-ttu-id="787cc-113">Det här kommandot skapar en ny failover-grupp med redundanskonfiguration automatiskt för det hanterade instans paret.</span><span class="sxs-lookup"><span data-stu-id="787cc-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="787cc-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="787cc-114">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Manual
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

<span data-ttu-id="787cc-115">Det här kommandot skapar en ny redundansrelation med redundanskonfiguration för det hanterade instans paret.</span><span class="sxs-lookup"><span data-stu-id="787cc-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

## <span data-ttu-id="787cc-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="787cc-116">PARAMETERS</span></span>

### <span data-ttu-id="787cc-117">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="787cc-117">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="787cc-118">Om ett avbrott på den sekundära servern ska utlösa automatisk redundans av den skrivskyddade slut punkten.</span><span class="sxs-lookup"><span data-stu-id="787cc-118">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="787cc-119">Den här funktionen stöds inte ännu.</span><span class="sxs-lookup"><span data-stu-id="787cc-119">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="787cc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787cc-120">-DefaultProfile</span></span>
<span data-ttu-id="787cc-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="787cc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="787cc-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="787cc-122">-FailoverPolicy</span></span>
<span data-ttu-id="787cc-123">Redundanskonfiguration för gruppen instance failover.</span><span class="sxs-lookup"><span data-stu-id="787cc-123">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="787cc-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="787cc-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="787cc-125">Intervallet innan automatisk redundans initieras om det uppstår ett avbrott på den primära servern och redundansväxlingen inte kan slutföras utan data förlust.</span><span class="sxs-lookup"><span data-stu-id="787cc-125">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="787cc-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="787cc-126">-Location</span></span>
<span data-ttu-id="787cc-127">Namnet på det lokala området som du vill hämta instans failover-gruppen från.</span><span class="sxs-lookup"><span data-stu-id="787cc-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="787cc-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="787cc-128">-Name</span></span>
<span data-ttu-id="787cc-129">Namnet på den failover-grupp i Azure SQL-databasen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="787cc-129">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="787cc-130">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="787cc-130">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="787cc-131">Namnet på den hanterade instans i partner regionen som ska läggas till i gruppen instance failover.</span><span class="sxs-lookup"><span data-stu-id="787cc-131">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="787cc-132">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="787cc-132">-PartnerRegion</span></span>
<span data-ttu-id="787cc-133">Namnet på partner regionen för instansens failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="787cc-133">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="787cc-134">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="787cc-134">-PartnerResourceGroupName</span></span>
<span data-ttu-id="787cc-135">Namnet på den sekundära resurs gruppen för instansens failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="787cc-135">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="787cc-136">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="787cc-136">-PartnerSubscriptionId</span></span>
<span data-ttu-id="787cc-137">Abonnemangs-ID för den sekundära hanterade instansen av instansens failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="787cc-137">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="787cc-138">Den här parametern behövs endast för konfiguration av kors prenumeration</span><span class="sxs-lookup"><span data-stu-id="787cc-138">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="787cc-139">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="787cc-139">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="787cc-140">Namnet på den hanterade instans i det lokala området som ska läggas till i gruppen instance failover.</span><span class="sxs-lookup"><span data-stu-id="787cc-140">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="787cc-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="787cc-141">-ResourceGroupName</span></span>
<span data-ttu-id="787cc-142">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="787cc-142">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="787cc-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="787cc-143">-Confirm</span></span>
<span data-ttu-id="787cc-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="787cc-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="787cc-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="787cc-145">-WhatIf</span></span>
<span data-ttu-id="787cc-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="787cc-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="787cc-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="787cc-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="787cc-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787cc-148">CommonParameters</span></span>
<span data-ttu-id="787cc-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="787cc-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787cc-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="787cc-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787cc-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="787cc-151">INPUTS</span></span>

### <span data-ttu-id="787cc-152">System. String</span><span class="sxs-lookup"><span data-stu-id="787cc-152">System.String</span></span>

## <span data-ttu-id="787cc-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="787cc-153">OUTPUTS</span></span>

### <span data-ttu-id="787cc-154">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="787cc-154">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="787cc-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="787cc-155">NOTES</span></span>

## <span data-ttu-id="787cc-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="787cc-156">RELATED LINKS</span></span>
