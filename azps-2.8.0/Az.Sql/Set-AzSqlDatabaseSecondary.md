---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 7c500ba5ea2494109a99e7c66e084efefc48d2e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920456"
---
# <span data-ttu-id="29d7c-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="29d7c-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="29d7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29d7c-102">SYNOPSIS</span></span>
<span data-ttu-id="29d7c-103">Växlar en sekundär databas till primärt för att initiera redundans.</span><span class="sxs-lookup"><span data-stu-id="29d7c-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="29d7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29d7c-104">SYNTAX</span></span>

### <span data-ttu-id="29d7c-105">NoOptionsSet (standard)</span><span class="sxs-lookup"><span data-stu-id="29d7c-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29d7c-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="29d7c-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29d7c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29d7c-107">DESCRIPTION</span></span>
<span data-ttu-id="29d7c-108">Cmdleten **set-AzSqlDatabaseSecondary** ändrar en sekundär databas så att den blir primär för att initiera redundans.</span><span class="sxs-lookup"><span data-stu-id="29d7c-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="29d7c-109">Denna cmdlet är utformad som en allmän konfigurations kommando, men är för närvarande begränsad till initiering av redundans.</span><span class="sxs-lookup"><span data-stu-id="29d7c-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="29d7c-110">Ange parametern *AllowDataLoss* för att initiera en Force redundans under ett avbrott.</span><span class="sxs-lookup"><span data-stu-id="29d7c-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="29d7c-111">Du behöver inte ange den här parametern när du utför en planerad åtgärd, till exempel en återställnings granskning.</span><span class="sxs-lookup"><span data-stu-id="29d7c-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="29d7c-112">I det senare fallet synkroniseras den sekundära databasen med primärt innan den ändras.</span><span class="sxs-lookup"><span data-stu-id="29d7c-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="29d7c-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29d7c-113">EXAMPLES</span></span>

### <span data-ttu-id="29d7c-114">1: initiera en planerad redundans</span><span class="sxs-lookup"><span data-stu-id="29d7c-114">1: Initiate a planned failover</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="29d7c-115">2: initiera en framtvingad redundans (med potentiell data förlust)</span><span class="sxs-lookup"><span data-stu-id="29d7c-115">2: Initiate a forced failover (with potential data loss)</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="29d7c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29d7c-116">PARAMETERS</span></span>

### <span data-ttu-id="29d7c-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="29d7c-117">-AllowDataLoss</span></span>
<span data-ttu-id="29d7c-118">Visar att denna redundansväxling tillåter data förlust.</span><span class="sxs-lookup"><span data-stu-id="29d7c-118">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d7c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29d7c-119">-AsJob</span></span>
<span data-ttu-id="29d7c-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="29d7c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29d7c-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29d7c-121">-DatabaseName</span></span>
<span data-ttu-id="29d7c-122">Anger namnet på den sekundära Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="29d7c-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="29d7c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d7c-123">-DefaultProfile</span></span>
<span data-ttu-id="29d7c-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="29d7c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29d7c-125">-Failover</span><span class="sxs-lookup"><span data-stu-id="29d7c-125">-Failover</span></span>
<span data-ttu-id="29d7c-126">Anger att den här åtgärden är en redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="29d7c-126">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d7c-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29d7c-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="29d7c-128">Anger namnet på den resurs grupp som partner-Azure SQL-databasen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="29d7c-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29d7c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29d7c-129">-ResourceGroupName</span></span>
<span data-ttu-id="29d7c-130">Anger namnet på den resurs grupp som den sekundära Azure SQL-databasen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="29d7c-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="29d7c-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="29d7c-131">-ServerName</span></span>
<span data-ttu-id="29d7c-132">Anger namnet på den SQL Server som är värd för den sekundära Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="29d7c-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="29d7c-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="29d7c-133">-Confirm</span></span>
<span data-ttu-id="29d7c-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29d7c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29d7c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29d7c-135">-WhatIf</span></span>
<span data-ttu-id="29d7c-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="29d7c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29d7c-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="29d7c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29d7c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d7c-138">CommonParameters</span></span>
<span data-ttu-id="29d7c-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29d7c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d7c-140">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29d7c-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d7c-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29d7c-141">INPUTS</span></span>

### <span data-ttu-id="29d7c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="29d7c-142">System.String</span></span>

## <span data-ttu-id="29d7c-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29d7c-143">OUTPUTS</span></span>

### <span data-ttu-id="29d7c-144">Microsoft. Azure. commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="29d7c-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="29d7c-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29d7c-145">NOTES</span></span>

## <span data-ttu-id="29d7c-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29d7c-146">RELATED LINKS</span></span>

[<span data-ttu-id="29d7c-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="29d7c-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="29d7c-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="29d7c-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="29d7c-149">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="29d7c-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
