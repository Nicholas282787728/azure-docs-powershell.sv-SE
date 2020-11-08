---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ca7aeed13627bba3c380b3f1062ee80fcc7c3ebf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927074"
---
# <span data-ttu-id="19896-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="19896-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="19896-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19896-102">SYNOPSIS</span></span>
<span data-ttu-id="19896-103">Stoppar arbets flödet som kör en rekommenderad index åtgärd.</span><span class="sxs-lookup"><span data-stu-id="19896-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="19896-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19896-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19896-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19896-105">DESCRIPTION</span></span>
<span data-ttu-id="19896-106">Cmdleten **Stop-AzSqlDatabaseExecuteIndexRecommendation** stoppar arbets flödet som kör en rekommenderad index åtgärd.</span><span class="sxs-lookup"><span data-stu-id="19896-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="19896-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19896-107">EXAMPLES</span></span>

### <span data-ttu-id="19896-108">Exempel 1: sluta köra en index rekommendation</span><span class="sxs-lookup"><span data-stu-id="19896-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="19896-109">Det här kommandot slutar använda en index rekommendation.</span><span class="sxs-lookup"><span data-stu-id="19896-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="19896-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19896-110">PARAMETERS</span></span>

### <span data-ttu-id="19896-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="19896-111">-DatabaseName</span></span>
<span data-ttu-id="19896-112">Anger namnet på den databas där denna cmdlet stoppar arbets flödet.</span><span class="sxs-lookup"><span data-stu-id="19896-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="19896-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19896-113">-DefaultProfile</span></span>
<span data-ttu-id="19896-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="19896-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19896-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="19896-115">-IndexRecommendationName</span></span>
<span data-ttu-id="19896-116">Anger namnet på den index rekommendation som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="19896-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="19896-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19896-117">-ResourceGroupName</span></span>
<span data-ttu-id="19896-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="19896-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="19896-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="19896-119">-ServerName</span></span>
<span data-ttu-id="19896-120">Anger den server som är värd för den databas som den här cmdleten stoppar ett arbets flöde för.</span><span class="sxs-lookup"><span data-stu-id="19896-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="19896-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19896-121">CommonParameters</span></span>
<span data-ttu-id="19896-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19896-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19896-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19896-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19896-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19896-124">INPUTS</span></span>

### <span data-ttu-id="19896-125">System. String</span><span class="sxs-lookup"><span data-stu-id="19896-125">System.String</span></span>

## <span data-ttu-id="19896-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19896-126">OUTPUTS</span></span>

### <span data-ttu-id="19896-127">Microsoft. Azure. commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="19896-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="19896-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19896-128">NOTES</span></span>

## <span data-ttu-id="19896-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19896-129">RELATED LINKS</span></span>

[<span data-ttu-id="19896-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="19896-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="19896-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="19896-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="19896-132">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="19896-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

