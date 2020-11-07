---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
ms.openlocfilehash: ebc9386df78af1a730578c57e3957a869bbc299b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928001"
---
# <span data-ttu-id="bf088-101">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bf088-101">Get-AzSqlElasticPool</span></span>

## <span data-ttu-id="bf088-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf088-102">SYNOPSIS</span></span>
<span data-ttu-id="bf088-103">Hämtar elastiska pooler och deras egenskaps värden i en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="bf088-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

## <span data-ttu-id="bf088-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf088-104">SYNTAX</span></span>

```
Get-AzSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf088-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf088-105">DESCRIPTION</span></span>
<span data-ttu-id="bf088-106">Cmdleten **Get-AzSqlElasticPool** får elastiska pooler och deras egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="bf088-106">The **Get-AzSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="bf088-107">Ange namnet på en befintlig elastisk pool för att Visa egenskapsvärdenas egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="bf088-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="bf088-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf088-108">EXAMPLES</span></span>

### <span data-ttu-id="bf088-109">Exempel 1: skaffa alla elastiska pooler</span><span class="sxs-lookup"><span data-stu-id="bf088-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="bf088-110">Det här kommandot får alla de elastiska poolerna på servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="bf088-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="bf088-111">Exempel 2: skaffa en specifik elastisk pool</span><span class="sxs-lookup"><span data-stu-id="bf088-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
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

<span data-ttu-id="bf088-112">Det här kommandot får den Elastic pool som heter ElasticPool0127 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="bf088-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="bf088-113">Exempel 3: få mått för en Azure SQL Elastic Database-adresspool</span><span class="sxs-lookup"><span data-stu-id="bf088-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-AzMetric -TimeGrain 0:5:0 -MetricName storage_percent
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

<span data-ttu-id="bf088-114">Det här kommandot returnerar Mät värden för en Azure SQL Elastic-databas som heter ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="bf088-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

### <span data-ttu-id="bf088-115">Exempel 4: Hämta alla elastiska pooler med filter-ElasticPoolName "ElasticPool \*"</span><span class="sxs-lookup"><span data-stu-id="bf088-115">Example 4: Get all elastic pools using filtering -ElasticPoolName "ElasticPool\*"</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="bf088-116">Det här kommandot får alla de elastiska poolerna på servern med namnet Server01 som börjar med "ElasticPool".</span><span class="sxs-lookup"><span data-stu-id="bf088-116">This command gets all of the elastic pools on the server named Server01 that start with "ElasticPool".</span></span>

## <span data-ttu-id="bf088-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf088-117">PARAMETERS</span></span>

### <span data-ttu-id="bf088-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf088-118">-DefaultProfile</span></span>
<span data-ttu-id="bf088-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bf088-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf088-120">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="bf088-120">-ElasticPoolName</span></span>
<span data-ttu-id="bf088-121">Anger namnet på den Elastic pool som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="bf088-121">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bf088-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf088-122">-ResourceGroupName</span></span>
<span data-ttu-id="bf088-123">Anger namnet på den resurs grupp som innehåller den Elastic pool som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="bf088-123">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bf088-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bf088-124">-ServerName</span></span>
<span data-ttu-id="bf088-125">Anger namnet på den server som innehåller den Elastic pool som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="bf088-125">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bf088-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf088-126">CommonParameters</span></span>
<span data-ttu-id="bf088-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf088-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf088-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf088-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf088-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf088-129">INPUTS</span></span>

### <span data-ttu-id="bf088-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bf088-130">System.String</span></span>

## <span data-ttu-id="bf088-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf088-131">OUTPUTS</span></span>

### <span data-ttu-id="bf088-132">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="bf088-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="bf088-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf088-133">NOTES</span></span>

## <span data-ttu-id="bf088-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf088-134">RELATED LINKS</span></span>

[<span data-ttu-id="bf088-135">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bf088-135">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="bf088-136">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bf088-136">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="bf088-137">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bf088-137">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


