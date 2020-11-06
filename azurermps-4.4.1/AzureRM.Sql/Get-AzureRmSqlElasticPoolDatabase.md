---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: f2229fa904144b0dd95a054da95db99600963406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575779"
---
# <span data-ttu-id="abc5d-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="abc5d-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="abc5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abc5d-102">SYNOPSIS</span></span>
<span data-ttu-id="abc5d-103">Hämtar Elastic databases i en elastisk pool och deras egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="abc5d-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abc5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abc5d-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abc5d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abc5d-105">DESCRIPTION</span></span>
<span data-ttu-id="abc5d-106">Cmdleten **Get-AzureRmSqlElasticPoolDatabase** får Elastic databases i en elastisk pool och deras egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="abc5d-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="abc5d-107">Du kan ange namnet på en elastisk databas i Azure SQL Database för att Visa egenskaps värden för enbart den databasen.</span><span class="sxs-lookup"><span data-stu-id="abc5d-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="abc5d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abc5d-108">EXAMPLES</span></span>

### <span data-ttu-id="abc5d-109">Exempel 1: Hämta alla databaser i en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="abc5d-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="abc5d-110">Det här kommandot får alla databaser i en elastisk pool med namnet ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="abc5d-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="abc5d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abc5d-111">PARAMETERS</span></span>

### <span data-ttu-id="abc5d-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="abc5d-112">-DatabaseName</span></span>
<span data-ttu-id="abc5d-113">Anger namnet på den SQL-databas som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="abc5d-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="abc5d-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="abc5d-114">-ElasticPoolName</span></span>
<span data-ttu-id="abc5d-115">Anger namnet på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="abc5d-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="abc5d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abc5d-116">-ResourceGroupName</span></span>
<span data-ttu-id="abc5d-117">Anger namnet på en resurs grupp som den elastiska poolen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="abc5d-117">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="abc5d-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="abc5d-118">-ServerName</span></span>
<span data-ttu-id="abc5d-119">Anger namnet på en server som innehåller en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="abc5d-119">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="abc5d-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="abc5d-120">-Confirm</span></span>
<span data-ttu-id="abc5d-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="abc5d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc5d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc5d-122">-WhatIf</span></span>
<span data-ttu-id="abc5d-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="abc5d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abc5d-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="abc5d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc5d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc5d-125">-DefaultProfile</span></span>
<span data-ttu-id="abc5d-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="abc5d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abc5d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc5d-127">CommonParameters</span></span>
<span data-ttu-id="abc5d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abc5d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc5d-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abc5d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc5d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abc5d-130">INPUTS</span></span>

## <span data-ttu-id="abc5d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abc5d-131">OUTPUTS</span></span>

### <span data-ttu-id="abc5d-132">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="abc5d-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="abc5d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abc5d-133">NOTES</span></span>

## <span data-ttu-id="abc5d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abc5d-134">RELATED LINKS</span></span>

[<span data-ttu-id="abc5d-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="abc5d-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="abc5d-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="abc5d-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="abc5d-137">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="abc5d-137">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="abc5d-138">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="abc5d-138">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="abc5d-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="abc5d-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

