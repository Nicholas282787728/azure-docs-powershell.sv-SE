---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: adf689396930b57b18c53d5ac6d98478ab6f952a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746728"
---
# <span data-ttu-id="592b6-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="592b6-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="592b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="592b6-102">SYNOPSIS</span></span>
<span data-ttu-id="592b6-103">Hämtar kodtips för en databas.</span><span class="sxs-lookup"><span data-stu-id="592b6-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="592b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="592b6-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="592b6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="592b6-105">DESCRIPTION</span></span>
<span data-ttu-id="592b6-106">Cmdleten **Get-AzSqlDatabaseUpgradeHint** får pris nivå tips för uppgradering av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="592b6-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="592b6-107">Databaser som fortfarande finns i webb-och företags pris nivåer är ett tips för att du ska kunna uppgradera till de nya grund klasserna.</span><span class="sxs-lookup"><span data-stu-id="592b6-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="592b6-108">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="592b6-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="592b6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="592b6-109">EXAMPLES</span></span>

### <span data-ttu-id="592b6-110">Exempel 1: få rekommendationer för alla databaser på en server</span><span class="sxs-lookup"><span data-stu-id="592b6-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="592b6-111">Det här kommandot returnerar uppgraderings tips för alla databaser på servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="592b6-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="592b6-112">Exempel 2: få rekommendationer för specifik databas</span><span class="sxs-lookup"><span data-stu-id="592b6-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="592b6-113">Det här kommandot returnerar ett uppgraderings tips för en viss databas.</span><span class="sxs-lookup"><span data-stu-id="592b6-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="592b6-114">Exempel 3: få rekommendationer för alla databaser som inte är i en elastisk databas</span><span class="sxs-lookup"><span data-stu-id="592b6-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="592b6-115">Det här kommandot returnerar ett uppgraderings tips för alla databaser som inte är i en elastisk databas.</span><span class="sxs-lookup"><span data-stu-id="592b6-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="592b6-116">Exempel 4: få rekommendationer för alla databaser på en server med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="592b6-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="592b6-117">Det här kommandot returnerar uppgraderings tips för alla databaser på servern med namnet Server01 som börjar med "databas".</span><span class="sxs-lookup"><span data-stu-id="592b6-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="592b6-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="592b6-118">PARAMETERS</span></span>

### <span data-ttu-id="592b6-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="592b6-119">-DatabaseName</span></span>
<span data-ttu-id="592b6-120">Anger namnet på den SQL-databas för vilken denna cmdlet får ett uppgraderings tips.</span><span class="sxs-lookup"><span data-stu-id="592b6-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="592b6-121">Om du inte anger en databas får denna cmdlet tips för alla databaser på den logiska servern.</span><span class="sxs-lookup"><span data-stu-id="592b6-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="592b6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592b6-122">-DefaultProfile</span></span>
<span data-ttu-id="592b6-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="592b6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="592b6-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="592b6-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="592b6-125">Anger om databaser i Elastic Database-pooler exkluderas från de rekommendationer som returneras.</span><span class="sxs-lookup"><span data-stu-id="592b6-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="592b6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="592b6-126">-ResourceGroupName</span></span>
<span data-ttu-id="592b6-127">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="592b6-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="592b6-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="592b6-128">-ServerName</span></span>
<span data-ttu-id="592b6-129">Anger namnet på den server som är värd för databasen för vilken denna cmdlet får ett uppgraderings tips.</span><span class="sxs-lookup"><span data-stu-id="592b6-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="592b6-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="592b6-130">-Confirm</span></span>
<span data-ttu-id="592b6-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="592b6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="592b6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="592b6-132">-WhatIf</span></span>
<span data-ttu-id="592b6-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="592b6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="592b6-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="592b6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="592b6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592b6-135">CommonParameters</span></span>
<span data-ttu-id="592b6-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="592b6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592b6-137">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="592b6-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592b6-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="592b6-138">INPUTS</span></span>

### <span data-ttu-id="592b6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="592b6-139">System.String</span></span>

### <span data-ttu-id="592b6-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="592b6-140">System.Boolean</span></span>

## <span data-ttu-id="592b6-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="592b6-141">OUTPUTS</span></span>

### <span data-ttu-id="592b6-142">Microsoft. Azure. Management. SQL. LegacySdk. Models. RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="592b6-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="592b6-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="592b6-143">NOTES</span></span>

## <span data-ttu-id="592b6-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="592b6-144">RELATED LINKS</span></span>

[<span data-ttu-id="592b6-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="592b6-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="592b6-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="592b6-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


