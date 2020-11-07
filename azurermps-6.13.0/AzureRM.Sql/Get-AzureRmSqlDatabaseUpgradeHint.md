---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b289dc637b3d75321120f06eb9ddf604ebcdabba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756659"
---
# <span data-ttu-id="49af6-101">Get-AzureRmSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="49af6-101">Get-AzureRmSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="49af6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49af6-102">SYNOPSIS</span></span>
<span data-ttu-id="49af6-103">Hämtar kodtips för en databas.</span><span class="sxs-lookup"><span data-stu-id="49af6-103">Gets pricing tier hints for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49af6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49af6-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49af6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49af6-105">DESCRIPTION</span></span>
<span data-ttu-id="49af6-106">Cmdleten **Get-AzureRmSqlDatabaseUpgradeHint** får pris nivå tips för uppgradering av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="49af6-106">The **Get-AzureRmSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="49af6-107">Databaser som fortfarande finns i webb-och företags pris nivåer är ett tips för att du ska kunna uppgradera till de nya grund klasserna.</span><span class="sxs-lookup"><span data-stu-id="49af6-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="49af6-108">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="49af6-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="49af6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49af6-109">EXAMPLES</span></span>

### <span data-ttu-id="49af6-110">Exempel 1: få rekommendationer för alla databaser på en server</span><span class="sxs-lookup"><span data-stu-id="49af6-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="49af6-111">Det här kommandot returnerar uppgraderings tips för alla databaser på servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="49af6-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="49af6-112">Exempel 2: få rekommendationer för specifik databas</span><span class="sxs-lookup"><span data-stu-id="49af6-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="49af6-113">Det här kommandot returnerar ett uppgraderings tips för en viss databas.</span><span class="sxs-lookup"><span data-stu-id="49af6-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="49af6-114">Exempel 3: få rekommendationer för alla databaser som inte är i en elastisk databas</span><span class="sxs-lookup"><span data-stu-id="49af6-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="49af6-115">Det här kommandot returnerar ett uppgraderings tips för alla databaser som inte är i en elastisk databas.</span><span class="sxs-lookup"><span data-stu-id="49af6-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

## <span data-ttu-id="49af6-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49af6-116">PARAMETERS</span></span>

### <span data-ttu-id="49af6-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="49af6-117">-DatabaseName</span></span>
<span data-ttu-id="49af6-118">Anger namnet på den SQL-databas för vilken denna cmdlet får ett uppgraderings tips.</span><span class="sxs-lookup"><span data-stu-id="49af6-118">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="49af6-119">Om du inte anger en databas får denna cmdlet tips för alla databaser på den logiska servern.</span><span class="sxs-lookup"><span data-stu-id="49af6-119">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="49af6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49af6-120">-DefaultProfile</span></span>
<span data-ttu-id="49af6-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="49af6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49af6-122">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="49af6-122">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="49af6-123">Anger om databaser i Elastic Database-pooler exkluderas från de rekommendationer som returneras.</span><span class="sxs-lookup"><span data-stu-id="49af6-123">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="49af6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49af6-124">-ResourceGroupName</span></span>
<span data-ttu-id="49af6-125">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="49af6-125">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="49af6-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="49af6-126">-ServerName</span></span>
<span data-ttu-id="49af6-127">Anger namnet på den server som är värd för databasen för vilken denna cmdlet får ett uppgraderings tips.</span><span class="sxs-lookup"><span data-stu-id="49af6-127">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="49af6-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="49af6-128">-Confirm</span></span>
<span data-ttu-id="49af6-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="49af6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49af6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49af6-130">-WhatIf</span></span>
<span data-ttu-id="49af6-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="49af6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49af6-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="49af6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49af6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49af6-133">CommonParameters</span></span>
<span data-ttu-id="49af6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49af6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49af6-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49af6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49af6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49af6-136">INPUTS</span></span>

### <span data-ttu-id="49af6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="49af6-137">System.String</span></span>

### <span data-ttu-id="49af6-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49af6-138">System.Boolean</span></span>

## <span data-ttu-id="49af6-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49af6-139">OUTPUTS</span></span>

### <span data-ttu-id="49af6-140">Microsoft. Azure. Management. SQL. LegacySdk. Models. RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="49af6-140">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="49af6-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49af6-141">NOTES</span></span>

## <span data-ttu-id="49af6-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49af6-142">RELATED LINKS</span></span>

[<span data-ttu-id="49af6-143">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="49af6-143">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="49af6-144">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="49af6-144">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)


