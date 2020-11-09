---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322183"
---
# <span data-ttu-id="9144f-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9144f-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="9144f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9144f-102">SYNOPSIS</span></span>
<span data-ttu-id="9144f-103">Hämtar information om nätverks mappningar för webbplats återställning för det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="9144f-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="9144f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9144f-104">SYNTAX</span></span>

### <span data-ttu-id="9144f-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="9144f-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9144f-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="9144f-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9144f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9144f-107">DESCRIPTION</span></span>
<span data-ttu-id="9144f-108">Cmdleten **Get-AzRecoveryServicesAsrNetworkMapping** hämtar information om nätverks mappningar för Azure Site Recovery för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="9144f-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="9144f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9144f-109">EXAMPLES</span></span>

### <span data-ttu-id="9144f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9144f-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="9144f-111">Hämtar alla nätverks mappningar för det skickade nätverket.</span><span class="sxs-lookup"><span data-stu-id="9144f-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="9144f-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9144f-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="9144f-113">Hämtar nätverks mappning med angivet namn i angivet Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="9144f-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="9144f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9144f-114">PARAMETERS</span></span>

### <span data-ttu-id="9144f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9144f-115">-DefaultProfile</span></span>
<span data-ttu-id="9144f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9144f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9144f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="9144f-117">-Name</span></span>
<span data-ttu-id="9144f-118">Namnet på det objekt för automatisk nätverks mappning som ska visas.</span><span class="sxs-lookup"><span data-stu-id="9144f-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9144f-119">-Network</span><span class="sxs-lookup"><span data-stu-id="9144f-119">-Network</span></span>
<span data-ttu-id="9144f-120">Skaffa de nätverks mappningar för automatisk återställning som motsvarar det angivna objektet för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="9144f-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9144f-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="9144f-121">-PrimaryFabric</span></span>
<span data-ttu-id="9144f-122">Hämta de nätverks mappningar för automatisk återställning som motsvarar det angivna primära infrastruktur resursen.</span><span class="sxs-lookup"><span data-stu-id="9144f-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9144f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9144f-123">CommonParameters</span></span>
<span data-ttu-id="9144f-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9144f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9144f-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9144f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9144f-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9144f-126">INPUTS</span></span>

### <span data-ttu-id="9144f-127">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="9144f-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="9144f-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="9144f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="9144f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9144f-129">OUTPUTS</span></span>

### <span data-ttu-id="9144f-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9144f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="9144f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9144f-131">NOTES</span></span>

## <span data-ttu-id="9144f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9144f-132">RELATED LINKS</span></span>

[<span data-ttu-id="9144f-133">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9144f-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="9144f-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9144f-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
