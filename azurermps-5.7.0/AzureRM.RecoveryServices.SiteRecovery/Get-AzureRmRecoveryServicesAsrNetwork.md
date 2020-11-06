---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 34977acc0889a3fa557af7dfc9f02d6937e22fde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575575"
---
# <span data-ttu-id="08c0b-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="08c0b-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="08c0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="08c0b-103">Hämtar information om nätverken som hanteras av webbplats återställning för det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="08c0b-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08c0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08c0b-104">SYNTAX</span></span>

### <span data-ttu-id="08c0b-105">ByFabricObject (standard)</span><span class="sxs-lookup"><span data-stu-id="08c0b-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08c0b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="08c0b-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08c0b-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="08c0b-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08c0b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08c0b-108">DESCRIPTION</span></span>
<span data-ttu-id="08c0b-109">Cmdleten **Get-AzureRmRecoveryServicesAsrNetwork** hämtar information om Azure Site Recovery-nätverk för det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="08c0b-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="08c0b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08c0b-110">EXAMPLES</span></span>

### <span data-ttu-id="08c0b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="08c0b-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="08c0b-112">Hämtar alla kända nätverk i angiven infrastruktur resurs.</span><span class="sxs-lookup"><span data-stu-id="08c0b-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="08c0b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08c0b-113">PARAMETERS</span></span>

### <span data-ttu-id="08c0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c0b-114">-DefaultProfile</span></span>
<span data-ttu-id="08c0b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08c0b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="08c0b-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="08c0b-116">-Fabric</span></span>
<span data-ttu-id="08c0b-117">ASR Fabric-objekt</span><span class="sxs-lookup"><span data-stu-id="08c0b-117">ASR fabric object</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08c0b-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="08c0b-118">-FriendlyName</span></span>
<span data-ttu-id="08c0b-119">Eget namn på systemets ASR-objekt.</span><span class="sxs-lookup"><span data-stu-id="08c0b-119">Friendly name of network ASR object.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08c0b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="08c0b-120">-Name</span></span>
<span data-ttu-id="08c0b-121">Namn på nätverkets ASR-objekt.</span><span class="sxs-lookup"><span data-stu-id="08c0b-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="08c0b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c0b-122">CommonParameters</span></span>
<span data-ttu-id="08c0b-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08c0b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c0b-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08c0b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c0b-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08c0b-125">INPUTS</span></span>

### <span data-ttu-id="08c0b-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="08c0b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="08c0b-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08c0b-127">OUTPUTS</span></span>

### <span data-ttu-id="08c0b-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetwork, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="08c0b-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="08c0b-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08c0b-129">NOTES</span></span>

## <span data-ttu-id="08c0b-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08c0b-130">RELATED LINKS</span></span>
