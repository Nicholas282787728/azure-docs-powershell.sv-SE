---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 2922edf4f7b7cfd0d814a5559bb1e6e7bb9ef3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576021"
---
# <span data-ttu-id="6c5cb-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6c5cb-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="6c5cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5cb-103">Stoppar arbets flödet som kör en rekommenderad index åtgärd.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c5cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c5cb-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c5cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c5cb-105">DESCRIPTION</span></span>
<span data-ttu-id="6c5cb-106">Cmdleten **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** stoppar arbets flödet som kör en rekommenderad index åtgärd.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="6c5cb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c5cb-107">EXAMPLES</span></span>

### <span data-ttu-id="6c5cb-108">Exempel 1: sluta köra en index rekommendation</span><span class="sxs-lookup"><span data-stu-id="6c5cb-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="6c5cb-109">Det här kommandot slutar använda en index rekommendation.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="6c5cb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c5cb-110">PARAMETERS</span></span>

### <span data-ttu-id="6c5cb-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6c5cb-111">-DatabaseName</span></span>
<span data-ttu-id="6c5cb-112">Anger namnet på den databas där denna cmdlet stoppar arbets flödet.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="6c5cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5cb-113">-DefaultProfile</span></span>
<span data-ttu-id="6c5cb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6c5cb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c5cb-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="6c5cb-115">-IndexRecommendationName</span></span>
<span data-ttu-id="6c5cb-116">Anger namnet på den index rekommendation som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="6c5cb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c5cb-117">-ResourceGroupName</span></span>
<span data-ttu-id="6c5cb-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="6c5cb-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6c5cb-119">-ServerName</span></span>
<span data-ttu-id="6c5cb-120">Anger den server som är värd för den databas som den här cmdleten stoppar ett arbets flöde för.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="6c5cb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5cb-121">CommonParameters</span></span>
<span data-ttu-id="6c5cb-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c5cb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5cb-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c5cb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5cb-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c5cb-124">INPUTS</span></span>

### <span data-ttu-id="6c5cb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6c5cb-125">System.String</span></span>

## <span data-ttu-id="6c5cb-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c5cb-126">OUTPUTS</span></span>

### <span data-ttu-id="6c5cb-127">Microsoft. Azure. commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6c5cb-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="6c5cb-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c5cb-128">NOTES</span></span>

## <span data-ttu-id="6c5cb-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c5cb-129">RELATED LINKS</span></span>

[<span data-ttu-id="6c5cb-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="6c5cb-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="6c5cb-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6c5cb-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="6c5cb-132">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="6c5cb-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


