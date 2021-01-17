---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 8341f465bab88f8d8a60e5f171f883dbb9a2467e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424976"
---
# <span data-ttu-id="dc933-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="dc933-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="dc933-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc933-102">SYNOPSIS</span></span>
<span data-ttu-id="dc933-103">Hämtar en lista över peering service-leverantörer som samarbetar med Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dc933-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="dc933-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc933-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc933-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc933-105">DESCRIPTION</span></span>
<span data-ttu-id="dc933-106">Lista peering service-leverantörer</span><span class="sxs-lookup"><span data-stu-id="dc933-106">List peering service providers</span></span>

## <span data-ttu-id="dc933-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc933-107">EXAMPLES</span></span>

### <span data-ttu-id="dc933-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dc933-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="dc933-109">Hämtar tillgängliga peering service-leverantörer</span><span class="sxs-lookup"><span data-stu-id="dc933-109">Gets available peering service providers</span></span>

## <span data-ttu-id="dc933-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc933-110">PARAMETERS</span></span>

### <span data-ttu-id="dc933-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc933-111">-DefaultProfile</span></span>
<span data-ttu-id="dc933-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc933-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc933-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc933-113">CommonParameters</span></span>
<span data-ttu-id="dc933-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc933-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc933-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc933-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc933-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc933-116">INPUTS</span></span>

### <span data-ttu-id="dc933-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="dc933-117">None</span></span>

## <span data-ttu-id="dc933-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc933-118">OUTPUTS</span></span>

### <span data-ttu-id="dc933-119">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="dc933-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="dc933-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc933-120">NOTES</span></span>

## <span data-ttu-id="dc933-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc933-121">RELATED LINKS</span></span>
