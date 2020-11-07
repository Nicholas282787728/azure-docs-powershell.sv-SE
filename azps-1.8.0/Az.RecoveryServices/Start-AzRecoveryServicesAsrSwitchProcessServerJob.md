---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: 4f926b88214a60cc05b6eb9666e10fa8ed7bf3ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747323"
---
# <span data-ttu-id="5f782-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="5f782-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="5f782-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f782-102">SYNOPSIS</span></span>
<span data-ttu-id="5f782-103">Växla replikering från en process server till en annan för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5f782-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="5f782-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f782-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f782-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f782-105">DESCRIPTION</span></span>
<span data-ttu-id="5f782-106">Med **Start-AzRecoveryServicesAsrSwitchProcessServerJob** växlar du replikeringstrafik för de angivna virtuella datorerna eller en angiven process server till den angivna mål Server servern.</span><span class="sxs-lookup"><span data-stu-id="5f782-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="5f782-107">Används för belastnings utjämning eller byte av replikering mellan process servrar.</span><span class="sxs-lookup"><span data-stu-id="5f782-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="5f782-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f782-108">EXAMPLES</span></span>

### <span data-ttu-id="5f782-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5f782-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="5f782-110">Jobb för att spåra växel Server för allt replikerat objekt från källa till mål server.</span><span class="sxs-lookup"><span data-stu-id="5f782-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="5f782-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5f782-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="5f782-112">Jobb för att spåra växel Server för passerat replikerat objekt från källa till mål server.</span><span class="sxs-lookup"><span data-stu-id="5f782-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="5f782-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f782-113">PARAMETERS</span></span>

### <span data-ttu-id="5f782-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f782-114">-DefaultProfile</span></span>
<span data-ttu-id="5f782-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f782-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f782-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="5f782-116">-Fabric</span></span>
<span data-ttu-id="5f782-117">Site Recovery Fabric för konfigurations servern.</span><span class="sxs-lookup"><span data-stu-id="5f782-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f782-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5f782-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="5f782-119">Lista över replikerat objekt vars process Server ska bytas.</span><span class="sxs-lookup"><span data-stu-id="5f782-119">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f782-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="5f782-120">-SourceProcessServer</span></span>
<span data-ttu-id="5f782-121">Process servern för att växla mellan replikering från.</span><span class="sxs-lookup"><span data-stu-id="5f782-121">The Process server to switch replication out from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f782-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="5f782-122">-TargetProcessServer</span></span>
<span data-ttu-id="5f782-123">Process servern för att växla mellan replikeringen.</span><span class="sxs-lookup"><span data-stu-id="5f782-123">The Process server to switch replication to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f782-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5f782-124">-Confirm</span></span>
<span data-ttu-id="5f782-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5f782-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f782-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f782-126">-WhatIf</span></span>
<span data-ttu-id="5f782-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5f782-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f782-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5f782-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f782-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f782-129">CommonParameters</span></span>
<span data-ttu-id="5f782-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f782-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f782-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f782-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f782-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f782-132">INPUTS</span></span>

### <span data-ttu-id="5f782-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="5f782-133">None</span></span>

## <span data-ttu-id="5f782-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f782-134">OUTPUTS</span></span>

### <span data-ttu-id="5f782-135">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5f782-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5f782-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f782-136">NOTES</span></span>

## <span data-ttu-id="5f782-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f782-137">RELATED LINKS</span></span>
