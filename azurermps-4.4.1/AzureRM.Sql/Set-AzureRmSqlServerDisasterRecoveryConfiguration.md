---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 196608c24e31daad500fbf9b8aae1945550bb3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758269"
---
# <span data-ttu-id="389d8-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="389d8-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="389d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="389d8-102">SYNOPSIS</span></span>
<span data-ttu-id="389d8-103">Ändrar en konfiguration för återställning av databas server.</span><span class="sxs-lookup"><span data-stu-id="389d8-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="389d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="389d8-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="389d8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="389d8-105">DESCRIPTION</span></span>
<span data-ttu-id="389d8-106">Cmdleten **set-AzureRmSqlServerDisasterRecoveryConfiguration** ändrar en återställnings konfiguration för SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="389d8-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="389d8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="389d8-107">EXAMPLES</span></span>

## <span data-ttu-id="389d8-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="389d8-108">PARAMETERS</span></span>

### <span data-ttu-id="389d8-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="389d8-109">-AllowDataLoss</span></span>
<span data-ttu-id="389d8-110">Visar att Redundansåtgärden tillåter data förlust.</span><span class="sxs-lookup"><span data-stu-id="389d8-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="389d8-111">-Failover</span><span class="sxs-lookup"><span data-stu-id="389d8-111">-Failover</span></span>
<span data-ttu-id="389d8-112">Anger att den här åtgärden är en redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="389d8-112">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="389d8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="389d8-113">-ResourceGroupName</span></span>
<span data-ttu-id="389d8-114">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="389d8-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="389d8-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="389d8-115">-ServerName</span></span>
<span data-ttu-id="389d8-116">Anger namnet på en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="389d8-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="389d8-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="389d8-117">-VirtualEndpointName</span></span>
<span data-ttu-id="389d8-118">Anger namnet på en virtuell slut punkt.</span><span class="sxs-lookup"><span data-stu-id="389d8-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="389d8-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="389d8-119">-Confirm</span></span>
<span data-ttu-id="389d8-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="389d8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="389d8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="389d8-121">-WhatIf</span></span>
<span data-ttu-id="389d8-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="389d8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="389d8-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="389d8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="389d8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="389d8-124">-DefaultProfile</span></span>
<span data-ttu-id="389d8-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="389d8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="389d8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="389d8-126">CommonParameters</span></span>
<span data-ttu-id="389d8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="389d8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="389d8-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="389d8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="389d8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="389d8-129">INPUTS</span></span>

## <span data-ttu-id="389d8-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="389d8-130">OUTPUTS</span></span>

## <span data-ttu-id="389d8-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="389d8-131">NOTES</span></span>

## <span data-ttu-id="389d8-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="389d8-132">RELATED LINKS</span></span>

[<span data-ttu-id="389d8-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="389d8-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="389d8-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="389d8-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="389d8-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="389d8-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="389d8-136">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="389d8-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
