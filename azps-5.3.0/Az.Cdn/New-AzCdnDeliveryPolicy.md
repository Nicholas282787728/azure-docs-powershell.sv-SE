---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: a00e8d11868ae487357f1105d2bc2ae3934a9db9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527127"
---
# <span data-ttu-id="bc040-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="bc040-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="bc040-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bc040-102">SYNOPSIS</span></span>
<span data-ttu-id="bc040-103">Skapar en leverans princip.</span><span class="sxs-lookup"><span data-stu-id="bc040-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="bc040-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bc040-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc040-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bc040-105">DESCRIPTION</span></span>
<span data-ttu-id="bc040-106">Cmdleten **New-AzCdnDeliveryPolicy** skapar en leverans princip för generering av CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="bc040-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="bc040-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bc040-107">EXAMPLES</span></span>

### <span data-ttu-id="bc040-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bc040-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="bc040-109">Skapa en exempel leverans Policy</span><span class="sxs-lookup"><span data-stu-id="bc040-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="bc040-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bc040-110">PARAMETERS</span></span>

### <span data-ttu-id="bc040-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc040-111">-DefaultProfile</span></span>
<span data-ttu-id="bc040-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bc040-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc040-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="bc040-113">-Description</span></span>
<span data-ttu-id="bc040-114">Beskrivning av policyn</span><span class="sxs-lookup"><span data-stu-id="bc040-114">Description of the policy</span></span>

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

### <span data-ttu-id="bc040-115">-Regel</span><span class="sxs-lookup"><span data-stu-id="bc040-115">-Rule</span></span>
<span data-ttu-id="bc040-116">En lista med deliveryRules.</span><span class="sxs-lookup"><span data-stu-id="bc040-116">A list of deliveryRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc040-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc040-117">CommonParameters</span></span>
<span data-ttu-id="bc040-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc040-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc040-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc040-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc040-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bc040-120">INPUTS</span></span>

### <span data-ttu-id="bc040-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="bc040-121">None</span></span>

## <span data-ttu-id="bc040-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bc040-122">OUTPUTS</span></span>

### <span data-ttu-id="bc040-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="bc040-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="bc040-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bc040-124">NOTES</span></span>

## <span data-ttu-id="bc040-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bc040-125">RELATED LINKS</span></span>
