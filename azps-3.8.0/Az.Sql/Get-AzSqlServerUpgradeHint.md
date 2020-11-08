---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: 841de793c6e0c6d9213be262576dbd4f407fd947
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088504"
---
# <span data-ttu-id="99045-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="99045-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="99045-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99045-102">SYNOPSIS</span></span>
<span data-ttu-id="99045-103">Hämtar pris nivå tips för uppgradering av en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="99045-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="99045-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99045-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99045-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99045-105">DESCRIPTION</span></span>
<span data-ttu-id="99045-106">Cmdleten **Get-AzSqlServerUpgradeHint** får pris nivå tips för uppgradering av en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="99045-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="99045-107">Tips kan innehålla den Elastic Database-poolen och fristående databas tips.</span><span class="sxs-lookup"><span data-stu-id="99045-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="99045-108">Databaser som fortfarande finns i webb-och företags pris nivåer är ett tips för att du ska kunna uppgradera till de nya grundläggande priser, standard-eller Premium-priserna eller att gå in i den Elastic Database-poolen.</span><span class="sxs-lookup"><span data-stu-id="99045-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="99045-109">Denna cmdlet returnerar tips för alla databaser som finns på den angivna servern.</span><span class="sxs-lookup"><span data-stu-id="99045-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="99045-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99045-110">EXAMPLES</span></span>

### <span data-ttu-id="99045-111">Exempel 1: få rekommendationer som kombineras</span><span class="sxs-lookup"><span data-stu-id="99045-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="99045-112">Med det här kommandot får du rekommendationer för alla databaser på en server med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="99045-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="99045-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99045-113">PARAMETERS</span></span>

### <span data-ttu-id="99045-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99045-114">-DefaultProfile</span></span>
<span data-ttu-id="99045-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="99045-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99045-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="99045-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="99045-117">Anger om databaser som ingår i Elastic Database-pooler ska returneras.</span><span class="sxs-lookup"><span data-stu-id="99045-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="99045-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99045-118">-ResourceGroupName</span></span>
<span data-ttu-id="99045-119">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="99045-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="99045-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="99045-120">-ServerName</span></span>
<span data-ttu-id="99045-121">Anger namnet på den server där denna cmdlet får ett uppgraderings tips.</span><span class="sxs-lookup"><span data-stu-id="99045-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="99045-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="99045-122">-Confirm</span></span>
<span data-ttu-id="99045-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="99045-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99045-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99045-124">-WhatIf</span></span>
<span data-ttu-id="99045-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="99045-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99045-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="99045-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99045-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99045-127">CommonParameters</span></span>
<span data-ttu-id="99045-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99045-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99045-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99045-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99045-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99045-130">INPUTS</span></span>

### <span data-ttu-id="99045-131">System. String</span><span class="sxs-lookup"><span data-stu-id="99045-131">System.String</span></span>

### <span data-ttu-id="99045-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99045-132">System.Boolean</span></span>

## <span data-ttu-id="99045-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99045-133">OUTPUTS</span></span>

### <span data-ttu-id="99045-134">Microsoft. Azure. commands. SQL. ServiceTierAdvisor. Model. UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="99045-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="99045-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99045-135">NOTES</span></span>

## <span data-ttu-id="99045-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99045-136">RELATED LINKS</span></span>

[<span data-ttu-id="99045-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="99045-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="99045-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="99045-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="99045-139">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="99045-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

