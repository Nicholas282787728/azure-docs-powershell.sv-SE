---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088484"
---
# <span data-ttu-id="56b1f-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="56b1f-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="56b1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="56b1f-103">Redundans för en databas.</span><span class="sxs-lookup"><span data-stu-id="56b1f-103">Failovers a database.</span></span>

## <span data-ttu-id="56b1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56b1f-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56b1f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56b1f-105">DESCRIPTION</span></span>
<span data-ttu-id="56b1f-106">Invoke-AzSqlDatabaseFailover cmdlet redundansväxlingen en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="56b1f-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="56b1f-107">Om databasen är i en elastisk pool kommer det här kommandot att redundansväxla den angivna databasen utan att det påverkar de andra databaserna i samma elastiska pool.</span><span class="sxs-lookup"><span data-stu-id="56b1f-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="56b1f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56b1f-108">EXAMPLES</span></span>

### <span data-ttu-id="56b1f-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="56b1f-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="56b1f-110">Det här kommandot kommer att redundansväxla den primära repliken av databasen med namnet "Database01" på servern med namnet "Server01"</span><span class="sxs-lookup"><span data-stu-id="56b1f-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="56b1f-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="56b1f-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="56b1f-112">Det här kommandot kommer att redundansväxla den läsbara sekundära repliken av databasen med namnet "Database01" på servern med namnet "Server01"</span><span class="sxs-lookup"><span data-stu-id="56b1f-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="56b1f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56b1f-113">PARAMETERS</span></span>

### <span data-ttu-id="56b1f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56b1f-114">-AsJob</span></span>
<span data-ttu-id="56b1f-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="56b1f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56b1f-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="56b1f-116">-DatabaseName</span></span>
<span data-ttu-id="56b1f-117">Namnet på din Azure SQL-databas till redundans.</span><span class="sxs-lookup"><span data-stu-id="56b1f-117">The name of the Azure SQL Database to failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56b1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b1f-118">-DefaultProfile</span></span>
<span data-ttu-id="56b1f-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56b1f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56b1f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="56b1f-120">-Force</span></span>
<span data-ttu-id="56b1f-121">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="56b1f-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="56b1f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56b1f-122">-PassThru</span></span>
<span data-ttu-id="56b1f-123">Returnerar true när den körs.</span><span class="sxs-lookup"><span data-stu-id="56b1f-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="56b1f-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="56b1f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="56b1f-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="56b1f-125">-ReadableSecondary</span></span>
<span data-ttu-id="56b1f-126">Redundansväxla den läsbara sekundära repliken i stället för den primära standard repliken</span><span class="sxs-lookup"><span data-stu-id="56b1f-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="56b1f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56b1f-127">-ResourceGroupName</span></span>
<span data-ttu-id="56b1f-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="56b1f-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="56b1f-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="56b1f-129">-ServerName</span></span>
<span data-ttu-id="56b1f-130">Namnet på den Azure SQL-databasserver som databasen finns i.</span><span class="sxs-lookup"><span data-stu-id="56b1f-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="56b1f-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="56b1f-131">-Confirm</span></span>
<span data-ttu-id="56b1f-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="56b1f-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b1f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56b1f-133">-WhatIf</span></span>
<span data-ttu-id="56b1f-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="56b1f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56b1f-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="56b1f-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b1f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b1f-136">CommonParameters</span></span>
<span data-ttu-id="56b1f-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56b1f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b1f-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56b1f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b1f-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56b1f-139">INPUTS</span></span>

### <span data-ttu-id="56b1f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="56b1f-140">System.String</span></span>

## <span data-ttu-id="56b1f-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56b1f-141">OUTPUTS</span></span>

## <span data-ttu-id="56b1f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56b1f-142">NOTES</span></span>

## <span data-ttu-id="56b1f-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56b1f-143">RELATED LINKS</span></span>

[<span data-ttu-id="56b1f-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56b1f-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="56b1f-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="56b1f-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="56b1f-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56b1f-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="56b1f-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56b1f-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="56b1f-148">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56b1f-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="56b1f-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56b1f-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="56b1f-150">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56b1f-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="56b1f-151">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="56b1f-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)