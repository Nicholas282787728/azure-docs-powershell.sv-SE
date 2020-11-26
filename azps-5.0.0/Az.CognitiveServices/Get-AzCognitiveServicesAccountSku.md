---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: 3c632e6ffbf26e3aaacb725e9b663ffafbc49ec2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270863"
---
# <span data-ttu-id="8f0c6-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="8f0c6-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="8f0c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="8f0c6-103">Hämtar tillgängliga SKU: er för ett konto.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="8f0c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f0c6-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f0c6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f0c6-105">DESCRIPTION</span></span>
<span data-ttu-id="8f0c6-106">Cmdleten **Get-AzCognitiveServicesAccountSku** hämtar tillgängliga SKU: er för ett kognitivt Services-konto.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="8f0c6-107">SKU är en nivå plan för ett konto.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="8f0c6-108">Det definierar priset, samtals gränsen och kostnaden för kontot.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="8f0c6-109">F0 SKU är en kostnads fri nivå.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="8f0c6-110">Betalda nivåer är S0, S1, S2 och så vidare.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="8f0c6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f0c6-111">EXAMPLES</span></span>

### <span data-ttu-id="8f0c6-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8f0c6-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="8f0c6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f0c6-113">PARAMETERS</span></span>

### <span data-ttu-id="8f0c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f0c6-114">-DefaultProfile</span></span>
<span data-ttu-id="8f0c6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8f0c6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f0c6-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="8f0c6-116">-Location</span></span>
<span data-ttu-id="8f0c6-117">Konto plats för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="8f0c6-118">– Skriv</span><span class="sxs-lookup"><span data-stu-id="8f0c6-118">-Type</span></span>
<span data-ttu-id="8f0c6-119">Konto typen för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-119">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f0c6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f0c6-120">CommonParameters</span></span>
<span data-ttu-id="8f0c6-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f0c6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f0c6-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f0c6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f0c6-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f0c6-123">INPUTS</span></span>

### <span data-ttu-id="8f0c6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8f0c6-124">System.String</span></span>

## <span data-ttu-id="8f0c6-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f0c6-125">OUTPUTS</span></span>

### <span data-ttu-id="8f0c6-126">Microsoft. Azure. Management. CognitiveServices. Models. ResourceSku</span><span class="sxs-lookup"><span data-stu-id="8f0c6-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="8f0c6-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f0c6-127">NOTES</span></span>

## <span data-ttu-id="8f0c6-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f0c6-128">RELATED LINKS</span></span>