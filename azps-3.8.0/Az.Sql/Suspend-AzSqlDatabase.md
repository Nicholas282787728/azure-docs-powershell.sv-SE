---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: a2bfaa0b6cd6d0731bceab7f05a59216e80bd135
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927066"
---
# <span data-ttu-id="31ea5-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31ea5-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="31ea5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="31ea5-103">Avbryter en SQL Data Warehouse-databas.</span><span class="sxs-lookup"><span data-stu-id="31ea5-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="31ea5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31ea5-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31ea5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31ea5-105">DESCRIPTION</span></span>
<span data-ttu-id="31ea5-106">Cmdleten **suspend-AzSqlDatabase** inaktive ras en Azure SQL Data Warehouse-databas.</span><span class="sxs-lookup"><span data-stu-id="31ea5-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="31ea5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31ea5-107">EXAMPLES</span></span>

### <span data-ttu-id="31ea5-108">Exempel 1: inaktiverar en Azure SQL Data Warehouse-databas</span><span class="sxs-lookup"><span data-stu-id="31ea5-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="31ea5-109">Det här kommandot gör att en Active Azure SQL Data Warehouse-databas stoppas.</span><span class="sxs-lookup"><span data-stu-id="31ea5-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="31ea5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31ea5-110">PARAMETERS</span></span>

### <span data-ttu-id="31ea5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31ea5-111">-AsJob</span></span>
<span data-ttu-id="31ea5-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="31ea5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31ea5-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="31ea5-113">-DatabaseName</span></span>
<span data-ttu-id="31ea5-114">Anger namnet på den databas som denna cmdlet gör paus för.</span><span class="sxs-lookup"><span data-stu-id="31ea5-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="31ea5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ea5-115">-DefaultProfile</span></span>
<span data-ttu-id="31ea5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="31ea5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31ea5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ea5-117">-ResourceGroupName</span></span>
<span data-ttu-id="31ea5-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="31ea5-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="31ea5-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="31ea5-119">-ServerName</span></span>
<span data-ttu-id="31ea5-120">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="31ea5-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="31ea5-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="31ea5-121">-Confirm</span></span>
<span data-ttu-id="31ea5-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="31ea5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31ea5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31ea5-123">-WhatIf</span></span>
<span data-ttu-id="31ea5-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="31ea5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31ea5-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="31ea5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31ea5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ea5-126">CommonParameters</span></span>
<span data-ttu-id="31ea5-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ea5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ea5-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31ea5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ea5-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31ea5-129">INPUTS</span></span>

### <span data-ttu-id="31ea5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="31ea5-130">System.String</span></span>

## <span data-ttu-id="31ea5-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31ea5-131">OUTPUTS</span></span>

### <span data-ttu-id="31ea5-132">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="31ea5-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="31ea5-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31ea5-133">NOTES</span></span>
* <span data-ttu-id="31ea5-134">Cmdleten **suspend-AzSqlDatabase** fungerar bara i Azure SQL Data Warehouse-databaser.</span><span class="sxs-lookup"><span data-stu-id="31ea5-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="31ea5-135">Den här åtgärden stöds inte i SQL-databaserna Basic, standard och Premium.</span><span class="sxs-lookup"><span data-stu-id="31ea5-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="31ea5-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31ea5-136">RELATED LINKS</span></span>

[<span data-ttu-id="31ea5-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31ea5-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="31ea5-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31ea5-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="31ea5-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31ea5-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="31ea5-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31ea5-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="31ea5-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31ea5-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="31ea5-142">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="31ea5-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


