---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: be16ff2145a4442861fd985dfbb55da63f010e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574194"
---
# <span data-ttu-id="30786-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="30786-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="30786-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30786-102">SYNOPSIS</span></span>
<span data-ttu-id="30786-103">Växla replikering från en process server till en annan för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="30786-103">Switch replication from one Process server to another for load balancing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30786-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30786-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric>
 -SourceProcessServer <ASRProcessServer> -TargetProcessServer <ASRProcessServer>
 [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30786-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30786-105">DESCRIPTION</span></span>
<span data-ttu-id="30786-106">Med **Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** växlar du replikeringstrafik för de angivna virtuella datorerna eller en angiven process server till den angivna mål Server servern.</span><span class="sxs-lookup"><span data-stu-id="30786-106">The **Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="30786-107">Används för belastnings utjämning eller byte av replikering mellan process servrar.</span><span class="sxs-lookup"><span data-stu-id="30786-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="30786-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30786-108">EXAMPLES</span></span>

### <span data-ttu-id="30786-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="30786-109">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="30786-110">Jobb för att spåra växel Server för allt replikerat objekt från källa till mål server.</span><span class="sxs-lookup"><span data-stu-id="30786-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="30786-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="30786-111">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="30786-112">Jobb för att spåra växel Server för passerat replikerat objekt från källa till mål server.</span><span class="sxs-lookup"><span data-stu-id="30786-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="30786-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30786-113">PARAMETERS</span></span>

### <span data-ttu-id="30786-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30786-114">-Confirm</span></span>
<span data-ttu-id="30786-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30786-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30786-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30786-116">-DefaultProfile</span></span>
<span data-ttu-id="30786-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30786-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30786-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="30786-118">-Fabric</span></span>
<span data-ttu-id="30786-119">Site Recovery Fabric för konfigurations servern.</span><span class="sxs-lookup"><span data-stu-id="30786-119">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30786-120">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="30786-120">-ReplicationProtectedItem</span></span>
<span data-ttu-id="30786-121">Lista över replikerat objekt vars process Server ska bytas.</span><span class="sxs-lookup"><span data-stu-id="30786-121">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30786-122">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="30786-122">-SourceProcessServer</span></span>
<span data-ttu-id="30786-123">Process servern för att växla mellan replikering från.</span><span class="sxs-lookup"><span data-stu-id="30786-123">The Process server to switch replication out from.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30786-124">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="30786-124">-TargetProcessServer</span></span>
<span data-ttu-id="30786-125">Process servern för att växla mellan replikeringen.</span><span class="sxs-lookup"><span data-stu-id="30786-125">The Process server to switch replication to.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30786-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30786-126">-WhatIf</span></span>
<span data-ttu-id="30786-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30786-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30786-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30786-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30786-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30786-129">CommonParameters</span></span>
<span data-ttu-id="30786-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30786-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30786-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30786-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30786-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30786-132">INPUTS</span></span>

### <span data-ttu-id="30786-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="30786-133">None</span></span>

## <span data-ttu-id="30786-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30786-134">OUTPUTS</span></span>

### <span data-ttu-id="30786-135">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="30786-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="30786-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30786-136">NOTES</span></span>

## <span data-ttu-id="30786-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30786-137">RELATED LINKS</span></span>
