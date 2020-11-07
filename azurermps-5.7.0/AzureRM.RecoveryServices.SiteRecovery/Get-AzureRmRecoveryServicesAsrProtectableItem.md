---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 876d30cd3c046136acc24a8492425c69fc845f3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575573"
---
# <span data-ttu-id="8962a-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8962a-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="8962a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8962a-102">SYNOPSIS</span></span>
<span data-ttu-id="8962a-103">Få skydds bara objekt i en system skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="8962a-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8962a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8962a-104">SYNTAX</span></span>

### <span data-ttu-id="8962a-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="8962a-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8962a-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="8962a-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8962a-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8962a-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8962a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8962a-108">DESCRIPTION</span></span>
<span data-ttu-id="8962a-109">Cmdleten **Get-AzureRmRecoveryServicesAsrProtectableItem** hämtar de objekt som skyddas i en behållare för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="8962a-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="8962a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8962a-110">EXAMPLES</span></span>

### <span data-ttu-id="8962a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8962a-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="8962a-112">Hämtar alla objekt som skyddas i angiven ASR-skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="8962a-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="8962a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8962a-113">Example 2</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -FriendlyName $piFriendlyName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="8962a-114">Få skydd bara objekt i angiven ASR-skydds behållare och med angivet eget namn.</span><span class="sxs-lookup"><span data-stu-id="8962a-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="8962a-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="8962a-115">Example 3</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -Name $piName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="8962a-116">Hämtar alla objekt som skyddas i angiven ASR-skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="8962a-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="8962a-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8962a-117">PARAMETERS</span></span>

### <span data-ttu-id="8962a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8962a-118">-DefaultProfile</span></span>
<span data-ttu-id="8962a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8962a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="8962a-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8962a-120">-FriendlyName</span></span>
<span data-ttu-id="8962a-121">Anger det egna namnet på det skrivskyddade ASR-objektet.</span><span class="sxs-lookup"><span data-stu-id="8962a-121">Specifies the friendly name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8962a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="8962a-122">-Name</span></span>
<span data-ttu-id="8962a-123">Anger namnet på objektet som skyddas av säkerhets system.</span><span class="sxs-lookup"><span data-stu-id="8962a-123">Specifies the name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8962a-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8962a-124">-ProtectionContainer</span></span>
<span data-ttu-id="8962a-125">Anger objekt för objektet för Azure Site Recovery-skyddet.</span><span class="sxs-lookup"><span data-stu-id="8962a-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8962a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8962a-126">CommonParameters</span></span>
<span data-ttu-id="8962a-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8962a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8962a-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8962a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8962a-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8962a-129">INPUTS</span></span>

### <span data-ttu-id="8962a-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8962a-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="8962a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8962a-131">OUTPUTS</span></span>

### <span data-ttu-id="8962a-132">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectableItem, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8962a-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8962a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8962a-133">NOTES</span></span>

## <span data-ttu-id="8962a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8962a-134">RELATED LINKS</span></span>

[<span data-ttu-id="8962a-135">Get-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="8962a-135">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="8962a-136">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="8962a-136">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)