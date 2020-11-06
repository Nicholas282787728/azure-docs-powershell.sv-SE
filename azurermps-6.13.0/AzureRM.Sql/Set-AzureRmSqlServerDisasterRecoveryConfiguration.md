---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 19f7d8adf7e8eae48bb85c19c9f01c61dc741da0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576043"
---
# <span data-ttu-id="799eb-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="799eb-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="799eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="799eb-102">SYNOPSIS</span></span>
<span data-ttu-id="799eb-103">Ändrar en konfiguration för återställning av databas server.</span><span class="sxs-lookup"><span data-stu-id="799eb-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="799eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="799eb-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="799eb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="799eb-105">DESCRIPTION</span></span>
<span data-ttu-id="799eb-106">Cmdleten **set-AzureRmSqlServerDisasterRecoveryConfiguration** ändrar en återställnings konfiguration för SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="799eb-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="799eb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="799eb-107">EXAMPLES</span></span>

## <span data-ttu-id="799eb-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="799eb-108">PARAMETERS</span></span>

### <span data-ttu-id="799eb-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="799eb-109">-AllowDataLoss</span></span>
<span data-ttu-id="799eb-110">Visar att Redundansåtgärden tillåter data förlust.</span><span class="sxs-lookup"><span data-stu-id="799eb-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="799eb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="799eb-111">-AsJob</span></span>
<span data-ttu-id="799eb-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="799eb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="799eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="799eb-113">-DefaultProfile</span></span>
<span data-ttu-id="799eb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="799eb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="799eb-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="799eb-115">-Failover</span></span>
<span data-ttu-id="799eb-116">Anger att den här åtgärden är en redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="799eb-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="799eb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="799eb-117">-ResourceGroupName</span></span>
<span data-ttu-id="799eb-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="799eb-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="799eb-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="799eb-119">-ServerName</span></span>
<span data-ttu-id="799eb-120">Anger namnet på en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="799eb-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="799eb-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="799eb-121">-VirtualEndpointName</span></span>
<span data-ttu-id="799eb-122">Anger namnet på en virtuell slut punkt.</span><span class="sxs-lookup"><span data-stu-id="799eb-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="799eb-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="799eb-123">-Confirm</span></span>
<span data-ttu-id="799eb-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="799eb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="799eb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="799eb-125">-WhatIf</span></span>
<span data-ttu-id="799eb-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="799eb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="799eb-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="799eb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="799eb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="799eb-128">CommonParameters</span></span>
<span data-ttu-id="799eb-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="799eb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="799eb-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="799eb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="799eb-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="799eb-131">INPUTS</span></span>

### <span data-ttu-id="799eb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="799eb-132">System.String</span></span>

## <span data-ttu-id="799eb-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="799eb-133">OUTPUTS</span></span>

### <span data-ttu-id="799eb-134">Microsoft. Azure. commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="799eb-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="799eb-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="799eb-135">NOTES</span></span>

## <span data-ttu-id="799eb-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="799eb-136">RELATED LINKS</span></span>

[<span data-ttu-id="799eb-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="799eb-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="799eb-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="799eb-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="799eb-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="799eb-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="799eb-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="799eb-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
