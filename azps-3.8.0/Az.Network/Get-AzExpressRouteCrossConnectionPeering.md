---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091097"
---
# <span data-ttu-id="95d77-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="95d77-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="95d77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95d77-102">SYNOPSIS</span></span>
<span data-ttu-id="95d77-103">Hämtar en ExpressRoute-konfiguration för flera kors anslutningar.</span><span class="sxs-lookup"><span data-stu-id="95d77-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="95d77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95d77-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95d77-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95d77-105">DESCRIPTION</span></span>
<span data-ttu-id="95d77-106">Cmdleten **Get-AzExpressRouteCrossConnectionPeering** hämtar konfigurationen för en peering-relation för en ExpressRoute-kors anslutning.</span><span class="sxs-lookup"><span data-stu-id="95d77-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="95d77-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95d77-107">EXAMPLES</span></span>

### <span data-ttu-id="95d77-108">Exempel 1: Visa peering-konfigurationen för en ExpressRoute-kors anslutning</span><span class="sxs-lookup"><span data-stu-id="95d77-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="95d77-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95d77-109">PARAMETERS</span></span>

### <span data-ttu-id="95d77-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d77-110">-DefaultProfile</span></span>
<span data-ttu-id="95d77-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95d77-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95d77-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="95d77-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="95d77-113">ExpressRoute Cross Connection-objekt som innehåller peering-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="95d77-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95d77-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="95d77-114">-Name</span></span>
<span data-ttu-id="95d77-115">Namnet på den peering-konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="95d77-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d77-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d77-116">CommonParameters</span></span>
<span data-ttu-id="95d77-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d77-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d77-118">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95d77-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d77-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95d77-119">INPUTS</span></span>

### <span data-ttu-id="95d77-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="95d77-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="95d77-121">Parametern ' ExpressRouteCrossConnection ' godkänner värdet av typen ' PSExpressRouteCrossConnection ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="95d77-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="95d77-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95d77-122">OUTPUTS</span></span>

### <span data-ttu-id="95d77-123">Microsoft. Azure. commands. Networks. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="95d77-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="95d77-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95d77-124">NOTES</span></span>

## <span data-ttu-id="95d77-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95d77-125">RELATED LINKS</span></span>

[<span data-ttu-id="95d77-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="95d77-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="95d77-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="95d77-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="95d77-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="95d77-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="95d77-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="95d77-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
