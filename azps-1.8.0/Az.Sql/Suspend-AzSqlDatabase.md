---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: 7a5ecbb21af23b31b321ef1568c2eb953a548cf1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746452"
---
# <span data-ttu-id="150bc-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="150bc-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="150bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="150bc-102">SYNOPSIS</span></span>
<span data-ttu-id="150bc-103">Avbryter en SQL Data Warehouse-databas.</span><span class="sxs-lookup"><span data-stu-id="150bc-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="150bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="150bc-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="150bc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="150bc-105">DESCRIPTION</span></span>
<span data-ttu-id="150bc-106">Cmdleten **suspend-AzSqlDatabase** inaktive ras en Azure SQL Data Warehouse-databas.</span><span class="sxs-lookup"><span data-stu-id="150bc-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="150bc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="150bc-107">EXAMPLES</span></span>

### <span data-ttu-id="150bc-108">Exempel 1: inaktiverar en Azure SQL Data Warehouse-databas</span><span class="sxs-lookup"><span data-stu-id="150bc-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="150bc-109">Det här kommandot gör att en Active Azure SQL Data Warehouse-databas stoppas.</span><span class="sxs-lookup"><span data-stu-id="150bc-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="150bc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="150bc-110">PARAMETERS</span></span>

### <span data-ttu-id="150bc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="150bc-111">-AsJob</span></span>
<span data-ttu-id="150bc-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="150bc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="150bc-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="150bc-113">-DatabaseName</span></span>
<span data-ttu-id="150bc-114">Anger namnet på den databas som denna cmdlet gör paus för.</span><span class="sxs-lookup"><span data-stu-id="150bc-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="150bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="150bc-115">-DefaultProfile</span></span>
<span data-ttu-id="150bc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="150bc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="150bc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="150bc-117">-ResourceGroupName</span></span>
<span data-ttu-id="150bc-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="150bc-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="150bc-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="150bc-119">-ServerName</span></span>
<span data-ttu-id="150bc-120">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="150bc-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="150bc-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="150bc-121">-Confirm</span></span>
<span data-ttu-id="150bc-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="150bc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="150bc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="150bc-123">-WhatIf</span></span>
<span data-ttu-id="150bc-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="150bc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="150bc-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="150bc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="150bc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150bc-126">CommonParameters</span></span>
<span data-ttu-id="150bc-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="150bc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150bc-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="150bc-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150bc-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="150bc-129">INPUTS</span></span>

### <span data-ttu-id="150bc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="150bc-130">System.String</span></span>

## <span data-ttu-id="150bc-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="150bc-131">OUTPUTS</span></span>

### <span data-ttu-id="150bc-132">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="150bc-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="150bc-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="150bc-133">NOTES</span></span>
* <span data-ttu-id="150bc-134">Cmdleten **suspend-AzSqlDatabase** fungerar bara i Azure SQL Data Warehouse-databaser.</span><span class="sxs-lookup"><span data-stu-id="150bc-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="150bc-135">Den här åtgärden stöds inte i SQL-databaserna Basic, standard och Premium.</span><span class="sxs-lookup"><span data-stu-id="150bc-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="150bc-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="150bc-136">RELATED LINKS</span></span>

[<span data-ttu-id="150bc-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="150bc-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="150bc-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="150bc-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="150bc-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="150bc-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="150bc-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="150bc-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="150bc-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="150bc-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="150bc-142">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="150bc-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


