---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: cc8881657c541a15ade44242ab5fb0e84c9bbab8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522254"
---
# <span data-ttu-id="598ba-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="598ba-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="598ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="598ba-102">SYNOPSIS</span></span>
<span data-ttu-id="598ba-103">Skapar en sekundär databas för en befintlig databas och startar datareplikering.</span><span class="sxs-lookup"><span data-stu-id="598ba-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="598ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="598ba-104">SYNTAX</span></span>

### <span data-ttu-id="598ba-105">DtuBasedDatabase (standard)</span><span class="sxs-lookup"><span data-stu-id="598ba-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="598ba-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="598ba-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="598ba-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="598ba-107">DESCRIPTION</span></span>
<span data-ttu-id="598ba-108">**New-AzSqlDatabaseSecondary** cmdlet ersätter Start-AzSqlDatabaseCopy cmdlet när den används för att konfigurera geo-replikering för en databas.</span><span class="sxs-lookup"><span data-stu-id="598ba-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="598ba-109">Det returnerar det geo-replikeringslänk som är länkat till den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="598ba-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="598ba-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="598ba-110">EXAMPLES</span></span>

### <span data-ttu-id="598ba-111">Exempel 1: etablera Active Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="598ba-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="598ba-112">Exempel 2: etablera Active Geo-Replication och ange partner databasens namn som inte är käll databasens namn</span><span class="sxs-lookup"><span data-stu-id="598ba-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="598ba-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="598ba-113">PARAMETERS</span></span>

### <span data-ttu-id="598ba-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="598ba-114">-AllowConnections</span></span>
<span data-ttu-id="598ba-115">Anger det alternativa Azure SQL-databasens Läs metod.</span><span class="sxs-lookup"><span data-stu-id="598ba-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="598ba-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="598ba-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="598ba-117">Nej</span><span class="sxs-lookup"><span data-stu-id="598ba-117">No</span></span>
- <span data-ttu-id="598ba-118">Alla</span><span class="sxs-lookup"><span data-stu-id="598ba-118">All</span></span>

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

### <span data-ttu-id="598ba-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="598ba-119">-AsJob</span></span>
<span data-ttu-id="598ba-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="598ba-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="598ba-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="598ba-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="598ba-122">Säkerhets kopians lagrings utrymme som används för att lagra säkerhets kopior för SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="598ba-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="598ba-123">Alternativen är: lokal, zon och geo.</span><span class="sxs-lookup"><span data-stu-id="598ba-123">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598ba-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="598ba-124">-DatabaseName</span></span>
<span data-ttu-id="598ba-125">Anger namnet på databasen som ska fungera som primärt.</span><span class="sxs-lookup"><span data-stu-id="598ba-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="598ba-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="598ba-126">-DefaultProfile</span></span>
<span data-ttu-id="598ba-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="598ba-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="598ba-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="598ba-128">-LicenseType</span></span>
<span data-ttu-id="598ba-129">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="598ba-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="598ba-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="598ba-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="598ba-131">Namnet på den sekundära databasen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="598ba-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="598ba-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="598ba-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="598ba-133">Anger namnet på den Azure Resource-grupp som den här cmdleten tilldelar den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="598ba-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="598ba-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="598ba-134">-PartnerServerName</span></span>
<span data-ttu-id="598ba-135">Anger namnet på den databas server för Azure SQL som ska fungera som sekundär.</span><span class="sxs-lookup"><span data-stu-id="598ba-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="598ba-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="598ba-136">-ResourceGroupName</span></span>
<span data-ttu-id="598ba-137">Anger namnet på den Azure Resource-grupp som den här cmdleten tilldelar den primära databasen.</span><span class="sxs-lookup"><span data-stu-id="598ba-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="598ba-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="598ba-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="598ba-139">Beräkna skapandet av Azure SQL Database sekundär.</span><span class="sxs-lookup"><span data-stu-id="598ba-139">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="598ba-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="598ba-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="598ba-141">Anger namnet på den elastiska pool som den sekundära databasen ska placeras i.</span><span class="sxs-lookup"><span data-stu-id="598ba-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="598ba-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="598ba-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="598ba-143">Anger namnet på det tjänst mål som ska kopplas till den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="598ba-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="598ba-144">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="598ba-144">-SecondaryType</span></span>
<span data-ttu-id="598ba-145">Den sekundära typen för databasen om den är en sekundär.</span><span class="sxs-lookup"><span data-stu-id="598ba-145">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="598ba-146">Giltiga värden är geo och named.</span><span class="sxs-lookup"><span data-stu-id="598ba-146">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598ba-147">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="598ba-147">-SecondaryVCore</span></span>
<span data-ttu-id="598ba-148">VCore-nummer i den sekundära Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="598ba-148">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="598ba-149">-ServerName</span><span class="sxs-lookup"><span data-stu-id="598ba-149">-ServerName</span></span>
<span data-ttu-id="598ba-150">Anger namnet på SQL-servern för den primära SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="598ba-150">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="598ba-151">-Taggar</span><span class="sxs-lookup"><span data-stu-id="598ba-151">-Tags</span></span>
<span data-ttu-id="598ba-152">Anger de viktigaste par i formen av en hash-tabell som ska kopplas till länken för SQL-databasfilen.</span><span class="sxs-lookup"><span data-stu-id="598ba-152">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="598ba-153">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="598ba-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="598ba-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="598ba-154">-Confirm</span></span>
<span data-ttu-id="598ba-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="598ba-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="598ba-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="598ba-156">-WhatIf</span></span>
<span data-ttu-id="598ba-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="598ba-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="598ba-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="598ba-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="598ba-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="598ba-159">CommonParameters</span></span>
<span data-ttu-id="598ba-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="598ba-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="598ba-161">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="598ba-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="598ba-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="598ba-162">INPUTS</span></span>

### <span data-ttu-id="598ba-163">System. String</span><span class="sxs-lookup"><span data-stu-id="598ba-163">System.String</span></span>

## <span data-ttu-id="598ba-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="598ba-164">OUTPUTS</span></span>

### <span data-ttu-id="598ba-165">Microsoft. Azure. commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="598ba-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="598ba-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="598ba-166">NOTES</span></span>

## <span data-ttu-id="598ba-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="598ba-167">RELATED LINKS</span></span>

[<span data-ttu-id="598ba-168">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="598ba-168">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="598ba-169">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="598ba-169">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="598ba-170">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="598ba-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
