---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: d4cb344f63b871f55668c4de7205ada80ff04f35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756437"
---
# <span data-ttu-id="3b814-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="3b814-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="3b814-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b814-102">SYNOPSIS</span></span>
<span data-ttu-id="3b814-103">Stoppar arbets flödet som kör en rekommenderad index åtgärd.</span><span class="sxs-lookup"><span data-stu-id="3b814-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b814-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b814-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b814-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b814-105">DESCRIPTION</span></span>
<span data-ttu-id="3b814-106">Cmdleten **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** stoppar arbets flödet som kör en rekommenderad index åtgärd.</span><span class="sxs-lookup"><span data-stu-id="3b814-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="3b814-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b814-107">EXAMPLES</span></span>

### <span data-ttu-id="3b814-108">Exempel 1: sluta köra en index rekommendation</span><span class="sxs-lookup"><span data-stu-id="3b814-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="3b814-109">Det här kommandot slutar använda en index rekommendation.</span><span class="sxs-lookup"><span data-stu-id="3b814-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="3b814-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b814-110">PARAMETERS</span></span>

### <span data-ttu-id="3b814-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3b814-111">-DatabaseName</span></span>
<span data-ttu-id="3b814-112">Anger namnet på den databas där denna cmdlet stoppar arbets flödet.</span><span class="sxs-lookup"><span data-stu-id="3b814-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="3b814-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b814-113">-DefaultProfile</span></span>
<span data-ttu-id="3b814-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3b814-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b814-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="3b814-115">-IndexRecommendationName</span></span>
<span data-ttu-id="3b814-116">Anger namnet på den index rekommendation som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="3b814-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="3b814-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b814-117">-ResourceGroupName</span></span>
<span data-ttu-id="3b814-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="3b814-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="3b814-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3b814-119">-ServerName</span></span>
<span data-ttu-id="3b814-120">Anger den server som är värd för den databas som den här cmdleten stoppar ett arbets flöde för.</span><span class="sxs-lookup"><span data-stu-id="3b814-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="3b814-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b814-121">CommonParameters</span></span>
<span data-ttu-id="3b814-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b814-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b814-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b814-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b814-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b814-124">INPUTS</span></span>

### <span data-ttu-id="3b814-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="3b814-125">None</span></span>
<span data-ttu-id="3b814-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3b814-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b814-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b814-127">OUTPUTS</span></span>

## <span data-ttu-id="3b814-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b814-128">NOTES</span></span>

## <span data-ttu-id="3b814-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b814-129">RELATED LINKS</span></span>

[<span data-ttu-id="3b814-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="3b814-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="3b814-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="3b814-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="3b814-132">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="3b814-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


