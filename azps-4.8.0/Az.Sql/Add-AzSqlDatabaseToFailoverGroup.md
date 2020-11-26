---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 7577809134987bd1a0092e28170d5bf25ccac04e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261010"
---
# <span data-ttu-id="6dc2b-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6dc2b-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="6dc2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6dc2b-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc2b-103">Lägger till en eller flera databaser i en failover-grupp i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="6dc2b-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="6dc2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6dc2b-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dc2b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6dc2b-105">DESCRIPTION</span></span>
<span data-ttu-id="6dc2b-106">Lägger till en eller flera databaser i en Azure SQL Database failover-grupps primära server i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="6dc2b-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="6dc2b-107">Databaser får inte vara sekundära databaser i befintliga replikeringspartners.</span><span class="sxs-lookup"><span data-stu-id="6dc2b-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="6dc2b-108">Kommandot påbörjar geo-replikering av eventuella tillagda databaser i gruppens sekundära Server.</span><span class="sxs-lookup"><span data-stu-id="6dc2b-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="6dc2b-109">Använd (till exempel) Get-AzSqlDatabase cmdlet för att hämta de databas objekt som ska fylla på parametern "-databas".</span><span class="sxs-lookup"><span data-stu-id="6dc2b-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="6dc2b-110">Failover-gruppens primär server måste användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="6dc2b-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="6dc2b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6dc2b-111">EXAMPLES</span></span>

### <span data-ttu-id="6dc2b-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6dc2b-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="6dc2b-113">Det här kommandot lägger till en databas i en failover-grupp genom att flytta den.</span><span class="sxs-lookup"><span data-stu-id="6dc2b-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="6dc2b-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6dc2b-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="6dc2b-115">Det här kommandot lägger till alla databaser i en server i en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="6dc2b-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="6dc2b-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="6dc2b-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="6dc2b-117">Det här kommandot lägger till alla databaser i en elastisk pool till en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="6dc2b-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="6dc2b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6dc2b-118">PARAMETERS</span></span>

### <span data-ttu-id="6dc2b-119">-Databas</span><span class="sxs-lookup"><span data-stu-id="6dc2b-119">-Database</span></span>
<span data-ttu-id="6dc2b-120">En eller flera Azure SQL-databaser på failover-gruppens primär server som ska läggas till i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="6dc2b-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="6dc2b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc2b-121">-DefaultProfile</span></span>
<span data-ttu-id="6dc2b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6dc2b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6dc2b-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="6dc2b-123">-FailoverGroupName</span></span>
<span data-ttu-id="6dc2b-124">Namnet på failover-gruppen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="6dc2b-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="6dc2b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dc2b-125">-ResourceGroupName</span></span>
<span data-ttu-id="6dc2b-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6dc2b-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="6dc2b-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6dc2b-127">-ServerName</span></span>
<span data-ttu-id="6dc2b-128">Namnet på den primära Azure SQL-databasfilen i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="6dc2b-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="6dc2b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc2b-129">CommonParameters</span></span>
<span data-ttu-id="6dc2b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dc2b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc2b-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dc2b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc2b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6dc2b-132">INPUTS</span></span>

### <span data-ttu-id="6dc2b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6dc2b-133">System.String</span></span>

### <span data-ttu-id="6dc2b-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. PowerShell. cmdletar. SQL, version = 1.3.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6dc2b-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6dc2b-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6dc2b-135">OUTPUTS</span></span>

### <span data-ttu-id="6dc2b-136">Microsoft. Azure. commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="6dc2b-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="6dc2b-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6dc2b-137">NOTES</span></span>

## <span data-ttu-id="6dc2b-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6dc2b-138">RELATED LINKS</span></span>

[<span data-ttu-id="6dc2b-139">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6dc2b-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6dc2b-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6dc2b-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6dc2b-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6dc2b-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6dc2b-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6dc2b-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="6dc2b-143">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6dc2b-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6dc2b-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6dc2b-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6dc2b-145">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="6dc2b-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)