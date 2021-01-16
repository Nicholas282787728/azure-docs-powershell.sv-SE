---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 9dd14e1f8b61978575501700346157d7c22c0111
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402155"
---
# <span data-ttu-id="a001a-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="a001a-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="a001a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a001a-102">SYNOPSIS</span></span>
<span data-ttu-id="a001a-103">Hämtar de rekommenderade index åtgärderna för en server eller en databas.</span><span class="sxs-lookup"><span data-stu-id="a001a-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="a001a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a001a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a001a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a001a-105">DESCRIPTION</span></span>
<span data-ttu-id="a001a-106">Cmdleten **Get-AzSqlDatabaseIndexRecommendation** får de rekommenderade index åtgärderna för en Azure SQL Database-Server eller-databas.</span><span class="sxs-lookup"><span data-stu-id="a001a-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="a001a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a001a-107">EXAMPLES</span></span>

### <span data-ttu-id="a001a-108">Exempel 1: få index rekommendationer för alla databaser på servern</span><span class="sxs-lookup"><span data-stu-id="a001a-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="a001a-109">Det här kommandot returnerar index rekommendationer för alla databaser på servern Server01.</span><span class="sxs-lookup"><span data-stu-id="a001a-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="a001a-110">Exempel 2: Hämta index rekommendationer för en viss databas</span><span class="sxs-lookup"><span data-stu-id="a001a-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a001a-111">Det här kommandot returnerar index rekommendationer för en viss databas.</span><span class="sxs-lookup"><span data-stu-id="a001a-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="a001a-112">Exempel 3: få en enda index rekommendation efter namn</span><span class="sxs-lookup"><span data-stu-id="a001a-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="a001a-113">Det här kommandot returnerar en enkel index rekommendation efter namn.</span><span class="sxs-lookup"><span data-stu-id="a001a-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="a001a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a001a-114">PARAMETERS</span></span>

### <span data-ttu-id="a001a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a001a-115">-DatabaseName</span></span>
<span data-ttu-id="a001a-116">Anger namnet på den databas som den här cmdleten får index rekommendationer för.</span><span class="sxs-lookup"><span data-stu-id="a001a-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="a001a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a001a-117">-DefaultProfile</span></span>
<span data-ttu-id="a001a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a001a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a001a-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="a001a-119">-IndexRecommendationName</span></span>
<span data-ttu-id="a001a-120">Anger namnet på den index rekommendation som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="a001a-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a001a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a001a-121">-ResourceGroupName</span></span>
<span data-ttu-id="a001a-122">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="a001a-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="a001a-123">Denna cmdlet hämtar index rekommendationer för en databas som finns på den här servern.</span><span class="sxs-lookup"><span data-stu-id="a001a-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="a001a-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a001a-124">-ServerName</span></span>
<span data-ttu-id="a001a-125">Anger den server som är värd för den databas som den här cmdleten får index rekommendationer för.</span><span class="sxs-lookup"><span data-stu-id="a001a-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="a001a-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="a001a-126">-TableName</span></span>
<span data-ttu-id="a001a-127">Anger namnet på en Azure SQL-tabell.</span><span class="sxs-lookup"><span data-stu-id="a001a-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="a001a-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a001a-128">-Confirm</span></span>
<span data-ttu-id="a001a-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a001a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a001a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a001a-130">-WhatIf</span></span>
<span data-ttu-id="a001a-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a001a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a001a-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a001a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a001a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a001a-133">CommonParameters</span></span>
<span data-ttu-id="a001a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a001a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a001a-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a001a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a001a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a001a-136">INPUTS</span></span>

### <span data-ttu-id="a001a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a001a-137">System.String</span></span>

## <span data-ttu-id="a001a-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a001a-138">OUTPUTS</span></span>

### <span data-ttu-id="a001a-139">Microsoft. Azure. commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="a001a-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="a001a-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a001a-140">NOTES</span></span>

## <span data-ttu-id="a001a-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a001a-141">RELATED LINKS</span></span>

[<span data-ttu-id="a001a-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="a001a-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="a001a-143">Stopp-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="a001a-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
