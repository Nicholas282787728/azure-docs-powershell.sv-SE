---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ae4564b1f583b8057438ee631de6b13d38e008ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757440"
---
# <span data-ttu-id="f65a2-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="f65a2-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="f65a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f65a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f65a2-103">Startar arbets flödet som kör en rekommenderad index åtgärd.</span><span class="sxs-lookup"><span data-stu-id="f65a2-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f65a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f65a2-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f65a2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f65a2-105">DESCRIPTION</span></span>
<span data-ttu-id="f65a2-106">Cmdleten **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** startar arbets flödet som kör en rekommenderad index åtgärd för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="f65a2-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="f65a2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f65a2-107">EXAMPLES</span></span>

### <span data-ttu-id="f65a2-108">Exempel 1: kör en index rekommendation</span><span class="sxs-lookup"><span data-stu-id="f65a2-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="f65a2-109">Det här kommandot kör en index rekommendation.</span><span class="sxs-lookup"><span data-stu-id="f65a2-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="f65a2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f65a2-110">PARAMETERS</span></span>

### <span data-ttu-id="f65a2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f65a2-111">-DatabaseName</span></span>
<span data-ttu-id="f65a2-112">Anger namnet på den databas som den här cmdleten startar arbets flödet för.</span><span class="sxs-lookup"><span data-stu-id="f65a2-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="f65a2-113">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="f65a2-113">-IndexRecommendationName</span></span>
<span data-ttu-id="f65a2-114">Anger namnet på den index rekommendation som denna cmdlet kör.</span><span class="sxs-lookup"><span data-stu-id="f65a2-114">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="f65a2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f65a2-115">-ResourceGroupName</span></span>
<span data-ttu-id="f65a2-116">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="f65a2-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f65a2-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f65a2-117">-ServerName</span></span>
<span data-ttu-id="f65a2-118">Anger den server som är värd för den databas som den här cmdleten startar ett arbets flöde för.</span><span class="sxs-lookup"><span data-stu-id="f65a2-118">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="f65a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f65a2-119">-DefaultProfile</span></span>
<span data-ttu-id="f65a2-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f65a2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f65a2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f65a2-121">CommonParameters</span></span>
<span data-ttu-id="f65a2-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f65a2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f65a2-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f65a2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f65a2-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f65a2-124">INPUTS</span></span>

## <span data-ttu-id="f65a2-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f65a2-125">OUTPUTS</span></span>

## <span data-ttu-id="f65a2-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f65a2-126">NOTES</span></span>

## <span data-ttu-id="f65a2-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f65a2-127">RELATED LINKS</span></span>

[<span data-ttu-id="f65a2-128">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="f65a2-128">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="f65a2-129">Stopp-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="f65a2-129">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="f65a2-130">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="f65a2-130">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


