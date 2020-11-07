---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f5fbef7c67676f16793b63a8448517ca24aa7e5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921824"
---
# <span data-ttu-id="05420-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="05420-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="05420-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05420-102">SYNOPSIS</span></span>
<span data-ttu-id="05420-103">Få en översikt över statusen för nätverks resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="05420-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="05420-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05420-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="05420-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05420-105">DESCRIPTION</span></span>
<span data-ttu-id="05420-106">Få en översikt över statusen för nätverks resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="05420-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="05420-107">Enskilda egenskaper ger detaljerad information om resursanvändning och hälsa efter komponent.</span><span class="sxs-lookup"><span data-stu-id="05420-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="05420-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05420-108">EXAMPLES</span></span>

### <span data-ttu-id="05420-109">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="05420-109">EXAMPLE 1</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="05420-110">Få översikt över nätverks administratör.</span><span class="sxs-lookup"><span data-stu-id="05420-110">Get network admin overview.</span></span>

### <span data-ttu-id="05420-111">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="05420-111">EXAMPLE 2</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="05420-112">Få offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="05420-112">Get public ip address usage.</span></span>

## <span data-ttu-id="05420-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05420-113">PARAMETERS</span></span>

### <span data-ttu-id="05420-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05420-114">CommonParameters</span></span>
<span data-ttu-id="05420-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05420-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05420-116">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05420-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05420-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05420-117">INPUTS</span></span>

## <span data-ttu-id="05420-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05420-118">OUTPUTS</span></span>

### <span data-ttu-id="05420-119">Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview</span><span class="sxs-lookup"><span data-stu-id="05420-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="05420-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05420-120">NOTES</span></span>

## <span data-ttu-id="05420-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05420-121">RELATED LINKS</span></span>
