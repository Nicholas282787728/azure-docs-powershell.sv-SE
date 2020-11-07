---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/add-azurermsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: b8e22e9a62fce4549122351d437916de52ba0ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756769"
---
# <span data-ttu-id="cd5bc-101">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cd5bc-101">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="cd5bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd5bc-102">SYNOPSIS</span></span>
<span data-ttu-id="cd5bc-103">Lägger till en eller flera databaser i en failover-grupp i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="cd5bc-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd5bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd5bc-104">SYNTAX</span></span>

```
Add-AzureRmSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd5bc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd5bc-105">DESCRIPTION</span></span>
<span data-ttu-id="cd5bc-106">Lägger till en eller flera databaser i en Azure SQL Database failover-grupps primära server i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="cd5bc-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="cd5bc-107">Databaser får inte vara sekundära databaser i befintliga replikeringspartners.</span><span class="sxs-lookup"><span data-stu-id="cd5bc-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="cd5bc-108">Kommandot påbörjar geo-replikering av eventuella tillagda databaser i gruppens sekundära Server.</span><span class="sxs-lookup"><span data-stu-id="cd5bc-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>

<span data-ttu-id="cd5bc-109">Använd (till exempel) Get-AzureRmSqlDatabase cmdlet för att hämta de databas objekt som ska fylla på parametern "-databas".</span><span class="sxs-lookup"><span data-stu-id="cd5bc-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>

<span data-ttu-id="cd5bc-110">Failover-gruppens primär server måste användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="cd5bc-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="cd5bc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd5bc-111">EXAMPLES</span></span>

### <span data-ttu-id="cd5bc-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cd5bc-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="cd5bc-113">Det här kommandot lägger till en databas i en failover-grupp genom att flytta den.</span><span class="sxs-lookup"><span data-stu-id="cd5bc-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="cd5bc-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cd5bc-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzureRmSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="cd5bc-115">Det här kommandot lägger till alla databaser i en server i en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="cd5bc-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="cd5bc-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="cd5bc-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzureRmSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="cd5bc-117">Det här kommandot lägger till alla databaser i en elastisk pool till en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="cd5bc-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="cd5bc-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd5bc-118">PARAMETERS</span></span>

### <span data-ttu-id="cd5bc-119">-Databas</span><span class="sxs-lookup"><span data-stu-id="cd5bc-119">-Database</span></span>
<span data-ttu-id="cd5bc-120">En eller flera Azure SQL-databaser på failover-gruppens primär server som ska läggas till i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="cd5bc-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="cd5bc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd5bc-121">-DefaultProfile</span></span>
<span data-ttu-id="cd5bc-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cd5bc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd5bc-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="cd5bc-123">-FailoverGroupName</span></span>
<span data-ttu-id="cd5bc-124">Namnet på failover-gruppen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="cd5bc-124">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd5bc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd5bc-125">-ResourceGroupName</span></span>
<span data-ttu-id="cd5bc-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cd5bc-126">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd5bc-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cd5bc-127">-ServerName</span></span>
<span data-ttu-id="cd5bc-128">Namnet på den primära Azure SQL-databasfilen i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="cd5bc-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd5bc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd5bc-129">CommonParameters</span></span>
<span data-ttu-id="cd5bc-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd5bc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd5bc-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd5bc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd5bc-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd5bc-132">INPUTS</span></span>

### <span data-ttu-id="cd5bc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cd5bc-133">System.String</span></span>
<span data-ttu-id="cd5bc-134">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. kommandon. SQL. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. commands. SQL, version = 2.5.0.0, Culture = neutralt, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="cd5bc-134">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="cd5bc-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd5bc-135">OUTPUTS</span></span>

### <span data-ttu-id="cd5bc-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="cd5bc-136">System.Object</span></span>

## <span data-ttu-id="cd5bc-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd5bc-137">NOTES</span></span>

## <span data-ttu-id="cd5bc-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd5bc-138">RELATED LINKS</span></span>

[<span data-ttu-id="cd5bc-139">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cd5bc-139">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cd5bc-140">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cd5bc-140">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cd5bc-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cd5bc-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cd5bc-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cd5bc-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="cd5bc-143">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cd5bc-143">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cd5bc-144">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cd5bc-144">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cd5bc-145">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="cd5bc-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
