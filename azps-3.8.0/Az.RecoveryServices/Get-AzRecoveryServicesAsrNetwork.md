---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925785"
---
# <span data-ttu-id="c40b7-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="c40b7-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="c40b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c40b7-102">SYNOPSIS</span></span>
<span data-ttu-id="c40b7-103">Hämtar information om nätverken som hanteras av webbplats återställning för det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="c40b7-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="c40b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c40b7-104">SYNTAX</span></span>

### <span data-ttu-id="c40b7-105">ByFabricObject (standard)</span><span class="sxs-lookup"><span data-stu-id="c40b7-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c40b7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c40b7-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c40b7-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c40b7-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c40b7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c40b7-108">DESCRIPTION</span></span>
<span data-ttu-id="c40b7-109">Cmdleten **Get-AzRecoveryServicesAsrNetwork** hämtar information om Azure Site Recovery-nätverk för det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="c40b7-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c40b7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c40b7-110">EXAMPLES</span></span>

### <span data-ttu-id="c40b7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c40b7-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="c40b7-112">Hämtar alla kända nätverk i angiven infrastruktur resurs.</span><span class="sxs-lookup"><span data-stu-id="c40b7-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="c40b7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c40b7-113">PARAMETERS</span></span>

### <span data-ttu-id="c40b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c40b7-114">-DefaultProfile</span></span>
<span data-ttu-id="c40b7-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c40b7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c40b7-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="c40b7-116">-Fabric</span></span>
<span data-ttu-id="c40b7-117">ASR Fabric-objekt</span><span class="sxs-lookup"><span data-stu-id="c40b7-117">ASR fabric object</span></span>

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

### <span data-ttu-id="c40b7-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c40b7-118">-FriendlyName</span></span>
<span data-ttu-id="c40b7-119">Eget namn på systemets ASR-objekt.</span><span class="sxs-lookup"><span data-stu-id="c40b7-119">Friendly name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c40b7-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="c40b7-120">-Name</span></span>
<span data-ttu-id="c40b7-121">Namn på nätverkets ASR-objekt.</span><span class="sxs-lookup"><span data-stu-id="c40b7-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="c40b7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c40b7-122">CommonParameters</span></span>
<span data-ttu-id="c40b7-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c40b7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c40b7-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c40b7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c40b7-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c40b7-125">INPUTS</span></span>

### <span data-ttu-id="c40b7-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c40b7-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c40b7-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c40b7-127">OUTPUTS</span></span>

### <span data-ttu-id="c40b7-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="c40b7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="c40b7-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c40b7-129">NOTES</span></span>

## <span data-ttu-id="c40b7-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c40b7-130">RELATED LINKS</span></span>