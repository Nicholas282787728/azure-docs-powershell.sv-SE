---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: e344dd4b5284a29c84b4f4c4b90d5a99f5d8d4ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747467"
---
# <span data-ttu-id="0ab61-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="0ab61-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="0ab61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ab61-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab61-103">Hämtar information om nätverken som hanteras av webbplats återställning för det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="0ab61-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="0ab61-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ab61-104">SYNTAX</span></span>

### <span data-ttu-id="0ab61-105">ByFabricObject (standard)</span><span class="sxs-lookup"><span data-stu-id="0ab61-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ab61-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0ab61-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ab61-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0ab61-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ab61-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ab61-108">DESCRIPTION</span></span>
<span data-ttu-id="0ab61-109">Cmdleten **Get-AzRecoveryServicesAsrNetwork** hämtar information om Azure Site Recovery-nätverk för det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="0ab61-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="0ab61-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ab61-110">EXAMPLES</span></span>

### <span data-ttu-id="0ab61-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0ab61-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="0ab61-112">Hämtar alla kända nätverk i angiven infrastruktur resurs.</span><span class="sxs-lookup"><span data-stu-id="0ab61-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="0ab61-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ab61-113">PARAMETERS</span></span>

### <span data-ttu-id="0ab61-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab61-114">-DefaultProfile</span></span>
<span data-ttu-id="0ab61-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab61-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0ab61-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="0ab61-116">-Fabric</span></span>
<span data-ttu-id="0ab61-117">ASR Fabric-objekt</span><span class="sxs-lookup"><span data-stu-id="0ab61-117">ASR fabric object</span></span>

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

### <span data-ttu-id="0ab61-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0ab61-118">-FriendlyName</span></span>
<span data-ttu-id="0ab61-119">Eget namn på systemets ASR-objekt.</span><span class="sxs-lookup"><span data-stu-id="0ab61-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="0ab61-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ab61-120">-Name</span></span>
<span data-ttu-id="0ab61-121">Namn på nätverkets ASR-objekt.</span><span class="sxs-lookup"><span data-stu-id="0ab61-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="0ab61-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab61-122">CommonParameters</span></span>
<span data-ttu-id="0ab61-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab61-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab61-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab61-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab61-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ab61-125">INPUTS</span></span>

### <span data-ttu-id="0ab61-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="0ab61-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="0ab61-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ab61-127">OUTPUTS</span></span>

### <span data-ttu-id="0ab61-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="0ab61-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="0ab61-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ab61-129">NOTES</span></span>

## <span data-ttu-id="0ab61-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ab61-130">RELATED LINKS</span></span>
