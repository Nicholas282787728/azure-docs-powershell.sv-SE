---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 689f432f117e67a3770518a3b2e86f1678f3662b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579479"
---
# <span data-ttu-id="28ca6-101">Get-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="28ca6-101">Get-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="28ca6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="28ca6-103">Hämtar information om de vCenter-servrar som är registrerade för identifiering på den konfigurations server som anges av ASR Fabric.</span><span class="sxs-lookup"><span data-stu-id="28ca6-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28ca6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28ca6-104">SYNTAX</span></span>

### <span data-ttu-id="28ca6-105">ByFabricObject (standard)</span><span class="sxs-lookup"><span data-stu-id="28ca6-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28ca6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="28ca6-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28ca6-107">ByName</span><span class="sxs-lookup"><span data-stu-id="28ca6-107">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28ca6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28ca6-108">DESCRIPTION</span></span>
<span data-ttu-id="28ca6-109">Cmdleten **Get-AzureRmRecoveryServicesAsrvCenter** hämtar information om de vCenter-servrar som registrerats för identifiering på den konfigurations server som anges av ASR Fabric.</span><span class="sxs-lookup"><span data-stu-id="28ca6-109">The **Get-AzureRmRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="28ca6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28ca6-110">EXAMPLES</span></span>

### <span data-ttu-id="28ca6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="28ca6-111">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

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

<span data-ttu-id="28ca6-112">Skaffa Azure Site Recovery vCenter efter infrastruktur namn och namn på vCenter.</span><span class="sxs-lookup"><span data-stu-id="28ca6-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="28ca6-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="28ca6-113">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="28ca6-114">Skaffa Azure Site Recovery vCenter-lista efter infrastruktur namn.</span><span class="sxs-lookup"><span data-stu-id="28ca6-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="28ca6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28ca6-115">PARAMETERS</span></span>

### <span data-ttu-id="28ca6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ca6-116">-DefaultProfile</span></span>
<span data-ttu-id="28ca6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="28ca6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28ca6-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="28ca6-118">-Fabric</span></span>
<span data-ttu-id="28ca6-119">ASR Fabric-objekt som representerar konfigurations servern.</span><span class="sxs-lookup"><span data-stu-id="28ca6-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28ca6-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="28ca6-120">-Name</span></span>
<span data-ttu-id="28ca6-121">Namn på vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="28ca6-121">Name of the vCenter server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ca6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28ca6-122">-ResourceId</span></span>
<span data-ttu-id="28ca6-123">Anger resourceId för vCenter.</span><span class="sxs-lookup"><span data-stu-id="28ca6-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28ca6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ca6-124">CommonParameters</span></span>
<span data-ttu-id="28ca6-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28ca6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ca6-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28ca6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ca6-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28ca6-127">INPUTS</span></span>

### <span data-ttu-id="28ca6-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="28ca6-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="28ca6-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28ca6-129">OUTPUTS</span></span>

### <span data-ttu-id="28ca6-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRvCenter, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 0.1.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="28ca6-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="28ca6-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28ca6-131">NOTES</span></span>

## <span data-ttu-id="28ca6-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28ca6-132">RELATED LINKS</span></span>
