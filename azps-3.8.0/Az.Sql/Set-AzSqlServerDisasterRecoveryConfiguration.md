---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: c49eb386265dff2650ba9bdb0882d25be98fca0c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927138"
---
# <span data-ttu-id="d3877-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3877-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="d3877-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3877-102">SYNOPSIS</span></span>
<span data-ttu-id="d3877-103">Ändrar en konfiguration för återställning av databas server.</span><span class="sxs-lookup"><span data-stu-id="d3877-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="d3877-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3877-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3877-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3877-105">DESCRIPTION</span></span>
<span data-ttu-id="d3877-106">Cmdleten **set-AzSqlServerDisasterRecoveryConfiguration** ändrar en återställnings konfiguration för SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="d3877-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="d3877-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3877-107">EXAMPLES</span></span>

## <span data-ttu-id="d3877-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3877-108">PARAMETERS</span></span>

### <span data-ttu-id="d3877-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="d3877-109">-AllowDataLoss</span></span>
<span data-ttu-id="d3877-110">Visar att Redundansåtgärden tillåter data förlust.</span><span class="sxs-lookup"><span data-stu-id="d3877-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="d3877-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3877-111">-AsJob</span></span>
<span data-ttu-id="d3877-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d3877-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3877-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3877-113">-DefaultProfile</span></span>
<span data-ttu-id="d3877-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d3877-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3877-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="d3877-115">-Failover</span></span>
<span data-ttu-id="d3877-116">Anger att den här åtgärden är en redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="d3877-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3877-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3877-117">-ResourceGroupName</span></span>
<span data-ttu-id="d3877-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d3877-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d3877-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d3877-119">-ServerName</span></span>
<span data-ttu-id="d3877-120">Anger namnet på en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="d3877-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="d3877-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="d3877-121">-VirtualEndpointName</span></span>
<span data-ttu-id="d3877-122">Anger namnet på en virtuell slut punkt.</span><span class="sxs-lookup"><span data-stu-id="d3877-122">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3877-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d3877-123">-Confirm</span></span>
<span data-ttu-id="d3877-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d3877-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3877-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3877-125">-WhatIf</span></span>
<span data-ttu-id="d3877-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d3877-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3877-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d3877-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3877-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3877-128">CommonParameters</span></span>
<span data-ttu-id="d3877-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3877-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3877-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3877-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3877-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3877-131">INPUTS</span></span>

### <span data-ttu-id="d3877-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d3877-132">System.String</span></span>

## <span data-ttu-id="d3877-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3877-133">OUTPUTS</span></span>

### <span data-ttu-id="d3877-134">Microsoft. Azure. commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="d3877-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="d3877-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3877-135">NOTES</span></span>

## <span data-ttu-id="d3877-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3877-136">RELATED LINKS</span></span>

[<span data-ttu-id="d3877-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3877-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d3877-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3877-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d3877-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3877-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d3877-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="d3877-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)