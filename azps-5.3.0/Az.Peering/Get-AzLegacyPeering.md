---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: e7b5ef8ef41c66cc3c19fd5ebdcfd53ddcc6f3a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522380"
---
# <span data-ttu-id="e1c2e-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="e1c2e-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="e1c2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c2e-103">Används för att konvertera gamla peering-resurser till resurser för Azure Resource Management (ARM).</span><span class="sxs-lookup"><span data-stu-id="e1c2e-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="e1c2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1c2e-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1c2e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1c2e-105">DESCRIPTION</span></span>
<span data-ttu-id="e1c2e-106">Kommandot används för att Visa äldre peering-resurser som alla du använder för att konvertera dem till resurser för Azure Resource Management (ARM).</span><span class="sxs-lookup"><span data-stu-id="e1c2e-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="e1c2e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1c2e-107">EXAMPLES</span></span>

### <span data-ttu-id="e1c2e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e1c2e-108">Example 1</span></span>
```powershell
PS C:> Get-AzLegacyPeering -PeeringLocation "Seattle" -Kind Direct

Name                       :
Sku                        : Basic_Direct_Free
Kind                       : Direct
PeeringLocation            : Seattle
UseForPeeringService       : False
PeerAsn.Id                 :
Connection                 : ------------------------
PeeringDBFacilityId        : 71
SessionPrefixIPv4          : 173.205.50.236/30
PeerSessionIPv4Address     : 173.205.50.237
MicrosoftIPv4Address       : 173.205.50.238
SessionStateV4             : Established
MaxPrefixesAdvertisedV4    : 20000
SessionPrefixIPv6          : 2001:668:0:3:ffff:0:adcd:32ec/126
PeerSessionIPv6Address     : 2001:668:0:3:ffff:0:adcd:32ed
MicrosoftIPv6Address       : 2001:668:0:3:ffff:0:adcd:32ee
SessionStateV6             : Established
MaxPrefixesAdvertisedV6    : 2000
ConnectionState            : Active
BandwidthInMbps            : 0
ProvisionedBandwidthInMbps : 20000
ProvisioningState          : Succeeded
```

<span data-ttu-id="e1c2e-109">Får äldre peering för Seattle</span><span class="sxs-lookup"><span data-stu-id="e1c2e-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="e1c2e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1c2e-110">PARAMETERS</span></span>

### <span data-ttu-id="e1c2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c2e-111">-DefaultProfile</span></span>
<span data-ttu-id="e1c2e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1c2e-113">-Sort</span><span class="sxs-lookup"><span data-stu-id="e1c2e-113">-Kind</span></span>
<span data-ttu-id="e1c2e-114">Visar alla peering-resurser av typen.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-114">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c2e-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="e1c2e-115">-PeeringLocation</span></span>
<span data-ttu-id="e1c2e-116">Visar alla peering-resurser av typen.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-116">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c2e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c2e-117">CommonParameters</span></span>
<span data-ttu-id="e1c2e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c2e-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1c2e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c2e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1c2e-120">INPUTS</span></span>

### <span data-ttu-id="e1c2e-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="e1c2e-121">None</span></span>

## <span data-ttu-id="e1c2e-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1c2e-122">OUTPUTS</span></span>

### <span data-ttu-id="e1c2e-123">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="e1c2e-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="e1c2e-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1c2e-124">NOTES</span></span>

## <span data-ttu-id="e1c2e-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1c2e-125">RELATED LINKS</span></span>
