---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 7019fc7345b4296d9c35f11c6acec5bf5a42d966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583448"
---
# <span data-ttu-id="3c260-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3c260-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="3c260-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c260-102">SYNOPSIS</span></span>
<span data-ttu-id="3c260-103">Skapar en kopia av en SQL-databas där ögonblicks bilden används för tillfället.</span><span class="sxs-lookup"><span data-stu-id="3c260-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c260-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c260-104">SYNTAX</span></span>

### <span data-ttu-id="3c260-105">DtuBasedDatabase (standard)</span><span class="sxs-lookup"><span data-stu-id="3c260-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c260-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="3c260-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-Tags <Hashtable>] [-CopyResourceGroupName <String>]
 [-CopyServerName <String>] -CopyDatabaseName <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c260-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c260-107">DESCRIPTION</span></span>
<span data-ttu-id="3c260-108">Cmdleten **New-AzureRmSqlDatabaseCopy** skapar en kopia av en Azure SQL-databas som använder ögonblicks bilden av data vid aktuell tidpunkt.</span><span class="sxs-lookup"><span data-stu-id="3c260-108">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="3c260-109">Använd denna cmdlet i stället för Start-AzureSqlDatabaseCopy-cmdleten för att skapa en databas kopia av en gång.</span><span class="sxs-lookup"><span data-stu-id="3c260-109">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="3c260-110">Denna cmdlet returnerar kopians **databas** objekt.</span><span class="sxs-lookup"><span data-stu-id="3c260-110">This cmdlet returns the **Database** object of the copy.</span></span>
<span data-ttu-id="3c260-111">Obs! Använd cmdleten New-AzureRmSqlDatabaseSecondary för att konfigurera geo-replikering för en databas.</span><span class="sxs-lookup"><span data-stu-id="3c260-111">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>
<span data-ttu-id="3c260-112">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="3c260-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3c260-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c260-113">EXAMPLES</span></span>

## <span data-ttu-id="3c260-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c260-114">PARAMETERS</span></span>

### <span data-ttu-id="3c260-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c260-115">-AsJob</span></span>
<span data-ttu-id="3c260-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3c260-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c260-117">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="3c260-117">-ComputeGeneration</span></span>
<span data-ttu-id="3c260-118">Skapa en ny kopia av beräkningen.</span><span class="sxs-lookup"><span data-stu-id="3c260-118">The compute generation to assign to the new copy.</span></span>

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

### <span data-ttu-id="3c260-119">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3c260-119">-CopyDatabaseName</span></span>
<span data-ttu-id="3c260-120">Anger namnet på kopian av SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3c260-120">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="3c260-121">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c260-121">-CopyResourceGroupName</span></span>
<span data-ttu-id="3c260-122">Anger namnet på den Azure Resource-grupp som du vill tilldela kopian i.</span><span class="sxs-lookup"><span data-stu-id="3c260-122">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="3c260-123">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="3c260-123">-CopyServerName</span></span>
<span data-ttu-id="3c260-124">Anger namnet på den SQL Server som är värd för kopian.</span><span class="sxs-lookup"><span data-stu-id="3c260-124">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="3c260-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3c260-125">-DatabaseName</span></span>
<span data-ttu-id="3c260-126">Anger namnet på den SQL-databas som ska kopieras.</span><span class="sxs-lookup"><span data-stu-id="3c260-126">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="3c260-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c260-127">-DefaultProfile</span></span>
<span data-ttu-id="3c260-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3c260-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c260-129">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3c260-129">-ElasticPoolName</span></span>
<span data-ttu-id="3c260-130">Anger namnet på den elastiska pool som kopian ska kopplas till.</span><span class="sxs-lookup"><span data-stu-id="3c260-130">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="3c260-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3c260-131">-LicenseType</span></span>
<span data-ttu-id="3c260-132">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3c260-132">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="3c260-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c260-133">-ResourceGroupName</span></span>
<span data-ttu-id="3c260-134">Anger namnet på den resurs grupp som innehåller databasen som ska kopieras.</span><span class="sxs-lookup"><span data-stu-id="3c260-134">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="3c260-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3c260-135">-ServerName</span></span>
<span data-ttu-id="3c260-136">Anger namnet på den SQL Server som innehåller databasen som ska kopieras.</span><span class="sxs-lookup"><span data-stu-id="3c260-136">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="3c260-137">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="3c260-137">-ServiceObjectiveName</span></span>
<span data-ttu-id="3c260-138">Anger namnet på det tjänst mål som ska kopplas till kopian.</span><span class="sxs-lookup"><span data-stu-id="3c260-138">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="3c260-139">-Taggar</span><span class="sxs-lookup"><span data-stu-id="3c260-139">-Tags</span></span>
<span data-ttu-id="3c260-140">Anger de viktigaste par i formen av en hash-tabell som ska kopplas till din kopia av Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3c260-140">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="3c260-141">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="3c260-141">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3c260-142">-VCore</span><span class="sxs-lookup"><span data-stu-id="3c260-142">-VCore</span></span>
<span data-ttu-id="3c260-143">VCore-nummer i Azure SQL-databasfilen.</span><span class="sxs-lookup"><span data-stu-id="3c260-143">The Vcore numbers of the Azure Sql Database copy.</span></span>

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

### <span data-ttu-id="3c260-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3c260-144">-Confirm</span></span>
<span data-ttu-id="3c260-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3c260-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c260-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c260-146">-WhatIf</span></span>
<span data-ttu-id="3c260-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3c260-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c260-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3c260-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c260-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c260-149">CommonParameters</span></span>
<span data-ttu-id="3c260-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c260-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c260-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c260-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c260-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c260-152">INPUTS</span></span>

### <span data-ttu-id="3c260-153">System. String</span><span class="sxs-lookup"><span data-stu-id="3c260-153">System.String</span></span>

## <span data-ttu-id="3c260-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c260-154">OUTPUTS</span></span>

### <span data-ttu-id="3c260-155">Microsoft. Azure. commands. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="3c260-155">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>

## <span data-ttu-id="3c260-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c260-156">NOTES</span></span>

## <span data-ttu-id="3c260-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c260-157">RELATED LINKS</span></span>

[<span data-ttu-id="3c260-158">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3c260-158">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="3c260-159">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="3c260-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
