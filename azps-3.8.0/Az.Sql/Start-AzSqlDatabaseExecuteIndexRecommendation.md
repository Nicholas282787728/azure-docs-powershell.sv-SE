---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: e69cffe6955a5bf19636dd519c0906be64ce4413
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927105"
---
# <span data-ttu-id="6f709-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6f709-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="6f709-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f709-102">SYNOPSIS</span></span>
<span data-ttu-id="6f709-103">Startar arbets flödet som kör en rekommenderad index åtgärd.</span><span class="sxs-lookup"><span data-stu-id="6f709-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="6f709-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f709-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f709-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f709-105">DESCRIPTION</span></span>
<span data-ttu-id="6f709-106">Cmdleten **Start-AzSqlDatabaseExecuteIndexRecommendation** startar arbets flödet som kör en rekommenderad index åtgärd för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="6f709-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="6f709-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f709-107">EXAMPLES</span></span>

### <span data-ttu-id="6f709-108">Exempel 1: kör en index rekommendation</span><span class="sxs-lookup"><span data-stu-id="6f709-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="6f709-109">Det här kommandot kör en index rekommendation.</span><span class="sxs-lookup"><span data-stu-id="6f709-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="6f709-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f709-110">PARAMETERS</span></span>

### <span data-ttu-id="6f709-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6f709-111">-DatabaseName</span></span>
<span data-ttu-id="6f709-112">Anger namnet på den databas som den här cmdleten startar arbets flödet för.</span><span class="sxs-lookup"><span data-stu-id="6f709-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f709-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f709-113">-DefaultProfile</span></span>
<span data-ttu-id="6f709-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6f709-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f709-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="6f709-115">-IndexRecommendationName</span></span>
<span data-ttu-id="6f709-116">Anger namnet på den index rekommendation som denna cmdlet kör.</span><span class="sxs-lookup"><span data-stu-id="6f709-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f709-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f709-117">-ResourceGroupName</span></span>
<span data-ttu-id="6f709-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="6f709-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="6f709-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6f709-119">-ServerName</span></span>
<span data-ttu-id="6f709-120">Anger den server som är värd för den databas som den här cmdleten startar ett arbets flöde för.</span><span class="sxs-lookup"><span data-stu-id="6f709-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f709-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f709-121">CommonParameters</span></span>
<span data-ttu-id="6f709-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f709-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f709-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f709-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f709-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f709-124">INPUTS</span></span>

### <span data-ttu-id="6f709-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6f709-125">System.String</span></span>

## <span data-ttu-id="6f709-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f709-126">OUTPUTS</span></span>

### <span data-ttu-id="6f709-127">Microsoft. Azure. commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6f709-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="6f709-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f709-128">NOTES</span></span>

## <span data-ttu-id="6f709-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f709-129">RELATED LINKS</span></span>

[<span data-ttu-id="6f709-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6f709-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="6f709-131">Stopp-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6f709-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="6f709-132">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="6f709-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

