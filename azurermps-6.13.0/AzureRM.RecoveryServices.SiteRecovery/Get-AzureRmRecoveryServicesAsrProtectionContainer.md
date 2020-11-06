---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 6572fb6f98e06d03d698f75948ac4a7a38f2e785
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575141"
---
# <span data-ttu-id="d03ed-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d03ed-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="d03ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d03ed-102">SYNOPSIS</span></span>
<span data-ttu-id="d03ed-103">Får ASR-skydds behållare i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="d03ed-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d03ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d03ed-104">SYNTAX</span></span>

### <span data-ttu-id="d03ed-105">ByFabricObject (standard)</span><span class="sxs-lookup"><span data-stu-id="d03ed-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d03ed-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d03ed-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d03ed-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d03ed-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d03ed-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d03ed-108">DESCRIPTION</span></span>
<span data-ttu-id="d03ed-109">Cmdleten **Get-AzureRmRecoveryServicesAsrProtectionContainer** får Azure Site Recovery-behållare i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="d03ed-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="d03ed-110">En skydds behållare är en logisk behållare för skydd bara (upptäckta) och skyddade objekt, till exempel virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="d03ed-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="d03ed-111">Replikeringsprinciper definierar replikeringsinställningar för skyddade objekt och kan associeras med en skydds behållare och tillämpas på ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="d03ed-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="d03ed-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d03ed-112">EXAMPLES</span></span>

### <span data-ttu-id="d03ed-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d03ed-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="d03ed-114">Lista med skydds behållare i Fabric $fabric.</span><span class="sxs-lookup"><span data-stu-id="d03ed-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="d03ed-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d03ed-115">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="d03ed-116">Skydds behållare i Fabric $fabric med namn.</span><span class="sxs-lookup"><span data-stu-id="d03ed-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="d03ed-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="d03ed-117">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="d03ed-118">Skydds behållare i Fabric $fabric med eget namn.</span><span class="sxs-lookup"><span data-stu-id="d03ed-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="d03ed-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d03ed-119">PARAMETERS</span></span>

### <span data-ttu-id="d03ed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d03ed-120">-DefaultProfile</span></span>
<span data-ttu-id="d03ed-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d03ed-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d03ed-122">-Fabric</span><span class="sxs-lookup"><span data-stu-id="d03ed-122">-Fabric</span></span>
<span data-ttu-id="d03ed-123">Leta efter skydds behållaren i den angivna ASR-fabricen.</span><span class="sxs-lookup"><span data-stu-id="d03ed-123">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d03ed-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d03ed-124">-FriendlyName</span></span>
<span data-ttu-id="d03ed-125">Anger det egna namnet på den systemsystem för ASR-skydd som du letar efter.</span><span class="sxs-lookup"><span data-stu-id="d03ed-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="d03ed-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="d03ed-126">-Name</span></span>
<span data-ttu-id="d03ed-127">Anger namnet på den behållare för automatisk system återställning som ska sökas efter.</span><span class="sxs-lookup"><span data-stu-id="d03ed-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="d03ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d03ed-128">CommonParameters</span></span>
<span data-ttu-id="d03ed-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d03ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d03ed-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d03ed-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d03ed-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d03ed-131">INPUTS</span></span>

### <span data-ttu-id="d03ed-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d03ed-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d03ed-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d03ed-133">OUTPUTS</span></span>

### <span data-ttu-id="d03ed-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d03ed-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d03ed-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d03ed-135">NOTES</span></span>

## <span data-ttu-id="d03ed-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d03ed-136">RELATED LINKS</span></span>
