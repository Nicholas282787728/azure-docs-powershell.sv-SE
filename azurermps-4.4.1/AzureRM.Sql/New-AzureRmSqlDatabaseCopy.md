---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: a962ca86c3d65cd11da4169626ed932bb78653b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757987"
---
# <span data-ttu-id="a600f-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a600f-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="a600f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a600f-102">SYNOPSIS</span></span>
<span data-ttu-id="a600f-103">Skapar en kopia av en SQL-databas där ögonblicks bilden används för tillfället.</span><span class="sxs-lookup"><span data-stu-id="a600f-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a600f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a600f-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a600f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a600f-105">DESCRIPTION</span></span>
<span data-ttu-id="a600f-106">Cmdleten **New-AzureRmSqlDatabaseCopy** skapar en kopia av en Azure SQL-databas som använder ögonblicks bilden av data vid aktuell tidpunkt.</span><span class="sxs-lookup"><span data-stu-id="a600f-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="a600f-107">Använd denna cmdlet i stället för Start-AzureSqlDatabaseCopy-cmdleten för att skapa en databas kopia av en gång.</span><span class="sxs-lookup"><span data-stu-id="a600f-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="a600f-108">Denna cmdlet returnerar kopians **databas** objekt.</span><span class="sxs-lookup"><span data-stu-id="a600f-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="a600f-109">Obs! Använd cmdleten New-AzureRmSqlDatabaseSecondary för att konfigurera geo-replikering för en databas.</span><span class="sxs-lookup"><span data-stu-id="a600f-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="a600f-110">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="a600f-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a600f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a600f-111">EXAMPLES</span></span>

## <span data-ttu-id="a600f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a600f-112">PARAMETERS</span></span>

### <span data-ttu-id="a600f-113">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a600f-113">-CopyDatabaseName</span></span>
<span data-ttu-id="a600f-114">Anger namnet på kopian av SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="a600f-114">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="a600f-115">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a600f-115">-CopyResourceGroupName</span></span>
<span data-ttu-id="a600f-116">Anger namnet på den Azure Resource-grupp som du vill tilldela kopian i.</span><span class="sxs-lookup"><span data-stu-id="a600f-116">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="a600f-117">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="a600f-117">-CopyServerName</span></span>
<span data-ttu-id="a600f-118">Anger namnet på den SQL Server som är värd för kopian.</span><span class="sxs-lookup"><span data-stu-id="a600f-118">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="a600f-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a600f-119">-DatabaseName</span></span>
<span data-ttu-id="a600f-120">Anger namnet på den SQL-databas som ska kopieras.</span><span class="sxs-lookup"><span data-stu-id="a600f-120">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="a600f-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a600f-121">-ElasticPoolName</span></span>
<span data-ttu-id="a600f-122">Anger namnet på den elastiska pool som kopian ska kopplas till.</span><span class="sxs-lookup"><span data-stu-id="a600f-122">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="a600f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a600f-123">-ResourceGroupName</span></span>
<span data-ttu-id="a600f-124">Anger namnet på den resurs grupp som den här cmdleten tilldelar den kopierade databasen.</span><span class="sxs-lookup"><span data-stu-id="a600f-124">Specifies the name of the  Resource Group to which this cmdlet assigns the copied database.</span></span>

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

### <span data-ttu-id="a600f-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a600f-125">-ServerName</span></span>
<span data-ttu-id="a600f-126">Anger namnet på den SQL Server som innehåller databasen som ska kopieras.</span><span class="sxs-lookup"><span data-stu-id="a600f-126">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="a600f-127">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="a600f-127">-ServiceObjectiveName</span></span>
<span data-ttu-id="a600f-128">Anger namnet på det tjänst mål som ska kopplas till kopian.</span><span class="sxs-lookup"><span data-stu-id="a600f-128">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="a600f-129">-Taggar</span><span class="sxs-lookup"><span data-stu-id="a600f-129">-Tags</span></span>
<span data-ttu-id="a600f-130">Anger de viktigaste par i formen av en hash-tabell som ska kopplas till din kopia av Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="a600f-130">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="a600f-131">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="a600f-131">For example:</span></span>

<span data-ttu-id="a600f-132">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="a600f-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a600f-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a600f-133">-Confirm</span></span>
<span data-ttu-id="a600f-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a600f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a600f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a600f-135">-WhatIf</span></span>
<span data-ttu-id="a600f-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a600f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a600f-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a600f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a600f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a600f-138">-DefaultProfile</span></span>
<span data-ttu-id="a600f-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a600f-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a600f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a600f-140">CommonParameters</span></span>
<span data-ttu-id="a600f-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a600f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a600f-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a600f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a600f-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a600f-143">INPUTS</span></span>

## <span data-ttu-id="a600f-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a600f-144">OUTPUTS</span></span>

### <span data-ttu-id="a600f-145">Microsoft. Azure. commands. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="a600f-145">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="a600f-146">Denna cmdlet returnerar ett **databas** objekt som representerar den kopierade databasen.</span><span class="sxs-lookup"><span data-stu-id="a600f-146">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="a600f-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a600f-147">NOTES</span></span>

## <span data-ttu-id="a600f-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a600f-148">RELATED LINKS</span></span>

[<span data-ttu-id="a600f-149">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a600f-149">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="a600f-150">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="a600f-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
