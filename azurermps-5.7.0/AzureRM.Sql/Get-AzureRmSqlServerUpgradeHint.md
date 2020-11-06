---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
ms.openlocfilehash: 8516cbecac3cb4c741bb7aea1e93c10f25222b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582916"
---
# <span data-ttu-id="9da19-101">Get-AzureRmSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="9da19-101">Get-AzureRmSqlServerUpgradeHint</span></span>

## <span data-ttu-id="9da19-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9da19-102">SYNOPSIS</span></span>
<span data-ttu-id="9da19-103">Hämtar pris nivå tips för uppgradering av en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="9da19-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9da19-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9da19-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9da19-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9da19-105">DESCRIPTION</span></span>
<span data-ttu-id="9da19-106">Cmdleten **Get-AzureRmSqlServerUpgradeHint** får pris nivå tips för uppgradering av en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="9da19-106">The **Get-AzureRmSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="9da19-107">Tips kan innehålla den Elastic Database-poolen och fristående databas tips.</span><span class="sxs-lookup"><span data-stu-id="9da19-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="9da19-108">Databaser som fortfarande finns i webb-och företags pris nivåer är ett tips för att du ska kunna uppgradera till de nya grundläggande priser, standard-eller Premium-priserna eller att gå in i den Elastic Database-poolen.</span><span class="sxs-lookup"><span data-stu-id="9da19-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="9da19-109">Denna cmdlet returnerar tips för alla databaser som finns på den angivna servern.</span><span class="sxs-lookup"><span data-stu-id="9da19-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="9da19-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9da19-110">EXAMPLES</span></span>

### <span data-ttu-id="9da19-111">Exempel 1: få rekommendationer som kombineras</span><span class="sxs-lookup"><span data-stu-id="9da19-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="9da19-112">Med det här kommandot får du rekommendationer för alla databaser på en server med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="9da19-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="9da19-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9da19-113">PARAMETERS</span></span>

### <span data-ttu-id="9da19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da19-114">-DefaultProfile</span></span>
<span data-ttu-id="9da19-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9da19-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9da19-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="9da19-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="9da19-117">Anger om databaser som ingår i Elastic Database-pooler ska returneras.</span><span class="sxs-lookup"><span data-stu-id="9da19-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da19-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9da19-118">-ResourceGroupName</span></span>
<span data-ttu-id="9da19-119">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="9da19-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9da19-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9da19-120">-ServerName</span></span>
<span data-ttu-id="9da19-121">Anger namnet på den server där denna cmdlet får ett uppgraderings tips.</span><span class="sxs-lookup"><span data-stu-id="9da19-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="9da19-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9da19-122">-Confirm</span></span>
<span data-ttu-id="9da19-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9da19-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9da19-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9da19-124">-WhatIf</span></span>
<span data-ttu-id="9da19-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9da19-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9da19-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9da19-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9da19-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da19-127">CommonParameters</span></span>
<span data-ttu-id="9da19-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9da19-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da19-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9da19-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da19-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9da19-130">INPUTS</span></span>

### <span data-ttu-id="9da19-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="9da19-131">None</span></span>
<span data-ttu-id="9da19-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9da19-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9da19-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9da19-133">OUTPUTS</span></span>

## <span data-ttu-id="9da19-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9da19-134">NOTES</span></span>

## <span data-ttu-id="9da19-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9da19-135">RELATED LINKS</span></span>

[<span data-ttu-id="9da19-136">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="9da19-136">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="9da19-137">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="9da19-137">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)

[<span data-ttu-id="9da19-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="9da19-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


