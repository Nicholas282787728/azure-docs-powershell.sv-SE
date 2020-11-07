---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
ms.openlocfilehash: e40510745ea7de39df4e15d0b1be7516d0fb33ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581611"
---
# <span data-ttu-id="c3a26-101">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c3a26-101">Get-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="c3a26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3a26-102">SYNOPSIS</span></span>
<span data-ttu-id="c3a26-103">Hämtar elastiska pooler och deras egenskaps värden i en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="c3a26-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3a26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3a26-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3a26-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3a26-105">DESCRIPTION</span></span>
<span data-ttu-id="c3a26-106">Cmdleten **Get-AzureRmSqlElasticPool** får elastiska pooler och deras egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="c3a26-106">The **Get-AzureRmSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="c3a26-107">Ange namnet på en befintlig elastisk pool för att Visa egenskapsvärdenas egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="c3a26-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="c3a26-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3a26-108">EXAMPLES</span></span>

### <span data-ttu-id="c3a26-109">Exempel 1: skaffa alla elastiska pooler</span><span class="sxs-lookup"><span data-stu-id="c3a26-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="c3a26-110">Det här kommandot får alla de elastiska poolerna på servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="c3a26-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="c3a26-111">Exempel 2: skaffa en specifik elastisk pool</span><span class="sxs-lookup"><span data-stu-id="c3a26-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="c3a26-112">Det här kommandot får den Elastic pool som heter ElasticPool0127 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="c3a26-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="c3a26-113">Exempel 3: få mått för en Azure SQL Elastic Database-adresspool</span><span class="sxs-lookup"><span data-stu-id="c3a26-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-Metrics -TimeGrain 0:5:0
DimensionName  : 
DimensionValue : 
Name           : cpu_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : physical_data_read_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : log_write_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : dtu_consumption_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : storage_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent
```

<span data-ttu-id="c3a26-114">Det här kommandot returnerar Mät värden för en Azure SQL Elastic-databas som heter ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="c3a26-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

## <span data-ttu-id="c3a26-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3a26-115">PARAMETERS</span></span>

### <span data-ttu-id="c3a26-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3a26-116">-DefaultProfile</span></span>
<span data-ttu-id="c3a26-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c3a26-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3a26-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c3a26-118">-ElasticPoolName</span></span>
<span data-ttu-id="c3a26-119">Anger namnet på den Elastic pool som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="c3a26-119">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3a26-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3a26-120">-ResourceGroupName</span></span>
<span data-ttu-id="c3a26-121">Anger namnet på den resurs grupp som innehåller den Elastic pool som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="c3a26-121">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c3a26-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c3a26-122">-ServerName</span></span>
<span data-ttu-id="c3a26-123">Anger namnet på den server som innehåller den Elastic pool som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="c3a26-123">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c3a26-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3a26-124">CommonParameters</span></span>
<span data-ttu-id="c3a26-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3a26-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3a26-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3a26-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3a26-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3a26-127">INPUTS</span></span>

### <span data-ttu-id="c3a26-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c3a26-128">System.String</span></span>

## <span data-ttu-id="c3a26-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3a26-129">OUTPUTS</span></span>

### <span data-ttu-id="c3a26-130">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="c3a26-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="c3a26-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3a26-131">NOTES</span></span>

## <span data-ttu-id="c3a26-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3a26-132">RELATED LINKS</span></span>

[<span data-ttu-id="c3a26-133">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c3a26-133">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="c3a26-134">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c3a26-134">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="c3a26-135">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c3a26-135">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

