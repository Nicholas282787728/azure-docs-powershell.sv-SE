---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 7a893099a81225f165fc6fc56c6ba3fd6cfaec3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270214"
---
# <span data-ttu-id="4de46-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4de46-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="4de46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4de46-102">SYNOPSIS</span></span>
<span data-ttu-id="4de46-103">Det här kommandot skapar en ny failover-grupp för Azure SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="4de46-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="4de46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4de46-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4de46-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4de46-105">DESCRIPTION</span></span>
<span data-ttu-id="4de46-106">Skapar en ny failover-grupp för Azure SQL-serverinstansen mellan de angivna regionerna med det beskrivande paret.</span><span class="sxs-lookup"><span data-stu-id="4de46-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="4de46-107">Två slut punkter för Azure SQL-databasens TDS skapas på Name. SqlDatabaseDnsSuffix (till exempel Name.database.windows.net) och Name. Secondary. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="4de46-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="4de46-108">Dessa slut punkter kan användas för att ansluta till den primära och sekundära regionen i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="4de46-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="4de46-109">Om det primära området påverkas av ett avbrott utlöses automatisk redundans för slut punkterna och databaserna enligt failover-principen för redundansrelationen och Grace-perioden.</span><span class="sxs-lookup"><span data-stu-id="4de46-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="4de46-110">Vid förhands granskning av funktionen för failover-grupper kan endast värden som är större än eller lika med 1 timme användas för parametern "-GracePeriodWithDataLossHours".</span><span class="sxs-lookup"><span data-stu-id="4de46-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="4de46-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4de46-111">EXAMPLES</span></span>

### <span data-ttu-id="4de46-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4de46-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="4de46-113">Det här kommandot skapar en ny failover-grupp med redundanskonfiguration automatiskt för det hanterade instans paret.</span><span class="sxs-lookup"><span data-stu-id="4de46-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="4de46-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4de46-114">Example 2</span></span>
```powershell
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

<span data-ttu-id="4de46-115">Det här kommandot skapar en ny redundansrelation med redundanskonfiguration för det hanterade instans paret.</span><span class="sxs-lookup"><span data-stu-id="4de46-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="4de46-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="4de46-116">Example 3</span></span>

<span data-ttu-id="4de46-117">Det här kommandot skapar en ny failover-grupp för Azure SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="4de46-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="4de46-118">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="4de46-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="4de46-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4de46-119">PARAMETERS</span></span>

### <span data-ttu-id="4de46-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="4de46-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="4de46-121">Om ett avbrott på den sekundära servern ska utlösa automatisk redundans av den skrivskyddade slut punkten.</span><span class="sxs-lookup"><span data-stu-id="4de46-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="4de46-122">Den här funktionen stöds inte ännu.</span><span class="sxs-lookup"><span data-stu-id="4de46-122">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="4de46-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de46-123">-DefaultProfile</span></span>
<span data-ttu-id="4de46-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4de46-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4de46-125">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="4de46-125">-FailoverPolicy</span></span>
<span data-ttu-id="4de46-126">Redundanskonfiguration för gruppen instance failover.</span><span class="sxs-lookup"><span data-stu-id="4de46-126">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4de46-127">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="4de46-127">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="4de46-128">Intervallet innan automatisk redundans initieras om det uppstår ett avbrott på den primära servern och redundansväxlingen inte kan slutföras utan data förlust.</span><span class="sxs-lookup"><span data-stu-id="4de46-128">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="4de46-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="4de46-129">-Location</span></span>
<span data-ttu-id="4de46-130">Namnet på det lokala området som du vill hämta instans failover-gruppen från.</span><span class="sxs-lookup"><span data-stu-id="4de46-130">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4de46-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="4de46-131">-Name</span></span>
<span data-ttu-id="4de46-132">Namnet på den failover-grupp i Azure SQL-databasen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="4de46-132">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="4de46-133">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="4de46-133">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="4de46-134">Namnet på den hanterade instans i partner regionen som ska läggas till i gruppen instance failover.</span><span class="sxs-lookup"><span data-stu-id="4de46-134">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4de46-135">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="4de46-135">-PartnerRegion</span></span>
<span data-ttu-id="4de46-136">Namnet på partner regionen för instansens failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="4de46-136">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4de46-137">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de46-137">-PartnerResourceGroupName</span></span>
<span data-ttu-id="4de46-138">Namnet på den sekundära resurs gruppen för instansens failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="4de46-138">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4de46-139">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4de46-139">-PartnerSubscriptionId</span></span>
<span data-ttu-id="4de46-140">Abonnemangs-ID för den sekundära hanterade instansen av instansens failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="4de46-140">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="4de46-141">Den här parametern behövs endast för konfiguration av kors prenumeration</span><span class="sxs-lookup"><span data-stu-id="4de46-141">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="4de46-142">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="4de46-142">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="4de46-143">Namnet på den hanterade instans i det lokala området som ska läggas till i gruppen instance failover.</span><span class="sxs-lookup"><span data-stu-id="4de46-143">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4de46-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de46-144">-ResourceGroupName</span></span>
<span data-ttu-id="4de46-145">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4de46-145">The name of the resource group.</span></span>

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

### <span data-ttu-id="4de46-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4de46-146">-Confirm</span></span>
<span data-ttu-id="4de46-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4de46-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4de46-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4de46-148">-WhatIf</span></span>
<span data-ttu-id="4de46-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4de46-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4de46-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4de46-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4de46-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de46-151">CommonParameters</span></span>
<span data-ttu-id="4de46-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de46-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de46-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4de46-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de46-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4de46-154">INPUTS</span></span>

### <span data-ttu-id="4de46-155">System. String</span><span class="sxs-lookup"><span data-stu-id="4de46-155">System.String</span></span>

## <span data-ttu-id="4de46-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4de46-156">OUTPUTS</span></span>

### <span data-ttu-id="4de46-157">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4de46-157">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="4de46-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4de46-158">NOTES</span></span>

## <span data-ttu-id="4de46-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4de46-159">RELATED LINKS</span></span>
