---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 4e9d33691cfd09681bb115c89d0eaf351ef14f13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573167"
---
# <span data-ttu-id="d24ae-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="d24ae-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="d24ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d24ae-102">SYNOPSIS</span></span>
<span data-ttu-id="d24ae-103">Skapar en kopia av en SQL-databas där ögonblicks bilden används för tillfället.</span><span class="sxs-lookup"><span data-stu-id="d24ae-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d24ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d24ae-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d24ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d24ae-105">DESCRIPTION</span></span>
<span data-ttu-id="d24ae-106">Cmdleten **New-AzureRmSqlDatabaseCopy** skapar en kopia av en Azure SQL-databas som använder ögonblicks bilden av data vid aktuell tidpunkt.</span><span class="sxs-lookup"><span data-stu-id="d24ae-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="d24ae-107">Använd denna cmdlet i stället för Start-AzureSqlDatabaseCopy-cmdleten för att skapa en databas kopia av en gång.</span><span class="sxs-lookup"><span data-stu-id="d24ae-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="d24ae-108">Denna cmdlet returnerar kopians **databas** objekt.</span><span class="sxs-lookup"><span data-stu-id="d24ae-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="d24ae-109">Obs! Använd cmdleten New-AzureRmSqlDatabaseSecondary för att konfigurera geo-replikering för en databas.</span><span class="sxs-lookup"><span data-stu-id="d24ae-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="d24ae-110">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="d24ae-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d24ae-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d24ae-111">EXAMPLES</span></span>

## <span data-ttu-id="d24ae-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d24ae-112">PARAMETERS</span></span>

### <span data-ttu-id="d24ae-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d24ae-113">-AsJob</span></span>
<span data-ttu-id="d24ae-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d24ae-114">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24ae-115">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d24ae-115">-CopyDatabaseName</span></span>
<span data-ttu-id="d24ae-116">Anger namnet på kopian av SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="d24ae-116">Specifies the name of the SQL Database copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24ae-117">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d24ae-117">-CopyResourceGroupName</span></span>
<span data-ttu-id="d24ae-118">Anger namnet på den Azure Resource-grupp som du vill tilldela kopian i.</span><span class="sxs-lookup"><span data-stu-id="d24ae-118">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24ae-119">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="d24ae-119">-CopyServerName</span></span>
<span data-ttu-id="d24ae-120">Anger namnet på den SQL Server som är värd för kopian.</span><span class="sxs-lookup"><span data-stu-id="d24ae-120">Specifies the name of the SQL Server which hosts the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24ae-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d24ae-121">-DatabaseName</span></span>
<span data-ttu-id="d24ae-122">Anger namnet på den SQL-databas som ska kopieras.</span><span class="sxs-lookup"><span data-stu-id="d24ae-122">Specifies the name of the SQL Database to copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d24ae-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24ae-123">-DefaultProfile</span></span>
<span data-ttu-id="d24ae-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d24ae-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24ae-125">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d24ae-125">-ElasticPoolName</span></span>
<span data-ttu-id="d24ae-126">Anger namnet på den elastiska pool som kopian ska kopplas till.</span><span class="sxs-lookup"><span data-stu-id="d24ae-126">Specifies the name of the elastic pool in which to assign the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d24ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="d24ae-128">Anger namnet på den resurs grupp som innehåller databasen som ska kopieras.</span><span class="sxs-lookup"><span data-stu-id="d24ae-128">Specifies the name of the Resource Group that contains the database to copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d24ae-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d24ae-129">-ServerName</span></span>
<span data-ttu-id="d24ae-130">Anger namnet på den SQL Server som innehåller databasen som ska kopieras.</span><span class="sxs-lookup"><span data-stu-id="d24ae-130">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d24ae-131">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="d24ae-131">-ServiceObjectiveName</span></span>
<span data-ttu-id="d24ae-132">Anger namnet på det tjänst mål som ska kopplas till kopian.</span><span class="sxs-lookup"><span data-stu-id="d24ae-132">Specifies the name of the service objective to assign to the copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24ae-133">-Taggar</span><span class="sxs-lookup"><span data-stu-id="d24ae-133">-Tags</span></span>
<span data-ttu-id="d24ae-134">Anger de viktigaste par i formen av en hash-tabell som ska kopplas till din kopia av Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="d24ae-134">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="d24ae-135">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="d24ae-135">For example:</span></span>

<span data-ttu-id="d24ae-136">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="d24ae-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24ae-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d24ae-137">-Confirm</span></span>
<span data-ttu-id="d24ae-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d24ae-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24ae-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d24ae-139">-WhatIf</span></span>
<span data-ttu-id="d24ae-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d24ae-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d24ae-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d24ae-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24ae-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24ae-142">CommonParameters</span></span>
<span data-ttu-id="d24ae-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d24ae-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24ae-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d24ae-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24ae-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d24ae-145">INPUTS</span></span>

### <span data-ttu-id="d24ae-146">Ingen</span><span class="sxs-lookup"><span data-stu-id="d24ae-146">None</span></span>
<span data-ttu-id="d24ae-147">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d24ae-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d24ae-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d24ae-148">OUTPUTS</span></span>

### <span data-ttu-id="d24ae-149">Microsoft. Azure. commands. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="d24ae-149">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="d24ae-150">Denna cmdlet returnerar ett **databas** objekt som representerar den kopierade databasen.</span><span class="sxs-lookup"><span data-stu-id="d24ae-150">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="d24ae-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d24ae-151">NOTES</span></span>

## <span data-ttu-id="d24ae-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d24ae-152">RELATED LINKS</span></span>

[<span data-ttu-id="d24ae-153">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d24ae-153">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="d24ae-154">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="d24ae-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
