---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 56749c265980fc40ee19b60261641f0c98c25da9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577823"
---
# <span data-ttu-id="30caa-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="30caa-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="30caa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30caa-102">SYNOPSIS</span></span>
<span data-ttu-id="30caa-103">Växlar en sekundär databas till primärt för att initiera redundans.</span><span class="sxs-lookup"><span data-stu-id="30caa-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30caa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30caa-104">SYNTAX</span></span>

### <span data-ttu-id="30caa-105">NoOptionsSet (standard)</span><span class="sxs-lookup"><span data-stu-id="30caa-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30caa-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="30caa-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30caa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30caa-107">DESCRIPTION</span></span>
<span data-ttu-id="30caa-108">Cmdleten **set-AzureRmSqlDatabaseSecondary** ändrar en sekundär databas så att den blir primär för att initiera redundans.</span><span class="sxs-lookup"><span data-stu-id="30caa-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="30caa-109">Denna cmdlet är utformad som en allmän konfigurations kommando, men är för närvarande begränsad till initiering av redundans.</span><span class="sxs-lookup"><span data-stu-id="30caa-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="30caa-110">Ange parametern *AllowDataLoss* för att initiera en Force redundans under ett avbrott.</span><span class="sxs-lookup"><span data-stu-id="30caa-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="30caa-111">Du behöver inte ange den här parametern när du utför en planerad åtgärd, till exempel en återställnings granskning.</span><span class="sxs-lookup"><span data-stu-id="30caa-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="30caa-112">I det senare fallet synkroniseras den sekundära databasen med primärt innan den ändras.</span><span class="sxs-lookup"><span data-stu-id="30caa-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="30caa-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30caa-113">EXAMPLES</span></span>

## <span data-ttu-id="30caa-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30caa-114">PARAMETERS</span></span>

### <span data-ttu-id="30caa-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="30caa-115">-AllowDataLoss</span></span>
<span data-ttu-id="30caa-116">Visar att denna redundansväxling tillåter data förlust.</span><span class="sxs-lookup"><span data-stu-id="30caa-116">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="30caa-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30caa-117">-AsJob</span></span>
<span data-ttu-id="30caa-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="30caa-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30caa-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="30caa-119">-DatabaseName</span></span>
<span data-ttu-id="30caa-120">Anger namnet på den sekundära Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="30caa-120">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="30caa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30caa-121">-DefaultProfile</span></span>
<span data-ttu-id="30caa-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="30caa-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30caa-123">-Failover</span><span class="sxs-lookup"><span data-stu-id="30caa-123">-Failover</span></span>
<span data-ttu-id="30caa-124">Anger att den här åtgärden är en redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="30caa-124">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="30caa-125">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30caa-125">-PartnerResourceGroupName</span></span>
<span data-ttu-id="30caa-126">Anger namnet på den resurs grupp som partner-Azure SQL-databasen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="30caa-126">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="30caa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30caa-127">-ResourceGroupName</span></span>
<span data-ttu-id="30caa-128">Anger namnet på den resurs grupp som den sekundära Azure SQL-databasen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="30caa-128">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="30caa-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="30caa-129">-ServerName</span></span>
<span data-ttu-id="30caa-130">Anger namnet på den SQL Server som är värd för den sekundära Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="30caa-130">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="30caa-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30caa-131">-Confirm</span></span>
<span data-ttu-id="30caa-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30caa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30caa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30caa-133">-WhatIf</span></span>
<span data-ttu-id="30caa-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30caa-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30caa-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30caa-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30caa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30caa-136">CommonParameters</span></span>
<span data-ttu-id="30caa-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30caa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30caa-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30caa-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30caa-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30caa-139">INPUTS</span></span>

### <span data-ttu-id="30caa-140">System. String</span><span class="sxs-lookup"><span data-stu-id="30caa-140">System.String</span></span>

## <span data-ttu-id="30caa-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30caa-141">OUTPUTS</span></span>

### <span data-ttu-id="30caa-142">Microsoft. Azure. commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="30caa-142">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="30caa-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30caa-143">NOTES</span></span>

## <span data-ttu-id="30caa-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30caa-144">RELATED LINKS</span></span>

[<span data-ttu-id="30caa-145">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="30caa-145">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="30caa-146">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="30caa-146">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="30caa-147">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="30caa-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
