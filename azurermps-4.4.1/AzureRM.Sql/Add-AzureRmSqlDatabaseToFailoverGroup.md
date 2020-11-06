---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 2772f806ba5297ee9809a8800b25b4c42daf171e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580519"
---
# <span data-ttu-id="27e9e-101">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27e9e-101">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="27e9e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="27e9e-103">Lägger till en eller flera databaser i en failover-grupp i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="27e9e-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27e9e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27e9e-104">SYNTAX</span></span>

```
Add-AzureRmSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27e9e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27e9e-105">DESCRIPTION</span></span>
<span data-ttu-id="27e9e-106">Lägger till en eller flera databaser i en Azure SQL Database failover-grupps primära server i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="27e9e-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="27e9e-107">Databaser får inte vara sekundära databaser i befintliga replikeringspartners.</span><span class="sxs-lookup"><span data-stu-id="27e9e-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="27e9e-108">Kommandot påbörjar geo-replikering av eventuella tillagda databaser i gruppens sekundära Server.</span><span class="sxs-lookup"><span data-stu-id="27e9e-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>

<span data-ttu-id="27e9e-109">Använd (till exempel) Get-AzureRmSqlDatabase cmdlet för att hämta de databas objekt som ska fylla på parametern "-databas".</span><span class="sxs-lookup"><span data-stu-id="27e9e-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>

<span data-ttu-id="27e9e-110">Failover-gruppens primär server måste användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="27e9e-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="27e9e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27e9e-111">EXAMPLES</span></span>

### <span data-ttu-id="27e9e-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="27e9e-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="27e9e-113">Det här kommandot lägger till en databas i en failover-grupp genom att flytta den.</span><span class="sxs-lookup"><span data-stu-id="27e9e-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="27e9e-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="27e9e-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzureRmSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="27e9e-115">Det här kommandot lägger till alla databaser i en server i en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="27e9e-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="27e9e-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="27e9e-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzureRmSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="27e9e-117">Det här kommandot lägger till alla databaser i en elastisk pool till en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="27e9e-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="27e9e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27e9e-118">PARAMETERS</span></span>

### <span data-ttu-id="27e9e-119">-Databas</span><span class="sxs-lookup"><span data-stu-id="27e9e-119">-Database</span></span>
<span data-ttu-id="27e9e-120">En eller flera Azure SQL-databaser på failover-gruppens primär server som ska läggas till i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="27e9e-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="27e9e-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="27e9e-121">-FailoverGroupName</span></span>
<span data-ttu-id="27e9e-122">Namnet på failover-gruppen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="27e9e-122">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="27e9e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27e9e-123">-ResourceGroupName</span></span>
<span data-ttu-id="27e9e-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="27e9e-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="27e9e-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="27e9e-125">-ServerName</span></span>
<span data-ttu-id="27e9e-126">Namnet på den primära Azure SQL-databasfilen i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="27e9e-126">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="27e9e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27e9e-127">-DefaultProfile</span></span>
<span data-ttu-id="27e9e-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27e9e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27e9e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e9e-129">CommonParameters</span></span>
<span data-ttu-id="27e9e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27e9e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e9e-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27e9e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e9e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27e9e-132">INPUTS</span></span>

### <span data-ttu-id="27e9e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="27e9e-133">System.String</span></span>
<span data-ttu-id="27e9e-134">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. kommandon. SQL. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. commands. SQL, version = 2.5.0.0, Culture = neutralt, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="27e9e-134">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="27e9e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27e9e-135">OUTPUTS</span></span>

### <span data-ttu-id="27e9e-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="27e9e-136">System.Object</span></span>

## <span data-ttu-id="27e9e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27e9e-137">NOTES</span></span>

## <span data-ttu-id="27e9e-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27e9e-138">RELATED LINKS</span></span>

[<span data-ttu-id="27e9e-139">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27e9e-139">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="27e9e-140">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27e9e-140">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="27e9e-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27e9e-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="27e9e-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27e9e-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="27e9e-143">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27e9e-143">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="27e9e-144">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27e9e-144">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="27e9e-145">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="27e9e-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
