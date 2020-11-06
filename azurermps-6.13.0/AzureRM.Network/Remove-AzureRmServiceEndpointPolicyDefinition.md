---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3d406bf0dffb0ee250e1494fc05727d0a4c983ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584087"
---
# <span data-ttu-id="4cd9d-101">Remove-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4cd9d-101">Remove-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="4cd9d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cd9d-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd9d-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="4cd9d-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cd9d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cd9d-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cd9d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cd9d-105">DESCRIPTION</span></span>
<span data-ttu-id="4cd9d-106">Cmdleten **Remove-AzureRmServiceEndpointPolicy** tar bort en princip för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="4cd9d-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="4cd9d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cd9d-107">EXAMPLES</span></span>

### <span data-ttu-id="4cd9d-108">Exempel 1: tar bort en princip för service slut punkter med namn</span><span class="sxs-lookup"><span data-stu-id="4cd9d-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="4cd9d-109">Det här kommandot tar bort en princip för service slut punkter med namnet PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="4cd9d-109">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="4cd9d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cd9d-110">PARAMETERS</span></span>

### <span data-ttu-id="4cd9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd9d-111">-DefaultProfile</span></span>
<span data-ttu-id="4cd9d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4cd9d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cd9d-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4cd9d-113">-Name</span></span>
<span data-ttu-id="4cd9d-114">Namnet på tjänst slut punkts definitionen</span><span class="sxs-lookup"><span data-stu-id="4cd9d-114">The name of the service endpoint definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd9d-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4cd9d-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="4cd9d-116">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4cd9d-116">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="4cd9d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd9d-117">CommonParameters</span></span>
<span data-ttu-id="4cd9d-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cd9d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4cd9d-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cd9d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd9d-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cd9d-120">INPUTS</span></span>

### <span data-ttu-id="4cd9d-121">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4cd9d-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="4cd9d-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cd9d-122">OUTPUTS</span></span>

### <span data-ttu-id="4cd9d-123">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4cd9d-123">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="4cd9d-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cd9d-124">NOTES</span></span>

## <span data-ttu-id="4cd9d-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cd9d-125">RELATED LINKS</span></span>
