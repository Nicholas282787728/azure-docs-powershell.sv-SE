---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
ms.openlocfilehash: c0a917d2f5e10bb499ecf6fc698bee9a84d64363
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756842"
---
# <span data-ttu-id="ed9c9-101">Get-AzureRmSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="ed9c9-101">Get-AzureRmSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="ed9c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9c9-103">Hämtar kodtips för en databas.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-103">Gets pricing tier hints for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed9c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed9c9-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed9c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed9c9-105">DESCRIPTION</span></span>
<span data-ttu-id="ed9c9-106">Cmdleten **Get-AzureRmSqlDatabaseUpgradeHint** får pris nivå tips för uppgradering av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-106">The **Get-AzureRmSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="ed9c9-107">Databaser som fortfarande finns i webb-och företags pris nivåer är ett tips för att du ska kunna uppgradera till de nya grund klasserna.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>

<span data-ttu-id="ed9c9-108">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ed9c9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed9c9-109">EXAMPLES</span></span>

### <span data-ttu-id="ed9c9-110">Exempel 1: få rekommendationer för alla databaser på en server</span><span class="sxs-lookup"><span data-stu-id="ed9c9-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="ed9c9-111">Det här kommandot returnerar uppgraderings tips för alla databaser på servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="ed9c9-112">Exempel 2: få rekommendationer för specifik databas</span><span class="sxs-lookup"><span data-stu-id="ed9c9-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ed9c9-113">Det här kommandot returnerar ett uppgraderings tips för en viss databas.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="ed9c9-114">Exempel 3: få rekommendationer för alla databaser som inte är i en elastisk databas</span><span class="sxs-lookup"><span data-stu-id="ed9c9-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="ed9c9-115">Det här kommandot returnerar ett uppgraderings tips för alla databaser som inte är i en elastisk databas.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

## <span data-ttu-id="ed9c9-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed9c9-116">PARAMETERS</span></span>

### <span data-ttu-id="ed9c9-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ed9c9-117">-DatabaseName</span></span>
<span data-ttu-id="ed9c9-118">Anger namnet på den SQL-databas för vilken denna cmdlet får ett uppgraderings tips.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-118">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="ed9c9-119">Om du inte anger en databas får denna cmdlet tips för alla databaser på den logiska servern.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-119">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed9c9-120">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="ed9c9-120">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="ed9c9-121">Anger om databaser i Elastic Database-pooler exkluderas från de rekommendationer som returneras.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-121">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="ed9c9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed9c9-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed9c9-123">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-123">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ed9c9-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ed9c9-124">-ServerName</span></span>
<span data-ttu-id="ed9c9-125">Anger namnet på den server som är värd för databasen för vilken denna cmdlet får ett uppgraderings tips.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-125">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="ed9c9-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed9c9-126">-Confirm</span></span>
<span data-ttu-id="ed9c9-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed9c9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed9c9-128">-WhatIf</span></span>
<span data-ttu-id="ed9c9-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed9c9-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed9c9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9c9-131">-DefaultProfile</span></span>
<span data-ttu-id="ed9c9-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed9c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9c9-133">CommonParameters</span></span>
<span data-ttu-id="ed9c9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed9c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9c9-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed9c9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9c9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed9c9-136">INPUTS</span></span>

## <span data-ttu-id="ed9c9-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed9c9-137">OUTPUTS</span></span>

## <span data-ttu-id="ed9c9-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed9c9-138">NOTES</span></span>

## <span data-ttu-id="ed9c9-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed9c9-139">RELATED LINKS</span></span>

[<span data-ttu-id="ed9c9-140">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="ed9c9-140">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="ed9c9-141">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="ed9c9-141">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)


