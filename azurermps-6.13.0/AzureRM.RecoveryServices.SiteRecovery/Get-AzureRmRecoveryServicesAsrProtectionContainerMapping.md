---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: c893d256351473aa1d840cf1a7e62a960300bdf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755525"
---
# <span data-ttu-id="13712-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="13712-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="13712-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13712-102">SYNOPSIS</span></span>
<span data-ttu-id="13712-103">Hämtar mappningar för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="13712-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13712-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13712-104">SYNTAX</span></span>

### <span data-ttu-id="13712-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="13712-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13712-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="13712-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13712-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13712-107">DESCRIPTION</span></span>
<span data-ttu-id="13712-108">Cmdleten **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** hämtar information om skydds behållaren för att mappa (associeringar) i valvet för den angivna ASR-skyddsagenten.</span><span class="sxs-lookup"><span data-stu-id="13712-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="13712-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13712-109">EXAMPLES</span></span>

### <span data-ttu-id="13712-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="13712-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="13712-111">Lista över mappningar för skydds behållare för container.</span><span class="sxs-lookup"><span data-stu-id="13712-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="13712-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="13712-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

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

<span data-ttu-id="13712-113">Hämtar alla skydds behållas mappningar för den angivna skydds behållaren.</span><span class="sxs-lookup"><span data-stu-id="13712-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="13712-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13712-114">PARAMETERS</span></span>

### <span data-ttu-id="13712-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13712-115">-DefaultProfile</span></span>
<span data-ttu-id="13712-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13712-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="13712-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="13712-117">-Name</span></span>
<span data-ttu-id="13712-118">Anger namnet på den mappning för skydds behållare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="13712-118">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="13712-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="13712-119">-ProtectionContainer</span></span>
<span data-ttu-id="13712-120">Hämta mappningar för skydds behållare för det angivna objektet för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="13712-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

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

### <span data-ttu-id="13712-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13712-121">CommonParameters</span></span>
<span data-ttu-id="13712-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13712-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13712-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13712-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13712-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13712-124">INPUTS</span></span>

### <span data-ttu-id="13712-125">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="13712-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="13712-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13712-126">OUTPUTS</span></span>

### <span data-ttu-id="13712-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="13712-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="13712-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13712-128">NOTES</span></span>

## <span data-ttu-id="13712-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13712-129">RELATED LINKS</span></span>

[<span data-ttu-id="13712-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="13712-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="13712-131">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="13712-131">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
