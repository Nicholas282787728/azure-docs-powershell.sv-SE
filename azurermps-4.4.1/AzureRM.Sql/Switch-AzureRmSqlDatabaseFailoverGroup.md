---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 45be8d0ef10b040fd27a714444bb60bbf6a69951
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583731"
---
# <span data-ttu-id="5d5b7-101">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d5b7-101">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="5d5b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d5b7-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5b7-103">Kör en redundansväxling av en failover-grupp för Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d5b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d5b7-104">SYNTAX</span></span>

```
Switch-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d5b7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d5b7-105">DESCRIPTION</span></span>
<span data-ttu-id="5d5b7-106">Det här kommandot byter plats på servrarnas roller i en failover-grupp och växlar alla sekundära databaser till den primära rollen.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="5d5b7-107">Alla nya TDS-sessioner omdirigeras automatiskt till den sekundära servern efter att DNS-klientcachen har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="5d5b7-108">När den ursprungliga primära servern är online kommer alla tidigare primära databaser i den att växla till den sekundära rollen.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>

<span data-ttu-id="5d5b7-109">Gruppens sekundära Server måste användas för att utföra det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="5d5b7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d5b7-110">EXAMPLES</span></span>

### <span data-ttu-id="5d5b7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5d5b7-111">Example 1</span></span>
```
C:\> Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzureRmSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="5d5b7-112">Problem med en redundansväxling som möjliggör förlust av data i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="5d5b7-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5d5b7-113">Example 2</span></span>
```
C:\> Switch-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="5d5b7-114">Få en failover-åtgärd som fungerar bäst utan att förlora data eller Miss lyckas och återställa.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="5d5b7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d5b7-115">PARAMETERS</span></span>

### <span data-ttu-id="5d5b7-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="5d5b7-116">-AllowDataLoss</span></span>
<span data-ttu-id="5d5b7-117">Slutför redundans trots att det kan leda till data förlust.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="5d5b7-118">Detta gör att redundansväxlingen kan fortsätta även om en primär databas inte är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="5d5b7-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="5d5b7-119">-FailoverGroupName</span></span>
<span data-ttu-id="5d5b7-120">Namnet på failover-gruppen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-120">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="5d5b7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d5b7-121">-ResourceGroupName</span></span>
<span data-ttu-id="5d5b7-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d5b7-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5d5b7-123">-ServerName</span></span>
<span data-ttu-id="5d5b7-124">Namnet på den sekundära Azure SQL-databasfilen för gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-124">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="5d5b7-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5d5b7-125">-Confirm</span></span>
<span data-ttu-id="5d5b7-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d5b7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d5b7-127">-WhatIf</span></span>
<span data-ttu-id="5d5b7-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d5b7-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d5b7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5b7-130">-DefaultProfile</span></span>
<span data-ttu-id="5d5b7-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d5b7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5b7-132">CommonParameters</span></span>
<span data-ttu-id="5d5b7-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d5b7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5b7-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d5b7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5b7-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d5b7-135">INPUTS</span></span>

### <span data-ttu-id="5d5b7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5d5b7-136">System.String</span></span>

## <span data-ttu-id="5d5b7-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d5b7-137">OUTPUTS</span></span>

### <span data-ttu-id="5d5b7-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="5d5b7-138">System.Object</span></span>

## <span data-ttu-id="5d5b7-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d5b7-139">NOTES</span></span>

## <span data-ttu-id="5d5b7-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d5b7-140">RELATED LINKS</span></span>

[<span data-ttu-id="5d5b7-141">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d5b7-141">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5d5b7-142">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d5b7-142">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5d5b7-143">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d5b7-143">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5d5b7-144">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d5b7-144">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="5d5b7-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d5b7-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="5d5b7-146">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d5b7-146">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5d5b7-147">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="5d5b7-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
