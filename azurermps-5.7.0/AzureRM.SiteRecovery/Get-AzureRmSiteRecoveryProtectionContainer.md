---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 77F1556C-323D-49CA-BD6C-75B2D4E0F894
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
ms.openlocfilehash: d5c2032828c5d34b94af8d448155c18b6d8b06c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757214"
---
# <span data-ttu-id="e4dea-101">Get-AzureRmSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e4dea-101">Get-AzureRmSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="e4dea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4dea-102">SYNOPSIS</span></span>
<span data-ttu-id="e4dea-103">Hämtar skydds behållare för det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="e4dea-103">Gets protection containers for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4dea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4dea-104">SYNTAX</span></span>

### <span data-ttu-id="e4dea-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="e4dea-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4dea-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e4dea-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4dea-107">ByObjectWithNameLegacy</span><span class="sxs-lookup"><span data-stu-id="e4dea-107">ByObjectWithNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4dea-108">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e4dea-108">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4dea-109">ByObjectWithFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="e4dea-109">ByObjectWithFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4dea-110">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="e4dea-110">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4dea-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4dea-111">DESCRIPTION</span></span>
<span data-ttu-id="e4dea-112">Cmdleten **Get-AzureRmSiteRecoveryProtectionContainer** får skydds behållare för det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="e4dea-112">The **Get-AzureRmSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="e4dea-113">En skydds behållare är en logisk behållare för skyddade objekt, till exempel virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="e4dea-113">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="e4dea-114">Skydds principer definierar replikeringsinställningar för skyddade objekt och kan associeras med en skydds behållare och tillämpas på en skyddad entitet.</span><span class="sxs-lookup"><span data-stu-id="e4dea-114">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="e4dea-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4dea-115">EXAMPLES</span></span>

## <span data-ttu-id="e4dea-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4dea-116">PARAMETERS</span></span>

### <span data-ttu-id="e4dea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4dea-117">-DefaultProfile</span></span>
<span data-ttu-id="e4dea-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4dea-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4dea-119">-Fabric</span><span class="sxs-lookup"><span data-stu-id="e4dea-119">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName, ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4dea-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e4dea-120">-FriendlyName</span></span>
<span data-ttu-id="e4dea-121">Anger det egna namnet på skydds behållaren.</span><span class="sxs-lookup"><span data-stu-id="e4dea-121">Specifies the friendly name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName, ByObjectWithFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4dea-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e4dea-122">-Name</span></span>
<span data-ttu-id="e4dea-123">Anger namnet på skydds behållaren.</span><span class="sxs-lookup"><span data-stu-id="e4dea-123">Specifies the name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByObjectWithNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4dea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4dea-124">CommonParameters</span></span>
<span data-ttu-id="e4dea-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4dea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4dea-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4dea-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4dea-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4dea-127">INPUTS</span></span>

### <span data-ttu-id="e4dea-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e4dea-128">ASRFabric</span></span>
<span data-ttu-id="e4dea-129">Parametern ' Fabric ' godkänner värdet av typen ' ASRFabric ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e4dea-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="e4dea-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4dea-130">OUTPUTS</span></span>

### <span data-ttu-id="e4dea-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRProtectionContainer]</span><span class="sxs-lookup"><span data-stu-id="e4dea-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer]</span></span>

## <span data-ttu-id="e4dea-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4dea-132">NOTES</span></span>

## <span data-ttu-id="e4dea-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4dea-133">RELATED LINKS</span></span>

