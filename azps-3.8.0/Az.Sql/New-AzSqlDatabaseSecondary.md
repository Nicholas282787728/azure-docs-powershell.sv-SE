---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: f7dbffffe9a51d35ced8861894373322898fd0f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090194"
---
# <span data-ttu-id="e8314-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e8314-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="e8314-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8314-102">SYNOPSIS</span></span>
<span data-ttu-id="e8314-103">Skapar en sekundär databas för en befintlig databas och startar datareplikering.</span><span class="sxs-lookup"><span data-stu-id="e8314-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="e8314-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8314-104">SYNTAX</span></span>

### <span data-ttu-id="e8314-105">DtuBasedDatabase (standard)</span><span class="sxs-lookup"><span data-stu-id="e8314-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8314-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="e8314-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8314-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8314-107">DESCRIPTION</span></span>
<span data-ttu-id="e8314-108">**New-AzSqlDatabaseSecondary** cmdlet ersätter Start-AzSqlDatabaseCopy cmdlet när den används för att konfigurera geo-replikering för en databas.</span><span class="sxs-lookup"><span data-stu-id="e8314-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="e8314-109">Det returnerar det geo-replikeringslänk som är länkat till den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="e8314-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="e8314-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8314-110">EXAMPLES</span></span>

### <span data-ttu-id="e8314-111">1: etablera Active Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="e8314-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="e8314-112">2: etablera Active Geo-Replication och ange partner databasens namn som inte är käll databasens namn</span><span class="sxs-lookup"><span data-stu-id="e8314-112">2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="e8314-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8314-113">PARAMETERS</span></span>

### <span data-ttu-id="e8314-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="e8314-114">-AllowConnections</span></span>
<span data-ttu-id="e8314-115">Anger det alternativa Azure SQL-databasens Läs metod.</span><span class="sxs-lookup"><span data-stu-id="e8314-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="e8314-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e8314-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e8314-117">Nej</span><span class="sxs-lookup"><span data-stu-id="e8314-117">No</span></span>
- <span data-ttu-id="e8314-118">Alla</span><span class="sxs-lookup"><span data-stu-id="e8314-118">All</span></span>

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

### <span data-ttu-id="e8314-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8314-119">-AsJob</span></span>
<span data-ttu-id="e8314-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e8314-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8314-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e8314-121">-DatabaseName</span></span>
<span data-ttu-id="e8314-122">Anger namnet på databasen som ska fungera som primärt.</span><span class="sxs-lookup"><span data-stu-id="e8314-122">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="e8314-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8314-123">-DefaultProfile</span></span>
<span data-ttu-id="e8314-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e8314-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8314-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e8314-125">-LicenseType</span></span>
<span data-ttu-id="e8314-126">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="e8314-126">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="e8314-127">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e8314-127">-PartnerDatabaseName</span></span>
<span data-ttu-id="e8314-128">Namnet på den sekundära databasen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e8314-128">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="e8314-129">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8314-129">-PartnerResourceGroupName</span></span>
<span data-ttu-id="e8314-130">Anger namnet på den Azure Resource-grupp som den här cmdleten tilldelar den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="e8314-130">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="e8314-131">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="e8314-131">-PartnerServerName</span></span>
<span data-ttu-id="e8314-132">Anger namnet på den databas server för Azure SQL som ska fungera som sekundär.</span><span class="sxs-lookup"><span data-stu-id="e8314-132">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="e8314-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8314-133">-ResourceGroupName</span></span>
<span data-ttu-id="e8314-134">Anger namnet på den Azure Resource-grupp som den här cmdleten tilldelar den primära databasen.</span><span class="sxs-lookup"><span data-stu-id="e8314-134">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="e8314-135">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="e8314-135">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="e8314-136">Beräkna skapandet av Azure SQL Database sekundär.</span><span class="sxs-lookup"><span data-stu-id="e8314-136">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="e8314-137">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e8314-137">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="e8314-138">Anger namnet på den elastiska pool som den sekundära databasen ska placeras i.</span><span class="sxs-lookup"><span data-stu-id="e8314-138">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="e8314-139">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e8314-139">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="e8314-140">Anger namnet på det tjänst mål som ska kopplas till den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="e8314-140">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="e8314-141">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="e8314-141">-SecondaryVCore</span></span>
<span data-ttu-id="e8314-142">VCore-nummer i den sekundära Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="e8314-142">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="e8314-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e8314-143">-ServerName</span></span>
<span data-ttu-id="e8314-144">Anger namnet på SQL-servern för den primära SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="e8314-144">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="e8314-145">-Taggar</span><span class="sxs-lookup"><span data-stu-id="e8314-145">-Tags</span></span>
<span data-ttu-id="e8314-146">Anger de viktigaste par i formen av en hash-tabell som ska kopplas till länken för SQL-databasfilen.</span><span class="sxs-lookup"><span data-stu-id="e8314-146">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="e8314-147">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="e8314-147">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e8314-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e8314-148">-Confirm</span></span>
<span data-ttu-id="e8314-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e8314-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8314-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8314-150">-WhatIf</span></span>
<span data-ttu-id="e8314-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e8314-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8314-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e8314-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8314-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8314-153">CommonParameters</span></span>
<span data-ttu-id="e8314-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8314-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8314-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8314-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8314-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8314-156">INPUTS</span></span>

### <span data-ttu-id="e8314-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e8314-157">System.String</span></span>

## <span data-ttu-id="e8314-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8314-158">OUTPUTS</span></span>

### <span data-ttu-id="e8314-159">Microsoft. Azure. commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="e8314-159">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="e8314-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8314-160">NOTES</span></span>

## <span data-ttu-id="e8314-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8314-161">RELATED LINKS</span></span>

[<span data-ttu-id="e8314-162">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e8314-162">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="e8314-163">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e8314-163">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="e8314-164">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e8314-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
