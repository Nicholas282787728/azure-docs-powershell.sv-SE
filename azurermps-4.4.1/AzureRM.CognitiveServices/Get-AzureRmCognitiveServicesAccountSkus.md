---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: de2640d8a2044a8124fb87bed53b9ee433977716
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578404"
---
# <span data-ttu-id="9a1fe-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="9a1fe-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="9a1fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="9a1fe-103">Hämtar tillgängliga SKU: er för ett konto.</span><span class="sxs-lookup"><span data-stu-id="9a1fe-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a1fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a1fe-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a1fe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a1fe-105">DESCRIPTION</span></span>
<span data-ttu-id="9a1fe-106">Cmdleten **Get-AzureRmCognitiveServicesAccountSkus** hämtar tillgängliga SKU: er för ett kognitivt Services-konto.</span><span class="sxs-lookup"><span data-stu-id="9a1fe-106">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>

<span data-ttu-id="9a1fe-107">SKU är en nivå plan för ett konto.</span><span class="sxs-lookup"><span data-stu-id="9a1fe-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="9a1fe-108">Det definierar priset, samtals gränsen och kostnaden för kontot.</span><span class="sxs-lookup"><span data-stu-id="9a1fe-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="9a1fe-109">F0 SKU är en kostnads fri nivå.</span><span class="sxs-lookup"><span data-stu-id="9a1fe-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="9a1fe-110">Betalda nivåer är S0, S1, S2 och så vidare.</span><span class="sxs-lookup"><span data-stu-id="9a1fe-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="9a1fe-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a1fe-111">EXAMPLES</span></span>

## <span data-ttu-id="9a1fe-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a1fe-112">PARAMETERS</span></span>

### <span data-ttu-id="9a1fe-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9a1fe-113">-Name</span></span>
<span data-ttu-id="9a1fe-114">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="9a1fe-114">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1fe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a1fe-115">-ResourceGroupName</span></span>
<span data-ttu-id="9a1fe-116">Anger namnet på resurs gruppen som kontot är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="9a1fe-116">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a1fe-117">-DefaultProfile</span></span>
<span data-ttu-id="9a1fe-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a1fe-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a1fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a1fe-119">CommonParameters</span></span>
<span data-ttu-id="9a1fe-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a1fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a1fe-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a1fe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a1fe-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a1fe-122">INPUTS</span></span>

## <span data-ttu-id="9a1fe-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a1fe-123">OUTPUTS</span></span>

### <span data-ttu-id="9a1fe-124">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="9a1fe-124">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="9a1fe-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a1fe-125">NOTES</span></span>

## <span data-ttu-id="9a1fe-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a1fe-126">RELATED LINKS</span></span>

