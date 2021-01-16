---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: fcd59eb37a518cc4f6cd0b5d1c580706d2f6e8bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523452"
---
# <span data-ttu-id="eca71-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="eca71-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="eca71-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eca71-102">SYNOPSIS</span></span>
<span data-ttu-id="eca71-103">Hämta lista över privata butiker</span><span class="sxs-lookup"><span data-stu-id="eca71-103">Get private store list</span></span>

## <span data-ttu-id="eca71-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eca71-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eca71-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eca71-105">DESCRIPTION</span></span>
<span data-ttu-id="eca71-106">Hämta en privat butiks lista som skapades under innehavarens omfattning</span><span class="sxs-lookup"><span data-stu-id="eca71-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="eca71-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eca71-107">EXAMPLES</span></span>

### <span data-ttu-id="eca71-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eca71-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="eca71-109">lista för privat lagring som har skapats under klient organisationens omfattning</span><span class="sxs-lookup"><span data-stu-id="eca71-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="eca71-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eca71-110">PARAMETERS</span></span>

### <span data-ttu-id="eca71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca71-111">-DefaultProfile</span></span>
<span data-ttu-id="eca71-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eca71-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eca71-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca71-113">CommonParameters</span></span>
<span data-ttu-id="eca71-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eca71-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca71-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eca71-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca71-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eca71-116">INPUTS</span></span>

### <span data-ttu-id="eca71-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="eca71-117">None</span></span>

## <span data-ttu-id="eca71-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eca71-118">OUTPUTS</span></span>

### <span data-ttu-id="eca71-119">Microsoft. Azure. commands. Marketplace. Models. PrivateStore. PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="eca71-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="eca71-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eca71-120">NOTES</span></span>

## <span data-ttu-id="eca71-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eca71-121">RELATED LINKS</span></span>
