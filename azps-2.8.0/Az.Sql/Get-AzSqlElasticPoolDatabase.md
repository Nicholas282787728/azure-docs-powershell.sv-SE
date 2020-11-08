---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: f03d172db1a4e8952fea989499f1689d9e0b6a83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920462"
---
# <span data-ttu-id="76631-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="76631-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="76631-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76631-102">SYNOPSIS</span></span>
<span data-ttu-id="76631-103">Hämtar Elastic databases i en elastisk pool och deras egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="76631-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="76631-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76631-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76631-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76631-105">DESCRIPTION</span></span>
<span data-ttu-id="76631-106">Cmdleten **Get-AzSqlElasticPoolDatabase** får Elastic databases i en elastisk pool och deras egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="76631-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="76631-107">Du kan ange namnet på en elastisk databas i Azure SQL Database för att Visa egenskaps värden för enbart den databasen.</span><span class="sxs-lookup"><span data-stu-id="76631-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="76631-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76631-108">EXAMPLES</span></span>

### <span data-ttu-id="76631-109">Exempel 1: Hämta alla databaser i en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="76631-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="76631-110">Det här kommandot får alla databaser i en elastisk pool med namnet ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="76631-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="76631-111">Exempel 2: Hämta alla databaser i en elastisk pool med filter</span><span class="sxs-lookup"><span data-stu-id="76631-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="76631-112">Det här kommandot får alla databaser i en elastisk pool med namnet ElasticPool01 som börjar med "databas".</span><span class="sxs-lookup"><span data-stu-id="76631-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="76631-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76631-113">PARAMETERS</span></span>

### <span data-ttu-id="76631-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="76631-114">-DatabaseName</span></span>
<span data-ttu-id="76631-115">Anger namnet på den SQL-databas som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="76631-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="76631-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76631-116">-DefaultProfile</span></span>
<span data-ttu-id="76631-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="76631-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76631-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="76631-118">-ElasticPoolName</span></span>
<span data-ttu-id="76631-119">Anger namnet på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="76631-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="76631-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76631-120">-ResourceGroupName</span></span>
<span data-ttu-id="76631-121">Anger namnet på en resurs grupp som den elastiska poolen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="76631-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="76631-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="76631-122">-ServerName</span></span>
<span data-ttu-id="76631-123">Anger namnet på en server som innehåller en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="76631-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="76631-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="76631-124">-Confirm</span></span>
<span data-ttu-id="76631-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="76631-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76631-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76631-126">-WhatIf</span></span>
<span data-ttu-id="76631-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="76631-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76631-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="76631-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76631-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76631-129">CommonParameters</span></span>
<span data-ttu-id="76631-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76631-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76631-131">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76631-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76631-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76631-132">INPUTS</span></span>

### <span data-ttu-id="76631-133">System. String</span><span class="sxs-lookup"><span data-stu-id="76631-133">System.String</span></span>

## <span data-ttu-id="76631-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76631-134">OUTPUTS</span></span>

### <span data-ttu-id="76631-135">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="76631-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="76631-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76631-136">NOTES</span></span>

## <span data-ttu-id="76631-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76631-137">RELATED LINKS</span></span>

[<span data-ttu-id="76631-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="76631-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="76631-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="76631-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="76631-140">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="76631-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="76631-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="76631-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="76631-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="76631-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)
