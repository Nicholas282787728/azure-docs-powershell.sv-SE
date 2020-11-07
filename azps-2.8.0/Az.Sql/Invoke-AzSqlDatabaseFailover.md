---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 5832b263f87ee0122dbc49c6dc765e7e54287311
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920591"
---
# <span data-ttu-id="9dddb-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="9dddb-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="9dddb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9dddb-102">SYNOPSIS</span></span>
<span data-ttu-id="9dddb-103">Redundans för en databas.</span><span class="sxs-lookup"><span data-stu-id="9dddb-103">Failovers a database.</span></span>

## <span data-ttu-id="9dddb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9dddb-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-AsJob] [-PassThru] [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9dddb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9dddb-105">DESCRIPTION</span></span>
<span data-ttu-id="9dddb-106">Invoke-AzSqlDatabaseFailover cmdlet redundansväxlingen en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="9dddb-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="9dddb-107">Om databasen är i en elastisk pool kommer det här kommandot att redundansväxla den angivna databasen utan att det påverkar de andra databaserna i samma elastiska pool.</span><span class="sxs-lookup"><span data-stu-id="9dddb-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="9dddb-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9dddb-108">EXAMPLES</span></span>

### <span data-ttu-id="9dddb-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9dddb-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="9dddb-110">Det här kommandot kommer att redundansväxla databasen med namnet "Database01" på servern med namnet "Server01"</span><span class="sxs-lookup"><span data-stu-id="9dddb-110">This command will failover the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="9dddb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9dddb-111">PARAMETERS</span></span>

### <span data-ttu-id="9dddb-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dddb-112">-AsJob</span></span>
<span data-ttu-id="9dddb-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9dddb-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9dddb-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9dddb-114">-DatabaseName</span></span>
<span data-ttu-id="9dddb-115">Namnet på din Azure SQL-databas till redundans.</span><span class="sxs-lookup"><span data-stu-id="9dddb-115">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="9dddb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dddb-116">-DefaultProfile</span></span>
<span data-ttu-id="9dddb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9dddb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dddb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9dddb-118">-Force</span></span>
<span data-ttu-id="9dddb-119">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="9dddb-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9dddb-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dddb-120">-PassThru</span></span>
<span data-ttu-id="9dddb-121">Returnerar true när den körs.</span><span class="sxs-lookup"><span data-stu-id="9dddb-121">On Successful execution, returns true.</span></span>  <span data-ttu-id="9dddb-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9dddb-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9dddb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dddb-123">-ResourceGroupName</span></span>
<span data-ttu-id="9dddb-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9dddb-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="9dddb-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9dddb-125">-ServerName</span></span>
<span data-ttu-id="9dddb-126">Namnet på den Azure SQL-databasserver som databasen finns i.</span><span class="sxs-lookup"><span data-stu-id="9dddb-126">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="9dddb-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9dddb-127">-Confirm</span></span>
<span data-ttu-id="9dddb-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9dddb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dddb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dddb-129">-WhatIf</span></span>
<span data-ttu-id="9dddb-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9dddb-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9dddb-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9dddb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dddb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dddb-132">CommonParameters</span></span>
<span data-ttu-id="9dddb-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dddb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dddb-134">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dddb-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dddb-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9dddb-135">INPUTS</span></span>

### <span data-ttu-id="9dddb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9dddb-136">System.String</span></span>

## <span data-ttu-id="9dddb-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9dddb-137">OUTPUTS</span></span>

## <span data-ttu-id="9dddb-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9dddb-138">NOTES</span></span>

## <span data-ttu-id="9dddb-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9dddb-139">RELATED LINKS</span></span>

[<span data-ttu-id="9dddb-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9dddb-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="9dddb-141">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="9dddb-141">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="9dddb-142">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9dddb-142">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="9dddb-143">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9dddb-143">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="9dddb-144">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9dddb-144">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="9dddb-145">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9dddb-145">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="9dddb-146">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9dddb-146">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="9dddb-147">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="9dddb-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
