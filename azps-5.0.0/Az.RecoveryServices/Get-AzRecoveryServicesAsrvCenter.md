---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 49adcdefac7fe3f06cfd9678137dd58cff021f52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269253"
---
# <span data-ttu-id="9f2ea-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="9f2ea-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="9f2ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f2ea-102">SYNOPSIS</span></span>
<span data-ttu-id="9f2ea-103">Hämtar information om de vCenter-servrar som är registrerade för identifiering på den konfigurations server som anges av ASR Fabric.</span><span class="sxs-lookup"><span data-stu-id="9f2ea-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="9f2ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f2ea-104">SYNTAX</span></span>

### <span data-ttu-id="9f2ea-105">ByFabricObject (standard)</span><span class="sxs-lookup"><span data-stu-id="9f2ea-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f2ea-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f2ea-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f2ea-107">ByName</span><span class="sxs-lookup"><span data-stu-id="9f2ea-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f2ea-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f2ea-108">DESCRIPTION</span></span>
<span data-ttu-id="9f2ea-109">Cmdleten **Get-AzRecoveryServicesAsrvCenter** hämtar information om de vCenter-servrar som registrerats för identifiering på den konfigurations server som anges av ASR Fabric.</span><span class="sxs-lookup"><span data-stu-id="9f2ea-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="9f2ea-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f2ea-110">EXAMPLES</span></span>

### <span data-ttu-id="9f2ea-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9f2ea-111">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

FriendlyName          : inmtest81
Server                : 10.150.209.27
Port                  : 443
Name                  : inmtest81
ID                    : /Subscriptions/xxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxx/replicationvCenters/inmtest81
FabricArmResourceName : d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9
ProcessServerId       : 526C9B6C-4039-D841-97A92FB0BD153B53
AccountId             : 2
DiscoveryStatus       : Pending
LastHeartbeat         :
```

<span data-ttu-id="9f2ea-112">Skaffa Azure Site Recovery vCenter efter infrastruktur namn och namn på vCenter.</span><span class="sxs-lookup"><span data-stu-id="9f2ea-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="9f2ea-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9f2ea-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="9f2ea-114">Skaffa Azure Site Recovery vCenter-lista efter infrastruktur namn.</span><span class="sxs-lookup"><span data-stu-id="9f2ea-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="9f2ea-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f2ea-115">PARAMETERS</span></span>

### <span data-ttu-id="9f2ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f2ea-116">-DefaultProfile</span></span>
<span data-ttu-id="9f2ea-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f2ea-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f2ea-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="9f2ea-118">-Fabric</span></span>
<span data-ttu-id="9f2ea-119">ASR Fabric-objekt som representerar konfigurations servern.</span><span class="sxs-lookup"><span data-stu-id="9f2ea-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2ea-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9f2ea-120">-Name</span></span>
<span data-ttu-id="9f2ea-121">Namn på vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="9f2ea-121">Name of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2ea-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f2ea-122">-ResourceId</span></span>
<span data-ttu-id="9f2ea-123">Anger resourceId för vCenter.</span><span class="sxs-lookup"><span data-stu-id="9f2ea-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2ea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f2ea-124">CommonParameters</span></span>
<span data-ttu-id="9f2ea-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f2ea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f2ea-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f2ea-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f2ea-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f2ea-127">INPUTS</span></span>

### <span data-ttu-id="9f2ea-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9f2ea-128">System.String</span></span>

### <span data-ttu-id="9f2ea-129">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="9f2ea-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="9f2ea-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f2ea-130">OUTPUTS</span></span>

### <span data-ttu-id="9f2ea-131">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="9f2ea-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="9f2ea-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f2ea-132">NOTES</span></span>

## <span data-ttu-id="9f2ea-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f2ea-133">RELATED LINKS</span></span>