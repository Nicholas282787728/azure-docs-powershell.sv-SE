---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: d8eff694378f6145931a18a622f29bf88d99e1ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272814"
---
# <span data-ttu-id="34ef9-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="34ef9-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="34ef9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="34ef9-103">Kör en redundansväxling av en failover-grupp för Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="34ef9-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="34ef9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34ef9-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34ef9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34ef9-105">DESCRIPTION</span></span>
<span data-ttu-id="34ef9-106">Det här kommandot byter plats på servrarnas roller i en failover-grupp och växlar alla sekundära databaser till den primära rollen.</span><span class="sxs-lookup"><span data-stu-id="34ef9-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="34ef9-107">Alla nya TDS-sessioner omdirigeras automatiskt till den sekundära servern efter att DNS-klientcachen har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="34ef9-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="34ef9-108">När den ursprungliga primära servern är online kommer alla tidigare primära databaser i den att växla till den sekundära rollen.</span><span class="sxs-lookup"><span data-stu-id="34ef9-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="34ef9-109">Gruppens sekundära Server måste användas för att utföra det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="34ef9-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="34ef9-110">Om parametern AllowDataLoss inte anges väntar det här kommandot tills båda rollerna har bytts.</span><span class="sxs-lookup"><span data-stu-id="34ef9-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="34ef9-111">Om parametern AllowDataLoss anges väntar kommandot bara på den nya primära rollen.</span><span class="sxs-lookup"><span data-stu-id="34ef9-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="34ef9-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34ef9-112">EXAMPLES</span></span>

### <span data-ttu-id="34ef9-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="34ef9-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="34ef9-114">Problem med en redundansväxling som möjliggör förlust av data i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="34ef9-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="34ef9-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="34ef9-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="34ef9-116">Få en failover-åtgärd som fungerar bäst utan att förlora data eller Miss lyckas och återställa.</span><span class="sxs-lookup"><span data-stu-id="34ef9-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="34ef9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34ef9-117">PARAMETERS</span></span>

### <span data-ttu-id="34ef9-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="34ef9-118">-AllowDataLoss</span></span>
<span data-ttu-id="34ef9-119">Slutför redundans trots att det kan leda till data förlust.</span><span class="sxs-lookup"><span data-stu-id="34ef9-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="34ef9-120">Detta gör att redundansväxlingen kan fortsätta även om en primär databas inte är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="34ef9-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="34ef9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34ef9-121">-AsJob</span></span>
<span data-ttu-id="34ef9-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="34ef9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34ef9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ef9-123">-DefaultProfile</span></span>
<span data-ttu-id="34ef9-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="34ef9-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34ef9-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="34ef9-125">-FailoverGroupName</span></span>
<span data-ttu-id="34ef9-126">Namnet på failover-gruppen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="34ef9-126">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="34ef9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34ef9-127">-ResourceGroupName</span></span>
<span data-ttu-id="34ef9-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="34ef9-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="34ef9-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="34ef9-129">-ServerName</span></span>
<span data-ttu-id="34ef9-130">Namnet på den sekundära Azure SQL-databasfilen för gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="34ef9-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="34ef9-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="34ef9-131">-Confirm</span></span>
<span data-ttu-id="34ef9-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="34ef9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34ef9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34ef9-133">-WhatIf</span></span>
<span data-ttu-id="34ef9-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="34ef9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34ef9-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="34ef9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34ef9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ef9-136">CommonParameters</span></span>
<span data-ttu-id="34ef9-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34ef9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ef9-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34ef9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ef9-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34ef9-139">INPUTS</span></span>

### <span data-ttu-id="34ef9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="34ef9-140">System.String</span></span>

## <span data-ttu-id="34ef9-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34ef9-141">OUTPUTS</span></span>

### <span data-ttu-id="34ef9-142">Microsoft. Azure. commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="34ef9-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="34ef9-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34ef9-143">NOTES</span></span>

## <span data-ttu-id="34ef9-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34ef9-144">RELATED LINKS</span></span>

[<span data-ttu-id="34ef9-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="34ef9-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="34ef9-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="34ef9-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="34ef9-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="34ef9-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="34ef9-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="34ef9-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="34ef9-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="34ef9-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="34ef9-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="34ef9-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="34ef9-151">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="34ef9-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
