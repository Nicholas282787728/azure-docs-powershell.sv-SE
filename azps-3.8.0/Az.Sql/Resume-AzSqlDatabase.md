---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: a31a77f4e0780b5100018962b3475a0dffa97d9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088602"
---
# <span data-ttu-id="71fc7-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="71fc7-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="71fc7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71fc7-102">SYNOPSIS</span></span>
<span data-ttu-id="71fc7-103">Återupptar en SQL Data Warehouse-databas.</span><span class="sxs-lookup"><span data-stu-id="71fc7-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="71fc7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71fc7-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71fc7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71fc7-105">DESCRIPTION</span></span>
<span data-ttu-id="71fc7-106">Cmdleten **Resume-AzSqlDatabase** återupptar en Azure SQL Data Warehouse-databas.</span><span class="sxs-lookup"><span data-stu-id="71fc7-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="71fc7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71fc7-107">EXAMPLES</span></span>

### <span data-ttu-id="71fc7-108">Exempel 1: återupptar en Azure SQL Data Warehouse-databas</span><span class="sxs-lookup"><span data-stu-id="71fc7-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="71fc7-109">Det här kommandot återupptar en upplåst Azure SQL Data Warehouse-databas.</span><span class="sxs-lookup"><span data-stu-id="71fc7-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="71fc7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71fc7-110">PARAMETERS</span></span>

### <span data-ttu-id="71fc7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71fc7-111">-AsJob</span></span>
<span data-ttu-id="71fc7-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="71fc7-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71fc7-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="71fc7-113">-DatabaseName</span></span>
<span data-ttu-id="71fc7-114">Anger namnet på den databas som denna cmdlet fortsätter.</span><span class="sxs-lookup"><span data-stu-id="71fc7-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="71fc7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71fc7-115">-DefaultProfile</span></span>
<span data-ttu-id="71fc7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="71fc7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71fc7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71fc7-117">-ResourceGroupName</span></span>
<span data-ttu-id="71fc7-118">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="71fc7-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="71fc7-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71fc7-119">-ServerName</span></span>
<span data-ttu-id="71fc7-120">Anger namnet på den server som är värd för databasen som denna cmdlet fortsätter.</span><span class="sxs-lookup"><span data-stu-id="71fc7-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="71fc7-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="71fc7-121">-Confirm</span></span>
<span data-ttu-id="71fc7-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71fc7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71fc7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71fc7-123">-WhatIf</span></span>
<span data-ttu-id="71fc7-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="71fc7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71fc7-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="71fc7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71fc7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71fc7-126">CommonParameters</span></span>
<span data-ttu-id="71fc7-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71fc7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71fc7-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71fc7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71fc7-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71fc7-129">INPUTS</span></span>

### <span data-ttu-id="71fc7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="71fc7-130">System.String</span></span>

## <span data-ttu-id="71fc7-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71fc7-131">OUTPUTS</span></span>

### <span data-ttu-id="71fc7-132">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="71fc7-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="71fc7-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71fc7-133">NOTES</span></span>
* <span data-ttu-id="71fc7-134">Cmdleten **Resume-AzSqlDatabase** fungerar bara i Azure SQL Data Warehouse-databaser.</span><span class="sxs-lookup"><span data-stu-id="71fc7-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="71fc7-135">Den här åtgärden stöds inte i SQL-databaserna Basic, standard och Premium.</span><span class="sxs-lookup"><span data-stu-id="71fc7-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="71fc7-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71fc7-136">RELATED LINKS</span></span>

[<span data-ttu-id="71fc7-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="71fc7-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="71fc7-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="71fc7-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="71fc7-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="71fc7-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="71fc7-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="71fc7-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="71fc7-141">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="71fc7-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="71fc7-142">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="71fc7-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


