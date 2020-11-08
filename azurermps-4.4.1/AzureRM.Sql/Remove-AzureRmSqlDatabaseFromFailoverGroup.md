---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: b796d1247d1f8a49316431ca944ac6cd1fb77d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758280"
---
# <span data-ttu-id="3bb16-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3bb16-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="3bb16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3bb16-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb16-103">Tar bort en eller flera databaser från en failover-grupp i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3bb16-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bb16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3bb16-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3bb16-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3bb16-105">DESCRIPTION</span></span>
<span data-ttu-id="3bb16-106">Tar bort en eller flera databaser från den angivna failover-gruppen för Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3bb16-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="3bb16-107">Databaserna och replikeringsrelationen är oförändrade, men de kommer inte längre att vara tillgängliga via slut punkter för gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="3bb16-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>

<span data-ttu-id="3bb16-108">Använd (till exempel) Get-AzureRmSqlDatabase cmdlet för att hämta de databas objekt som ska fylla på parametern "-databas".</span><span class="sxs-lookup"><span data-stu-id="3bb16-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>

<span data-ttu-id="3bb16-109">Failover-gruppens primär server måste användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="3bb16-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="3bb16-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3bb16-110">EXAMPLES</span></span>

### <span data-ttu-id="3bb16-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3bb16-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="3bb16-112">Det här kommandot tar bort en databas från en failover-grupp genom att flytta den.</span><span class="sxs-lookup"><span data-stu-id="3bb16-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="3bb16-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3bb16-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzureRmSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="3bb16-114">Det här kommandot tar bort alla databaser från en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="3bb16-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="3bb16-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="3bb16-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzureRMSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="3bb16-116">Det här kommandot tar bort alla databaser i en elastisk pool från en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="3bb16-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="3bb16-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3bb16-117">PARAMETERS</span></span>

### <span data-ttu-id="3bb16-118">-Databas</span><span class="sxs-lookup"><span data-stu-id="3bb16-118">-Database</span></span>
<span data-ttu-id="3bb16-119">En eller flera Azure SQL-databaser på failover-gruppens primär server som ska tas bort från failover-gruppen.</span><span class="sxs-lookup"><span data-stu-id="3bb16-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="3bb16-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="3bb16-120">-FailoverGroupName</span></span>
<span data-ttu-id="3bb16-121">Namnet på failover-gruppen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3bb16-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="3bb16-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3bb16-122">-Force</span></span>
<span data-ttu-id="3bb16-123">Hoppa över bekräftelse meddelande för att utföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="3bb16-123">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="3bb16-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bb16-124">-ResourceGroupName</span></span>
<span data-ttu-id="3bb16-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3bb16-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="3bb16-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3bb16-126">-ServerName</span></span>
<span data-ttu-id="3bb16-127">Namnet på den primära Azure SQL-databasfilen i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="3bb16-127">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="3bb16-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3bb16-128">-Confirm</span></span>
<span data-ttu-id="3bb16-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3bb16-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bb16-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bb16-130">-WhatIf</span></span>
<span data-ttu-id="3bb16-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3bb16-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bb16-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3bb16-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bb16-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb16-133">-DefaultProfile</span></span>
<span data-ttu-id="3bb16-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb16-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bb16-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb16-135">CommonParameters</span></span>
<span data-ttu-id="3bb16-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bb16-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb16-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bb16-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb16-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3bb16-138">INPUTS</span></span>

### <span data-ttu-id="3bb16-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3bb16-139">System.String</span></span>
<span data-ttu-id="3bb16-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. commands. SQL, version = 2.5.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3bb16-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3bb16-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3bb16-141">OUTPUTS</span></span>

### <span data-ttu-id="3bb16-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="3bb16-142">System.Object</span></span>

## <span data-ttu-id="3bb16-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3bb16-143">NOTES</span></span>

## <span data-ttu-id="3bb16-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3bb16-144">RELATED LINKS</span></span>

[<span data-ttu-id="3bb16-145">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3bb16-145">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3bb16-146">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3bb16-146">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3bb16-147">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3bb16-147">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3bb16-148">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3bb16-148">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="3bb16-149">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3bb16-149">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3bb16-150">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3bb16-150">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3bb16-151">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="3bb16-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)