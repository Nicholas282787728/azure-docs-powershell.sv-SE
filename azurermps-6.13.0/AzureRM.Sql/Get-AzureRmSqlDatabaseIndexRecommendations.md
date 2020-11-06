---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseindexrecommendations
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
ms.openlocfilehash: 9180b89e54f84d2b457de79c400b7d6aa8259d28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576753"
---
# <span data-ttu-id="7cba9-101">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="7cba9-101">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>

## <span data-ttu-id="7cba9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7cba9-102">SYNOPSIS</span></span>
<span data-ttu-id="7cba9-103">Hämtar de rekommenderade index åtgärderna för en server eller en databas.</span><span class="sxs-lookup"><span data-stu-id="7cba9-103">Gets the recommended index operations for a server or database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cba9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7cba9-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseIndexRecommendations -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cba9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7cba9-105">DESCRIPTION</span></span>
<span data-ttu-id="7cba9-106">Cmdleten **Get-AzureRmSqlDatabaseIndexRecommendations** får de rekommenderade index åtgärderna för en Azure SQL Database-Server eller-databas.</span><span class="sxs-lookup"><span data-stu-id="7cba9-106">The **Get-AzureRmSqlDatabaseIndexRecommendations** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="7cba9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7cba9-107">EXAMPLES</span></span>

### <span data-ttu-id="7cba9-108">Exempel 1: få index rekommendationer för alla databaser på servern</span><span class="sxs-lookup"><span data-stu-id="7cba9-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="7cba9-109">Det här kommandot returnerar index rekommendationer för alla databaser på servern Server01.</span><span class="sxs-lookup"><span data-stu-id="7cba9-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="7cba9-110">Exempel 2: Hämta index rekommendationer för en viss databas</span><span class="sxs-lookup"><span data-stu-id="7cba9-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="7cba9-111">Det här kommandot returnerar index rekommendationer för en viss databas.</span><span class="sxs-lookup"><span data-stu-id="7cba9-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="7cba9-112">Exempel 3: få en enda index rekommendation efter namn</span><span class="sxs-lookup"><span data-stu-id="7cba9-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="7cba9-113">Det här kommandot returnerar en enkel index rekommendation efter namn.</span><span class="sxs-lookup"><span data-stu-id="7cba9-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="7cba9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7cba9-114">PARAMETERS</span></span>

### <span data-ttu-id="7cba9-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7cba9-115">-DatabaseName</span></span>
<span data-ttu-id="7cba9-116">Anger namnet på den databas som den här cmdleten får index rekommendationer för.</span><span class="sxs-lookup"><span data-stu-id="7cba9-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="7cba9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cba9-117">-DefaultProfile</span></span>
<span data-ttu-id="7cba9-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7cba9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cba9-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="7cba9-119">-IndexRecommendationName</span></span>
<span data-ttu-id="7cba9-120">Anger namnet på den index rekommendation som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="7cba9-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7cba9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cba9-121">-ResourceGroupName</span></span>
<span data-ttu-id="7cba9-122">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="7cba9-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="7cba9-123">Denna cmdlet hämtar index rekommendationer för en databas som finns på den här servern.</span><span class="sxs-lookup"><span data-stu-id="7cba9-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="7cba9-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7cba9-124">-ServerName</span></span>
<span data-ttu-id="7cba9-125">Anger den server som är värd för den databas som den här cmdleten får index rekommendationer för.</span><span class="sxs-lookup"><span data-stu-id="7cba9-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="7cba9-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="7cba9-126">-TableName</span></span>
<span data-ttu-id="7cba9-127">Anger namnet på en Azure SQL-tabell.</span><span class="sxs-lookup"><span data-stu-id="7cba9-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="7cba9-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7cba9-128">-Confirm</span></span>
<span data-ttu-id="7cba9-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7cba9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cba9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cba9-130">-WhatIf</span></span>
<span data-ttu-id="7cba9-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7cba9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cba9-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7cba9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cba9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cba9-133">CommonParameters</span></span>
<span data-ttu-id="7cba9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cba9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cba9-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cba9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cba9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7cba9-136">INPUTS</span></span>

### <span data-ttu-id="7cba9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7cba9-137">System.String</span></span>

## <span data-ttu-id="7cba9-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7cba9-138">OUTPUTS</span></span>

### <span data-ttu-id="7cba9-139">Microsoft. Azure. commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7cba9-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="7cba9-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7cba9-140">NOTES</span></span>

## <span data-ttu-id="7cba9-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7cba9-141">RELATED LINKS</span></span>

[<span data-ttu-id="7cba9-142">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7cba9-142">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="7cba9-143">Stopp-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7cba9-143">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)
