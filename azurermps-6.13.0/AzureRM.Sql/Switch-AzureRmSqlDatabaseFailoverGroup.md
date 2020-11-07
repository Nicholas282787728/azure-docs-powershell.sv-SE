---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/switch-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 708b010a8ff7b2a289d538a07e7b679fcec6efab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757330"
---
# <span data-ttu-id="4e2b2-101">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4e2b2-101">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="4e2b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e2b2-102">SYNOPSIS</span></span>
<span data-ttu-id="4e2b2-103">Kör en redundansväxling av en failover-grupp för Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e2b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e2b2-104">SYNTAX</span></span>

```
Switch-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e2b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e2b2-105">DESCRIPTION</span></span>
<span data-ttu-id="4e2b2-106">Det här kommandot byter plats på servrarnas roller i en failover-grupp och växlar alla sekundära databaser till den primära rollen.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="4e2b2-107">Alla nya TDS-sessioner omdirigeras automatiskt till den sekundära servern efter att DNS-klientcachen har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="4e2b2-108">När den ursprungliga primära servern är online kommer alla tidigare primära databaser i den att växla till den sekundära rollen.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="4e2b2-109">Gruppens sekundära Server måste användas för att utföra det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="4e2b2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e2b2-110">EXAMPLES</span></span>

### <span data-ttu-id="4e2b2-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4e2b2-111">Example 1</span></span>
```
C:\> Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzureRmSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="4e2b2-112">Problem med en redundansväxling som möjliggör förlust av data i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="4e2b2-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4e2b2-113">Example 2</span></span>
```
C:\> Switch-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="4e2b2-114">Få en failover-åtgärd som fungerar bäst utan att förlora data eller Miss lyckas och återställa.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="4e2b2-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e2b2-115">PARAMETERS</span></span>

### <span data-ttu-id="4e2b2-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="4e2b2-116">-AllowDataLoss</span></span>
<span data-ttu-id="4e2b2-117">Slutför redundans trots att det kan leda till data förlust.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="4e2b2-118">Detta gör att redundansväxlingen kan fortsätta även om en primär databas inte är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="4e2b2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e2b2-119">-AsJob</span></span>
<span data-ttu-id="4e2b2-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4e2b2-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e2b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e2b2-121">-DefaultProfile</span></span>
<span data-ttu-id="4e2b2-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4e2b2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e2b2-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="4e2b2-123">-FailoverGroupName</span></span>
<span data-ttu-id="4e2b2-124">Namnet på failover-gruppen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="4e2b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e2b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="4e2b2-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="4e2b2-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4e2b2-127">-ServerName</span></span>
<span data-ttu-id="4e2b2-128">Namnet på den sekundära Azure SQL-databasfilen för gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="4e2b2-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e2b2-129">-Confirm</span></span>
<span data-ttu-id="4e2b2-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e2b2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e2b2-131">-WhatIf</span></span>
<span data-ttu-id="4e2b2-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e2b2-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e2b2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e2b2-134">CommonParameters</span></span>
<span data-ttu-id="4e2b2-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e2b2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e2b2-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e2b2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e2b2-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e2b2-137">INPUTS</span></span>

### <span data-ttu-id="4e2b2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4e2b2-138">System.String</span></span>

## <span data-ttu-id="4e2b2-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e2b2-139">OUTPUTS</span></span>

### <span data-ttu-id="4e2b2-140">Microsoft. Azure. commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4e2b2-140">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="4e2b2-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e2b2-141">NOTES</span></span>

## <span data-ttu-id="4e2b2-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e2b2-142">RELATED LINKS</span></span>

[<span data-ttu-id="4e2b2-143">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4e2b2-143">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4e2b2-144">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4e2b2-144">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4e2b2-145">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4e2b2-145">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4e2b2-146">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4e2b2-146">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="4e2b2-147">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4e2b2-147">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="4e2b2-148">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4e2b2-148">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4e2b2-149">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="4e2b2-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
