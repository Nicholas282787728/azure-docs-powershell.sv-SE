---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: 3068b3a406414eb7302d76d5d053658dcf0e6245
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756061"
---
# <span data-ttu-id="177b2-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="177b2-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="177b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="177b2-102">SYNOPSIS</span></span>
<span data-ttu-id="177b2-103">Hämtar Elastic databases i en elastisk pool och deras egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="177b2-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="177b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="177b2-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="177b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="177b2-105">DESCRIPTION</span></span>
<span data-ttu-id="177b2-106">Cmdleten **Get-AzureRmSqlElasticPoolDatabase** får Elastic databases i en elastisk pool och deras egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="177b2-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="177b2-107">Du kan ange namnet på en elastisk databas i Azure SQL Database för att Visa egenskaps värden för enbart den databasen.</span><span class="sxs-lookup"><span data-stu-id="177b2-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="177b2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="177b2-108">EXAMPLES</span></span>

### <span data-ttu-id="177b2-109">Exempel 1: Hämta alla databaser i en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="177b2-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="177b2-110">Det här kommandot får alla databaser i en elastisk pool med namnet ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="177b2-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="177b2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="177b2-111">PARAMETERS</span></span>

### <span data-ttu-id="177b2-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="177b2-112">-DatabaseName</span></span>
<span data-ttu-id="177b2-113">Anger namnet på den SQL-databas som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="177b2-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="177b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="177b2-114">-DefaultProfile</span></span>
<span data-ttu-id="177b2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="177b2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="177b2-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="177b2-116">-ElasticPoolName</span></span>
<span data-ttu-id="177b2-117">Anger namnet på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="177b2-117">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="177b2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="177b2-118">-ResourceGroupName</span></span>
<span data-ttu-id="177b2-119">Anger namnet på en resurs grupp som den elastiska poolen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="177b2-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="177b2-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="177b2-120">-ServerName</span></span>
<span data-ttu-id="177b2-121">Anger namnet på en server som innehåller en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="177b2-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="177b2-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="177b2-122">-Confirm</span></span>
<span data-ttu-id="177b2-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="177b2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="177b2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="177b2-124">-WhatIf</span></span>
<span data-ttu-id="177b2-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="177b2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="177b2-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="177b2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="177b2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="177b2-127">CommonParameters</span></span>
<span data-ttu-id="177b2-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="177b2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="177b2-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="177b2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="177b2-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="177b2-130">INPUTS</span></span>

### <span data-ttu-id="177b2-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="177b2-131">None</span></span>
<span data-ttu-id="177b2-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="177b2-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="177b2-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="177b2-133">OUTPUTS</span></span>

### <span data-ttu-id="177b2-134">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="177b2-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="177b2-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="177b2-135">NOTES</span></span>

## <span data-ttu-id="177b2-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="177b2-136">RELATED LINKS</span></span>

[<span data-ttu-id="177b2-137">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="177b2-137">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="177b2-138">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="177b2-138">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="177b2-139">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="177b2-139">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="177b2-140">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="177b2-140">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="177b2-141">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="177b2-141">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

