---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 9e0af4c5110fe0732782293eb9d8c67fb7d89600
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927190"
---
# <span data-ttu-id="4bc0f-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4bc0f-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="4bc0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4bc0f-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc0f-103">Växlar en sekundär databas till primärt för att initiera redundans.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="4bc0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4bc0f-104">SYNTAX</span></span>

### <span data-ttu-id="4bc0f-105">NoOptionsSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4bc0f-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bc0f-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="4bc0f-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bc0f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4bc0f-107">DESCRIPTION</span></span>
<span data-ttu-id="4bc0f-108">Cmdleten **set-AzSqlDatabaseSecondary** ändrar en sekundär databas så att den blir primär för att initiera redundans.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="4bc0f-109">Denna cmdlet är utformad som en allmän konfigurations kommando, men är för närvarande begränsad till initiering av redundans.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="4bc0f-110">Ange parametern *AllowDataLoss* för att initiera en Force redundans under ett avbrott.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="4bc0f-111">Du behöver inte ange den här parametern när du utför en planerad åtgärd, till exempel en återställnings granskning.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="4bc0f-112">I det senare fallet synkroniseras den sekundära databasen med primärt innan den ändras.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="4bc0f-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4bc0f-113">EXAMPLES</span></span>

### <span data-ttu-id="4bc0f-114">1: initiera en planerad redundans</span><span class="sxs-lookup"><span data-stu-id="4bc0f-114">1: Initiate a planned failover</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="4bc0f-115">2: initiera en framtvingad redundans (med potentiell data förlust)</span><span class="sxs-lookup"><span data-stu-id="4bc0f-115">2: Initiate a forced failover (with potential data loss)</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="4bc0f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4bc0f-116">PARAMETERS</span></span>

### <span data-ttu-id="4bc0f-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="4bc0f-117">-AllowDataLoss</span></span>
<span data-ttu-id="4bc0f-118">Visar att denna redundansväxling tillåter data förlust.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-118">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="4bc0f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bc0f-119">-AsJob</span></span>
<span data-ttu-id="4bc0f-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4bc0f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bc0f-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4bc0f-121">-DatabaseName</span></span>
<span data-ttu-id="4bc0f-122">Anger namnet på den sekundära Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="4bc0f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc0f-123">-DefaultProfile</span></span>
<span data-ttu-id="4bc0f-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4bc0f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4bc0f-125">-Failover</span><span class="sxs-lookup"><span data-stu-id="4bc0f-125">-Failover</span></span>
<span data-ttu-id="4bc0f-126">Anger att den här åtgärden är en redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-126">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="4bc0f-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc0f-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="4bc0f-128">Anger namnet på den resurs grupp som partner-Azure SQL-databasen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="4bc0f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc0f-129">-ResourceGroupName</span></span>
<span data-ttu-id="4bc0f-130">Anger namnet på den resurs grupp som den sekundära Azure SQL-databasen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="4bc0f-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4bc0f-131">-ServerName</span></span>
<span data-ttu-id="4bc0f-132">Anger namnet på den SQL Server som är värd för den sekundära Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="4bc0f-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4bc0f-133">-Confirm</span></span>
<span data-ttu-id="4bc0f-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bc0f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bc0f-135">-WhatIf</span></span>
<span data-ttu-id="4bc0f-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bc0f-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bc0f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc0f-138">CommonParameters</span></span>
<span data-ttu-id="4bc0f-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bc0f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc0f-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bc0f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc0f-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4bc0f-141">INPUTS</span></span>

### <span data-ttu-id="4bc0f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4bc0f-142">System.String</span></span>

## <span data-ttu-id="4bc0f-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4bc0f-143">OUTPUTS</span></span>

### <span data-ttu-id="4bc0f-144">Microsoft. Azure. commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="4bc0f-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="4bc0f-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4bc0f-145">NOTES</span></span>

## <span data-ttu-id="4bc0f-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4bc0f-146">RELATED LINKS</span></span>

[<span data-ttu-id="4bc0f-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4bc0f-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="4bc0f-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4bc0f-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="4bc0f-149">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="4bc0f-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
