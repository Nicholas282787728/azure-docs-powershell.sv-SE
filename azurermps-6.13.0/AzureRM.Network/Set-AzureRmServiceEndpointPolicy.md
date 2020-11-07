---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: ecd5a8eafc70a88b4ebda17a83f2b40139f5463f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756145"
---
# <span data-ttu-id="688ef-101">Set-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="688ef-101">Set-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="688ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="688ef-102">SYNOPSIS</span></span>
<span data-ttu-id="688ef-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="688ef-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="688ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="688ef-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="688ef-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="688ef-105">DESCRIPTION</span></span>
<span data-ttu-id="688ef-106">Cmdleten **set-AzureRmServiceEndpointPolicy** skapar en tjänst slut punkts princip.</span><span class="sxs-lookup"><span data-stu-id="688ef-106">The **Set-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="688ef-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="688ef-107">EXAMPLES</span></span>

### <span data-ttu-id="688ef-108">Exempel 1: anger en policy för tjänst slut punkter</span><span class="sxs-lookup"><span data-stu-id="688ef-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="688ef-109">Det här kommandot uppdaterar en tjänst slut punkts princip med namnet Policy1 som definieras av objektet $serviceEndpointPolicy tillhör resourcegroup "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="688ef-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="688ef-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="688ef-110">PARAMETERS</span></span>

### <span data-ttu-id="688ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="688ef-111">-DefaultProfile</span></span>
<span data-ttu-id="688ef-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="688ef-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="688ef-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="688ef-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="688ef-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="688ef-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="688ef-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="688ef-115">CommonParameters</span></span>
<span data-ttu-id="688ef-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="688ef-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="688ef-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="688ef-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="688ef-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="688ef-118">INPUTS</span></span>

### <span data-ttu-id="688ef-119">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="688ef-119">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="688ef-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="688ef-120">OUTPUTS</span></span>

### <span data-ttu-id="688ef-121">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="688ef-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="688ef-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="688ef-122">NOTES</span></span>

## <span data-ttu-id="688ef-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="688ef-123">RELATED LINKS</span></span>
