---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 15b0026158f3942ffbb9ff1d426104cffcb18a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746451"
---
# <span data-ttu-id="d91f0-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d91f0-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="d91f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d91f0-102">SYNOPSIS</span></span>
<span data-ttu-id="d91f0-103">Kör en redundansväxling av en failover-grupp för Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="d91f0-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="d91f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d91f0-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d91f0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d91f0-105">DESCRIPTION</span></span>
<span data-ttu-id="d91f0-106">Det här kommandot byter plats på servrarnas roller i en failover-grupp och växlar alla sekundära databaser till den primära rollen.</span><span class="sxs-lookup"><span data-stu-id="d91f0-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="d91f0-107">Alla nya TDS-sessioner omdirigeras automatiskt till den sekundära servern efter att DNS-klientcachen har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="d91f0-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="d91f0-108">När den ursprungliga primära servern är online kommer alla tidigare primära databaser i den att växla till den sekundära rollen.</span><span class="sxs-lookup"><span data-stu-id="d91f0-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="d91f0-109">Gruppens sekundära Server måste användas för att utföra det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="d91f0-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="d91f0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d91f0-110">EXAMPLES</span></span>

### <span data-ttu-id="d91f0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d91f0-111">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="d91f0-112">Problem med en redundansväxling som möjliggör förlust av data i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="d91f0-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="d91f0-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d91f0-113">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="d91f0-114">Få en failover-åtgärd som fungerar bäst utan att förlora data eller Miss lyckas och återställa.</span><span class="sxs-lookup"><span data-stu-id="d91f0-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="d91f0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d91f0-115">PARAMETERS</span></span>

### <span data-ttu-id="d91f0-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="d91f0-116">-AllowDataLoss</span></span>
<span data-ttu-id="d91f0-117">Slutför redundans trots att det kan leda till data förlust.</span><span class="sxs-lookup"><span data-stu-id="d91f0-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="d91f0-118">Detta gör att redundansväxlingen kan fortsätta även om en primär databas inte är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="d91f0-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d91f0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d91f0-119">-AsJob</span></span>
<span data-ttu-id="d91f0-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d91f0-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d91f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d91f0-121">-DefaultProfile</span></span>
<span data-ttu-id="d91f0-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d91f0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d91f0-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="d91f0-123">-FailoverGroupName</span></span>
<span data-ttu-id="d91f0-124">Namnet på failover-gruppen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="d91f0-124">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d91f0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d91f0-125">-ResourceGroupName</span></span>
<span data-ttu-id="d91f0-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d91f0-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="d91f0-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d91f0-127">-ServerName</span></span>
<span data-ttu-id="d91f0-128">Namnet på den sekundära Azure SQL-databasfilen för gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="d91f0-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="d91f0-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d91f0-129">-Confirm</span></span>
<span data-ttu-id="d91f0-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d91f0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d91f0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d91f0-131">-WhatIf</span></span>
<span data-ttu-id="d91f0-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d91f0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d91f0-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d91f0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d91f0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d91f0-134">CommonParameters</span></span>
<span data-ttu-id="d91f0-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d91f0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d91f0-136">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d91f0-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d91f0-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d91f0-137">INPUTS</span></span>

### <span data-ttu-id="d91f0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d91f0-138">System.String</span></span>

## <span data-ttu-id="d91f0-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d91f0-139">OUTPUTS</span></span>

### <span data-ttu-id="d91f0-140">Microsoft. Azure. commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="d91f0-140">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="d91f0-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d91f0-141">NOTES</span></span>

## <span data-ttu-id="d91f0-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d91f0-142">RELATED LINKS</span></span>

[<span data-ttu-id="d91f0-143">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d91f0-143">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d91f0-144">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d91f0-144">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d91f0-145">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d91f0-145">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d91f0-146">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d91f0-146">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="d91f0-147">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d91f0-147">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="d91f0-148">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d91f0-148">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d91f0-149">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="d91f0-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
