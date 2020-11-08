---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 7fa7c09d5c6c992dfa3eab7a6f81b70e820a9ee4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090928"
---
# <span data-ttu-id="72f2d-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72f2d-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="72f2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="72f2d-103">Tar bort en eller flera databaser från en failover-grupp i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="72f2d-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="72f2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72f2d-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72f2d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72f2d-105">DESCRIPTION</span></span>
<span data-ttu-id="72f2d-106">Tar bort en eller flera databaser från den angivna failover-gruppen för Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="72f2d-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="72f2d-107">Databaserna och replikeringsrelationen är oförändrade, men de kommer inte längre att vara tillgängliga via slut punkter för gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="72f2d-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="72f2d-108">Använd (till exempel) Get-AzSqlDatabase cmdlet för att hämta de databas objekt som ska fylla på parametern "-databas".</span><span class="sxs-lookup"><span data-stu-id="72f2d-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="72f2d-109">Failover-gruppens primär server måste användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="72f2d-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="72f2d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72f2d-110">EXAMPLES</span></span>

### <span data-ttu-id="72f2d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="72f2d-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="72f2d-112">Det här kommandot tar bort en databas från en failover-grupp genom att flytta den.</span><span class="sxs-lookup"><span data-stu-id="72f2d-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="72f2d-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="72f2d-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="72f2d-114">Det här kommandot tar bort alla databaser från en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="72f2d-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="72f2d-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="72f2d-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="72f2d-116">Det här kommandot tar bort alla databaser i en elastisk pool från en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="72f2d-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="72f2d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72f2d-117">PARAMETERS</span></span>

### <span data-ttu-id="72f2d-118">-Databas</span><span class="sxs-lookup"><span data-stu-id="72f2d-118">-Database</span></span>
<span data-ttu-id="72f2d-119">En eller flera Azure SQL-databaser på failover-gruppens primär server som ska tas bort från failover-gruppen.</span><span class="sxs-lookup"><span data-stu-id="72f2d-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72f2d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72f2d-120">-DefaultProfile</span></span>
<span data-ttu-id="72f2d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="72f2d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72f2d-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="72f2d-122">-FailoverGroupName</span></span>
<span data-ttu-id="72f2d-123">Namnet på failover-gruppen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="72f2d-123">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f2d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="72f2d-124">-Force</span></span>
<span data-ttu-id="72f2d-125">Hoppa över bekräftelse meddelande för att utföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="72f2d-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="72f2d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72f2d-126">-ResourceGroupName</span></span>
<span data-ttu-id="72f2d-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="72f2d-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="72f2d-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72f2d-128">-ServerName</span></span>
<span data-ttu-id="72f2d-129">Namnet på den primära Azure SQL-databasfilen i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="72f2d-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="72f2d-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72f2d-130">-Confirm</span></span>
<span data-ttu-id="72f2d-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72f2d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72f2d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72f2d-132">-WhatIf</span></span>
<span data-ttu-id="72f2d-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72f2d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72f2d-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72f2d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72f2d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f2d-135">CommonParameters</span></span>
<span data-ttu-id="72f2d-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72f2d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f2d-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72f2d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f2d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72f2d-138">INPUTS</span></span>

### <span data-ttu-id="72f2d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="72f2d-139">System.String</span></span>

### <span data-ttu-id="72f2d-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. PowerShell. cmdletar. SQL, version = 1.3.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="72f2d-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="72f2d-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72f2d-141">OUTPUTS</span></span>

### <span data-ttu-id="72f2d-142">Microsoft. Azure. commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="72f2d-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="72f2d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72f2d-143">NOTES</span></span>

## <span data-ttu-id="72f2d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72f2d-144">RELATED LINKS</span></span>

[<span data-ttu-id="72f2d-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72f2d-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="72f2d-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72f2d-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="72f2d-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72f2d-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="72f2d-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72f2d-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="72f2d-149">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72f2d-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="72f2d-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72f2d-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="72f2d-151">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="72f2d-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
