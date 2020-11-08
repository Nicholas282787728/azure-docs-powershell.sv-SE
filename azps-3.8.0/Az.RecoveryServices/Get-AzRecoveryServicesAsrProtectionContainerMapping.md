---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 7d3b5735cc52ae190cc16c93ad9806a9f47b452d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088339"
---
# <span data-ttu-id="4cebe-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4cebe-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="4cebe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cebe-102">SYNOPSIS</span></span>
<span data-ttu-id="4cebe-103">Hämtar mappningar för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="4cebe-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

## <span data-ttu-id="4cebe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cebe-104">SYNTAX</span></span>

### <span data-ttu-id="4cebe-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="4cebe-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cebe-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4cebe-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cebe-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cebe-107">DESCRIPTION</span></span>
<span data-ttu-id="4cebe-108">Cmdleten **Get-AzRecoveryServicesAsrProtectionContainerMapping** hämtar information om skydds behållaren för att mappa (associeringar) i valvet för den angivna ASR-skyddsagenten.</span><span class="sxs-lookup"><span data-stu-id="4cebe-108">The **Get-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="4cebe-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cebe-109">EXAMPLES</span></span>

### <span data-ttu-id="4cebe-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4cebe-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="4cebe-111">Lista över mappningar för skydds behållare för container.</span><span class="sxs-lookup"><span data-stu-id="4cebe-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="4cebe-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4cebe-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

Name                                  : pcmmapping
ID                                    : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replica
                                        tionProtectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectionContainerMappings/pcmmapping
Health                                : Normal
HealthErrorDetails                    : {}
PolicyFriendlyName                    : V2aTestPolicy
PolicyId                              : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationPolicies/V2aTestPolicy
SourceFabricFriendlyName              : V2A-W2K12-400
SourceProtectionContainerFriendlyName : V2A-W2K12-400
State                                 : Paired
TargetFabricFriendlyName              : Microsoft Azure
TargetProtectionContainerFriendlyName : Microsoft Azure
TargetProtectionContainerId           : Microsoft Azure
```

<span data-ttu-id="4cebe-113">Hämtar alla skydds behållas mappningar för den angivna skydds behållaren.</span><span class="sxs-lookup"><span data-stu-id="4cebe-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="4cebe-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cebe-114">PARAMETERS</span></span>

### <span data-ttu-id="4cebe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cebe-115">-DefaultProfile</span></span>
<span data-ttu-id="4cebe-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4cebe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4cebe-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="4cebe-117">-Name</span></span>
<span data-ttu-id="4cebe-118">Anger namnet på den mappning för skydds behållare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="4cebe-118">Specifies the name of the protection container mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cebe-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4cebe-119">-ProtectionContainer</span></span>
<span data-ttu-id="4cebe-120">Hämta mappningar för skydds behållare för det angivna objektet för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="4cebe-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cebe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cebe-121">CommonParameters</span></span>
<span data-ttu-id="4cebe-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cebe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cebe-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cebe-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cebe-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cebe-124">INPUTS</span></span>

### <span data-ttu-id="4cebe-125">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4cebe-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="4cebe-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cebe-126">OUTPUTS</span></span>

### <span data-ttu-id="4cebe-127">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4cebe-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="4cebe-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cebe-128">NOTES</span></span>

## <span data-ttu-id="4cebe-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cebe-129">RELATED LINKS</span></span>

[<span data-ttu-id="4cebe-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4cebe-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="4cebe-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4cebe-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
