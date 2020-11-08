---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: 91c23a32fd25c184e46249424b439375caed6ac5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920244"
---
# <span data-ttu-id="04705-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="04705-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="04705-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04705-102">SYNOPSIS</span></span>
<span data-ttu-id="04705-103">Hämtar databas operationernas status.</span><span class="sxs-lookup"><span data-stu-id="04705-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="04705-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04705-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04705-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04705-105">DESCRIPTION</span></span>
<span data-ttu-id="04705-106">Cmdleten **Get-AzSqlDatabaseActivity** får statusen för databas åtgärder i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="04705-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="04705-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04705-107">EXAMPLES</span></span>

### <span data-ttu-id="04705-108">Exempel 1: Hämta status för alla SQL Database-instanser</span><span class="sxs-lookup"><span data-stu-id="04705-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="04705-109">Det här kommandot returnerar status för alla SQL databas-instanser i en elastisk pool med namnet ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="04705-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="04705-110">Exempel 2: Hämta status för alla SQL-databas operationer</span><span class="sxs-lookup"><span data-stu-id="04705-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="04705-111">Det här kommandot returnerar statusen för alla SQL-databas operationer i en databas.</span><span class="sxs-lookup"><span data-stu-id="04705-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="04705-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04705-112">PARAMETERS</span></span>

### <span data-ttu-id="04705-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="04705-113">-DatabaseName</span></span>
<span data-ttu-id="04705-114">Anger namnet på den databas där denna cmdlet får status.</span><span class="sxs-lookup"><span data-stu-id="04705-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="04705-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04705-115">-DefaultProfile</span></span>
<span data-ttu-id="04705-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04705-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04705-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="04705-117">-ElasticPoolName</span></span>
<span data-ttu-id="04705-118">Anger namnet på den Elastic Database-pool för vilken denna cmdlet får status.</span><span class="sxs-lookup"><span data-stu-id="04705-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="04705-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="04705-119">-OperationId</span></span>
<span data-ttu-id="04705-120">Anger ID för den operation som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="04705-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04705-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04705-121">-ResourceGroupName</span></span>
<span data-ttu-id="04705-122">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="04705-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="04705-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="04705-123">-ServerName</span></span>
<span data-ttu-id="04705-124">Anger namnet på den Microsoft SQL Server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="04705-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="04705-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="04705-125">-Confirm</span></span>
<span data-ttu-id="04705-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04705-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04705-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04705-127">-WhatIf</span></span>
<span data-ttu-id="04705-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="04705-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04705-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="04705-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04705-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04705-130">CommonParameters</span></span>
<span data-ttu-id="04705-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04705-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04705-132">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04705-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04705-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04705-133">INPUTS</span></span>

### <span data-ttu-id="04705-134">System. String</span><span class="sxs-lookup"><span data-stu-id="04705-134">System.String</span></span>

### <span data-ttu-id="04705-135">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="04705-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="04705-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04705-136">OUTPUTS</span></span>

### <span data-ttu-id="04705-137">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="04705-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="04705-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04705-138">NOTES</span></span>

## <span data-ttu-id="04705-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04705-139">RELATED LINKS</span></span>