---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseCopy.md
ms.openlocfilehash: aa2ba844e364d1c95274573a6b1b38e4550c70f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746632"
---
# <span data-ttu-id="fb712-101">New-AzSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="fb712-101">New-AzSqlDatabaseCopy</span></span>

## <span data-ttu-id="fb712-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb712-102">SYNOPSIS</span></span>
<span data-ttu-id="fb712-103">Skapar en kopia av en SQL-databas där ögonblicks bilden används för tillfället.</span><span class="sxs-lookup"><span data-stu-id="fb712-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

## <span data-ttu-id="fb712-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb712-104">SYNTAX</span></span>

### <span data-ttu-id="fb712-105">DtuBasedDatabase (standard)</span><span class="sxs-lookup"><span data-stu-id="fb712-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>] -CopyDatabaseName <String>
 [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb712-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="fb712-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseCopy [-DatabaseName] <String> [-Tags <Hashtable>] [-CopyResourceGroupName <String>]
 [-CopyServerName <String>] -CopyDatabaseName <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb712-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb712-107">DESCRIPTION</span></span>
<span data-ttu-id="fb712-108">Cmdleten **New-AzSqlDatabaseCopy** skapar en kopia av en Azure SQL-databas som använder ögonblicks bilden av data vid aktuell tidpunkt.</span><span class="sxs-lookup"><span data-stu-id="fb712-108">The **New-AzSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="fb712-109">Använd denna cmdlet i stället för Start-AzSqlDatabaseCopy-cmdleten för att skapa en databas kopia av en gång.</span><span class="sxs-lookup"><span data-stu-id="fb712-109">Use this cmdlet instead of the Start-AzSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="fb712-110">Denna cmdlet returnerar kopians **databas** objekt.</span><span class="sxs-lookup"><span data-stu-id="fb712-110">This cmdlet returns the **Database** object of the copy.</span></span>
<span data-ttu-id="fb712-111">Obs! Använd cmdleten New-AzSqlDatabaseSecondary för att konfigurera geo-replikering för en databas.</span><span class="sxs-lookup"><span data-stu-id="fb712-111">Note: Use the New-AzSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>
<span data-ttu-id="fb712-112">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="fb712-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="fb712-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb712-113">EXAMPLES</span></span>

## <span data-ttu-id="fb712-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb712-114">PARAMETERS</span></span>

### <span data-ttu-id="fb712-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb712-115">-AsJob</span></span>
<span data-ttu-id="fb712-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="fb712-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb712-117">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="fb712-117">-ComputeGeneration</span></span>
<span data-ttu-id="fb712-118">Skapa en ny kopia av beräkningen.</span><span class="sxs-lookup"><span data-stu-id="fb712-118">The compute generation to assign to the new copy.</span></span>

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

### <span data-ttu-id="fb712-119">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fb712-119">-CopyDatabaseName</span></span>
<span data-ttu-id="fb712-120">Anger namnet på kopian av SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="fb712-120">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="fb712-121">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb712-121">-CopyResourceGroupName</span></span>
<span data-ttu-id="fb712-122">Anger namnet på den Azure Resource-grupp som du vill tilldela kopian i.</span><span class="sxs-lookup"><span data-stu-id="fb712-122">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="fb712-123">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="fb712-123">-CopyServerName</span></span>
<span data-ttu-id="fb712-124">Anger namnet på den SQL Server som är värd för kopian.</span><span class="sxs-lookup"><span data-stu-id="fb712-124">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="fb712-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fb712-125">-DatabaseName</span></span>
<span data-ttu-id="fb712-126">Anger namnet på den SQL-databas som ska kopieras.</span><span class="sxs-lookup"><span data-stu-id="fb712-126">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="fb712-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb712-127">-DefaultProfile</span></span>
<span data-ttu-id="fb712-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fb712-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb712-129">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fb712-129">-ElasticPoolName</span></span>
<span data-ttu-id="fb712-130">Anger namnet på den elastiska pool som kopian ska kopplas till.</span><span class="sxs-lookup"><span data-stu-id="fb712-130">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="fb712-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fb712-131">-LicenseType</span></span>
<span data-ttu-id="fb712-132">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="fb712-132">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="fb712-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb712-133">-ResourceGroupName</span></span>
<span data-ttu-id="fb712-134">Anger namnet på den resurs grupp som innehåller databasen som ska kopieras.</span><span class="sxs-lookup"><span data-stu-id="fb712-134">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="fb712-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fb712-135">-ServerName</span></span>
<span data-ttu-id="fb712-136">Anger namnet på den SQL Server som innehåller databasen som ska kopieras.</span><span class="sxs-lookup"><span data-stu-id="fb712-136">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="fb712-137">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="fb712-137">-ServiceObjectiveName</span></span>
<span data-ttu-id="fb712-138">Anger namnet på det tjänst mål som ska kopplas till kopian.</span><span class="sxs-lookup"><span data-stu-id="fb712-138">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="fb712-139">-Taggar</span><span class="sxs-lookup"><span data-stu-id="fb712-139">-Tags</span></span>
<span data-ttu-id="fb712-140">Anger de viktigaste par i formen av en hash-tabell som ska kopplas till din kopia av Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="fb712-140">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="fb712-141">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="fb712-141">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fb712-142">-VCore</span><span class="sxs-lookup"><span data-stu-id="fb712-142">-VCore</span></span>
<span data-ttu-id="fb712-143">VCore-nummer i Azure SQL-databasfilen.</span><span class="sxs-lookup"><span data-stu-id="fb712-143">The Vcore numbers of the Azure Sql Database copy.</span></span>

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

### <span data-ttu-id="fb712-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb712-144">-Confirm</span></span>
<span data-ttu-id="fb712-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb712-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb712-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb712-146">-WhatIf</span></span>
<span data-ttu-id="fb712-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb712-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb712-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb712-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb712-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb712-149">CommonParameters</span></span>
<span data-ttu-id="fb712-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb712-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb712-151">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb712-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb712-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb712-152">INPUTS</span></span>

### <span data-ttu-id="fb712-153">System. String</span><span class="sxs-lookup"><span data-stu-id="fb712-153">System.String</span></span>

## <span data-ttu-id="fb712-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb712-154">OUTPUTS</span></span>

### <span data-ttu-id="fb712-155">Microsoft. Azure. commands. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="fb712-155">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>

## <span data-ttu-id="fb712-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb712-156">NOTES</span></span>

## <span data-ttu-id="fb712-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb712-157">RELATED LINKS</span></span>

[<span data-ttu-id="fb712-158">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="fb712-158">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="fb712-159">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="fb712-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)