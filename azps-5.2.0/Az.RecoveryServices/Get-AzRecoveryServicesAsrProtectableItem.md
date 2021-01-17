---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: c9c50e26e99493fb693b8bded693bceb24f5a40f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413504"
---
# <span data-ttu-id="8b244-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8b244-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="8b244-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b244-102">SYNOPSIS</span></span>
<span data-ttu-id="8b244-103">Få skydds bara objekt i en system skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="8b244-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="8b244-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b244-104">SYNTAX</span></span>

### <span data-ttu-id="8b244-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="8b244-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b244-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="8b244-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b244-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8b244-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b244-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b244-108">DESCRIPTION</span></span>
<span data-ttu-id="8b244-109">Cmdleten **Get-AzRecoveryServicesAsrProtectableItem** hämtar de objekt som skyddas i en behållare för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="8b244-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="8b244-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b244-110">EXAMPLES</span></span>

### <span data-ttu-id="8b244-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8b244-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="8b244-112">Hämtar alla objekt som skyddas i angiven ASR-skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="8b244-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="8b244-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8b244-113">Example 2</span></span>
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

<span data-ttu-id="8b244-114">Få skydd bara objekt i angiven ASR-skydds behållare och med angivet eget namn.</span><span class="sxs-lookup"><span data-stu-id="8b244-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="8b244-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="8b244-115">Example 3</span></span>
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

<span data-ttu-id="8b244-116">Hämtar alla objekt som skyddas i angiven ASR-skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="8b244-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="8b244-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b244-117">PARAMETERS</span></span>

### <span data-ttu-id="8b244-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b244-118">-DefaultProfile</span></span>
<span data-ttu-id="8b244-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b244-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8b244-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8b244-120">-FriendlyName</span></span>
<span data-ttu-id="8b244-121">Anger det egna namnet på det skrivskyddade ASR-objektet.</span><span class="sxs-lookup"><span data-stu-id="8b244-121">Specifies the friendly name of the ASR protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b244-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b244-122">-Name</span></span>
<span data-ttu-id="8b244-123">Anger namnet på objektet som skyddas av säkerhets system.</span><span class="sxs-lookup"><span data-stu-id="8b244-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="8b244-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8b244-124">-ProtectionContainer</span></span>
<span data-ttu-id="8b244-125">Anger objekt för objektet för Azure Site Recovery-skyddet.</span><span class="sxs-lookup"><span data-stu-id="8b244-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="8b244-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b244-126">CommonParameters</span></span>
<span data-ttu-id="8b244-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b244-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b244-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b244-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b244-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b244-129">INPUTS</span></span>

### <span data-ttu-id="8b244-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8b244-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="8b244-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b244-131">OUTPUTS</span></span>

### <span data-ttu-id="8b244-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8b244-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="8b244-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b244-133">NOTES</span></span>

## <span data-ttu-id="8b244-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b244-134">RELATED LINKS</span></span>

[<span data-ttu-id="8b244-135">Get-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="8b244-135">Get-AzRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="8b244-136">Set-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="8b244-136">Set-AzRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzRecoveryServicesAsrProtectionEntity.md)
