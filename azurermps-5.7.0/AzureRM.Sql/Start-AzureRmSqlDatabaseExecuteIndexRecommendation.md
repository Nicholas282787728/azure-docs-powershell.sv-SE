---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ac5bf33bd87ff290784728fd0c4857d5278d3057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579268"
---
# <span data-ttu-id="f3dad-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="f3dad-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="f3dad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3dad-102">SYNOPSIS</span></span>
<span data-ttu-id="f3dad-103">Startar arbets flödet som kör en rekommenderad index åtgärd.</span><span class="sxs-lookup"><span data-stu-id="f3dad-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3dad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3dad-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3dad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3dad-105">DESCRIPTION</span></span>
<span data-ttu-id="f3dad-106">Cmdleten **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** startar arbets flödet som kör en rekommenderad index åtgärd för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="f3dad-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="f3dad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3dad-107">EXAMPLES</span></span>

### <span data-ttu-id="f3dad-108">Exempel 1: kör en index rekommendation</span><span class="sxs-lookup"><span data-stu-id="f3dad-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="f3dad-109">Det här kommandot kör en index rekommendation.</span><span class="sxs-lookup"><span data-stu-id="f3dad-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="f3dad-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3dad-110">PARAMETERS</span></span>

### <span data-ttu-id="f3dad-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f3dad-111">-DatabaseName</span></span>
<span data-ttu-id="f3dad-112">Anger namnet på den databas som den här cmdleten startar arbets flödet för.</span><span class="sxs-lookup"><span data-stu-id="f3dad-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3dad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3dad-113">-DefaultProfile</span></span>
<span data-ttu-id="f3dad-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f3dad-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3dad-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="f3dad-115">-IndexRecommendationName</span></span>
<span data-ttu-id="f3dad-116">Anger namnet på den index rekommendation som denna cmdlet kör.</span><span class="sxs-lookup"><span data-stu-id="f3dad-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3dad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3dad-117">-ResourceGroupName</span></span>
<span data-ttu-id="f3dad-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="f3dad-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f3dad-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f3dad-119">-ServerName</span></span>
<span data-ttu-id="f3dad-120">Anger den server som är värd för den databas som den här cmdleten startar ett arbets flöde för.</span><span class="sxs-lookup"><span data-stu-id="f3dad-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3dad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3dad-121">CommonParameters</span></span>
<span data-ttu-id="f3dad-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3dad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3dad-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3dad-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3dad-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3dad-124">INPUTS</span></span>

### <span data-ttu-id="f3dad-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="f3dad-125">None</span></span>
<span data-ttu-id="f3dad-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f3dad-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3dad-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3dad-127">OUTPUTS</span></span>

## <span data-ttu-id="f3dad-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3dad-128">NOTES</span></span>

## <span data-ttu-id="f3dad-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3dad-129">RELATED LINKS</span></span>

[<span data-ttu-id="f3dad-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="f3dad-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="f3dad-131">Stopp-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="f3dad-131">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="f3dad-132">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="f3dad-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


