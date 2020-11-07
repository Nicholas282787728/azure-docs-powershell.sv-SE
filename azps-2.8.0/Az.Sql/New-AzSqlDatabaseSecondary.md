---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 1ed31d2fedc44900d08a4108ea53220a29228a7c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920577"
---
# <span data-ttu-id="547f7-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="547f7-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="547f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="547f7-102">SYNOPSIS</span></span>
<span data-ttu-id="547f7-103">Skapar en sekundär databas för en befintlig databas och startar datareplikering.</span><span class="sxs-lookup"><span data-stu-id="547f7-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="547f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="547f7-104">SYNTAX</span></span>

### <span data-ttu-id="547f7-105">DtuBasedDatabase (standard)</span><span class="sxs-lookup"><span data-stu-id="547f7-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-LicenseType <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="547f7-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="547f7-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="547f7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="547f7-107">DESCRIPTION</span></span>
<span data-ttu-id="547f7-108">**New-AzSqlDatabaseSecondary** cmdlet ersätter Start-AzSqlDatabaseCopy cmdlet när den används för att konfigurera geo-replikering för en databas.</span><span class="sxs-lookup"><span data-stu-id="547f7-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="547f7-109">Det returnerar det geo-replikeringslänk som är länkat till den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="547f7-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="547f7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="547f7-110">EXAMPLES</span></span>

### <span data-ttu-id="547f7-111">1: etablera Active Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="547f7-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="547f7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="547f7-112">PARAMETERS</span></span>

### <span data-ttu-id="547f7-113">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="547f7-113">-AllowConnections</span></span>
<span data-ttu-id="547f7-114">Anger det alternativa Azure SQL-databasens Läs metod.</span><span class="sxs-lookup"><span data-stu-id="547f7-114">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="547f7-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="547f7-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="547f7-116">Nej</span><span class="sxs-lookup"><span data-stu-id="547f7-116">No</span></span>
- <span data-ttu-id="547f7-117">Alla</span><span class="sxs-lookup"><span data-stu-id="547f7-117">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Replication.Model.AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="547f7-118">-AsJob</span></span>
<span data-ttu-id="547f7-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="547f7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="547f7-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="547f7-120">-DatabaseName</span></span>
<span data-ttu-id="547f7-121">Anger namnet på databasen som ska fungera som primärt.</span><span class="sxs-lookup"><span data-stu-id="547f7-121">Specifies the name of the database to act as primary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="547f7-122">-DefaultProfile</span></span>
<span data-ttu-id="547f7-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="547f7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="547f7-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="547f7-124">-LicenseType</span></span>
<span data-ttu-id="547f7-125">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="547f7-125">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="547f7-126">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="547f7-126">-PartnerResourceGroupName</span></span>
<span data-ttu-id="547f7-127">Anger namnet på den Azure Resource-grupp som den här cmdleten tilldelar den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="547f7-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="547f7-128">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="547f7-128">-PartnerServerName</span></span>
<span data-ttu-id="547f7-129">Anger namnet på den databas server för Azure SQL som ska fungera som sekundär.</span><span class="sxs-lookup"><span data-stu-id="547f7-129">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="547f7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="547f7-130">-ResourceGroupName</span></span>
<span data-ttu-id="547f7-131">Anger namnet på den Azure Resource-grupp som den här cmdleten tilldelar den primära databasen.</span><span class="sxs-lookup"><span data-stu-id="547f7-131">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547f7-132">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="547f7-132">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="547f7-133">Beräkna skapandet av Azure SQL Database sekundär.</span><span class="sxs-lookup"><span data-stu-id="547f7-133">The compute generation of the Azure Sql Database secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f7-134">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="547f7-134">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="547f7-135">Anger namnet på den elastiska pool som den sekundära databasen ska placeras i.</span><span class="sxs-lookup"><span data-stu-id="547f7-135">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f7-136">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="547f7-136">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="547f7-137">Anger namnet på det tjänst mål som ska kopplas till den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="547f7-137">Specifies the name of the service objective to assign to the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f7-138">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="547f7-138">-SecondaryVCore</span></span>
<span data-ttu-id="547f7-139">VCore-nummer i den sekundära Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="547f7-139">The Vcore numbers of the Azure Sql Database secondary.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f7-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="547f7-140">-ServerName</span></span>
<span data-ttu-id="547f7-141">Anger namnet på SQL-servern för den primära SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="547f7-141">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547f7-142">-Taggar</span><span class="sxs-lookup"><span data-stu-id="547f7-142">-Tags</span></span>
<span data-ttu-id="547f7-143">Anger de viktigaste par i formen av en hash-tabell som ska kopplas till länken för SQL-databasfilen.</span><span class="sxs-lookup"><span data-stu-id="547f7-143">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="547f7-144">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="547f7-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f7-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="547f7-145">-Confirm</span></span>
<span data-ttu-id="547f7-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="547f7-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f7-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="547f7-147">-WhatIf</span></span>
<span data-ttu-id="547f7-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="547f7-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="547f7-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="547f7-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547f7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547f7-150">CommonParameters</span></span>
<span data-ttu-id="547f7-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="547f7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547f7-152">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="547f7-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547f7-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="547f7-153">INPUTS</span></span>

### <span data-ttu-id="547f7-154">System. String</span><span class="sxs-lookup"><span data-stu-id="547f7-154">System.String</span></span>

## <span data-ttu-id="547f7-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="547f7-155">OUTPUTS</span></span>

### <span data-ttu-id="547f7-156">Microsoft. Azure. commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="547f7-156">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="547f7-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="547f7-157">NOTES</span></span>

## <span data-ttu-id="547f7-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="547f7-158">RELATED LINKS</span></span>

[<span data-ttu-id="547f7-159">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="547f7-159">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="547f7-160">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="547f7-160">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="547f7-161">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="547f7-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
