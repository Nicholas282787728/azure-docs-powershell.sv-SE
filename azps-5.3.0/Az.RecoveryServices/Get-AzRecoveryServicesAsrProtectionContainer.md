---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 6db09c69d112e2638026fde97d586f7945f0508e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523999"
---
# <span data-ttu-id="37cd8-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="37cd8-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="37cd8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="37cd8-103">Får ASR-skydds behållare i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="37cd8-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="37cd8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37cd8-104">SYNTAX</span></span>

### <span data-ttu-id="37cd8-105">ByFabricObject (standard)</span><span class="sxs-lookup"><span data-stu-id="37cd8-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37cd8-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="37cd8-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37cd8-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="37cd8-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37cd8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37cd8-108">DESCRIPTION</span></span>
<span data-ttu-id="37cd8-109">Cmdleten **Get-AzRecoveryServicesAsrProtectionContainer** får Azure Site Recovery-behållare i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="37cd8-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="37cd8-110">En skydds behållare är en logisk behållare för skydd bara (upptäckta) och skyddade objekt, till exempel virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="37cd8-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="37cd8-111">Replikeringsprinciper definierar replikeringsinställningar för skyddade objekt och kan associeras med en skydds behållare och tillämpas på ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="37cd8-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="37cd8-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37cd8-112">EXAMPLES</span></span>

### <span data-ttu-id="37cd8-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="37cd8-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="37cd8-114">Lista med skydds behållare i Fabric $fabric.</span><span class="sxs-lookup"><span data-stu-id="37cd8-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="37cd8-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="37cd8-115">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
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

<span data-ttu-id="37cd8-116">Skydds behållare i Fabric $fabric med namn.</span><span class="sxs-lookup"><span data-stu-id="37cd8-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="37cd8-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="37cd8-117">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
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

<span data-ttu-id="37cd8-118">Skydds behållare i Fabric $fabric med eget namn.</span><span class="sxs-lookup"><span data-stu-id="37cd8-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="37cd8-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37cd8-119">PARAMETERS</span></span>

### <span data-ttu-id="37cd8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37cd8-120">-DefaultProfile</span></span>
<span data-ttu-id="37cd8-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37cd8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="37cd8-122">-Fabric</span><span class="sxs-lookup"><span data-stu-id="37cd8-122">-Fabric</span></span>
<span data-ttu-id="37cd8-123">Leta efter skydds behållaren i den angivna ASR-fabricen.</span><span class="sxs-lookup"><span data-stu-id="37cd8-123">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="37cd8-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="37cd8-124">-FriendlyName</span></span>
<span data-ttu-id="37cd8-125">Anger det egna namnet på den systemsystem för ASR-skydd som du letar efter.</span><span class="sxs-lookup"><span data-stu-id="37cd8-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="37cd8-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="37cd8-126">-Name</span></span>
<span data-ttu-id="37cd8-127">Anger namnet på den behållare för automatisk system återställning som ska sökas efter.</span><span class="sxs-lookup"><span data-stu-id="37cd8-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="37cd8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37cd8-128">CommonParameters</span></span>
<span data-ttu-id="37cd8-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37cd8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37cd8-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37cd8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37cd8-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37cd8-131">INPUTS</span></span>

### <span data-ttu-id="37cd8-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="37cd8-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="37cd8-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37cd8-133">OUTPUTS</span></span>

### <span data-ttu-id="37cd8-134">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="37cd8-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="37cd8-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37cd8-135">NOTES</span></span>

## <span data-ttu-id="37cd8-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37cd8-136">RELATED LINKS</span></span>
