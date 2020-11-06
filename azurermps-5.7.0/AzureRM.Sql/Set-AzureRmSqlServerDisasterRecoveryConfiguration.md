---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 588954527c76bb0f5394afe4df9e19b37c10fe0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574156"
---
# <span data-ttu-id="b79ac-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b79ac-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="b79ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b79ac-102">SYNOPSIS</span></span>
<span data-ttu-id="b79ac-103">Ändrar en konfiguration för återställning av databas server.</span><span class="sxs-lookup"><span data-stu-id="b79ac-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b79ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b79ac-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b79ac-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b79ac-105">DESCRIPTION</span></span>
<span data-ttu-id="b79ac-106">Cmdleten **set-AzureRmSqlServerDisasterRecoveryConfiguration** ändrar en återställnings konfiguration för SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="b79ac-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="b79ac-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b79ac-107">EXAMPLES</span></span>

## <span data-ttu-id="b79ac-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b79ac-108">PARAMETERS</span></span>

### <span data-ttu-id="b79ac-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="b79ac-109">-AllowDataLoss</span></span>
<span data-ttu-id="b79ac-110">Visar att Redundansåtgärden tillåter data förlust.</span><span class="sxs-lookup"><span data-stu-id="b79ac-110">Indicates that the failover operation permits data loss.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b79ac-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b79ac-111">-AsJob</span></span>
<span data-ttu-id="b79ac-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b79ac-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b79ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b79ac-113">-DefaultProfile</span></span>
<span data-ttu-id="b79ac-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b79ac-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b79ac-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="b79ac-115">-Failover</span></span>
<span data-ttu-id="b79ac-116">Anger att den här åtgärden är en redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="b79ac-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b79ac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b79ac-117">-ResourceGroupName</span></span>
<span data-ttu-id="b79ac-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b79ac-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b79ac-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b79ac-119">-ServerName</span></span>
<span data-ttu-id="b79ac-120">Anger namnet på en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="b79ac-120">Specifies the name of a SQL database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b79ac-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="b79ac-121">-VirtualEndpointName</span></span>
<span data-ttu-id="b79ac-122">Anger namnet på en virtuell slut punkt.</span><span class="sxs-lookup"><span data-stu-id="b79ac-122">Specifies the name of a virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b79ac-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b79ac-123">-Confirm</span></span>
<span data-ttu-id="b79ac-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b79ac-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b79ac-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b79ac-125">-WhatIf</span></span>
<span data-ttu-id="b79ac-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b79ac-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b79ac-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b79ac-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b79ac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b79ac-128">CommonParameters</span></span>
<span data-ttu-id="b79ac-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b79ac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b79ac-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b79ac-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b79ac-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b79ac-131">INPUTS</span></span>

### <span data-ttu-id="b79ac-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="b79ac-132">None</span></span>
<span data-ttu-id="b79ac-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b79ac-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b79ac-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b79ac-134">OUTPUTS</span></span>

## <span data-ttu-id="b79ac-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b79ac-135">NOTES</span></span>

## <span data-ttu-id="b79ac-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b79ac-136">RELATED LINKS</span></span>

[<span data-ttu-id="b79ac-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b79ac-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b79ac-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b79ac-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b79ac-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b79ac-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b79ac-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="b79ac-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
