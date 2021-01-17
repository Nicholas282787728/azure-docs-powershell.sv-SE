---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 370965325a265ef4c2b7fa5e0070ae705099e2c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397979"
---
# <span data-ttu-id="f0d01-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="f0d01-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="f0d01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0d01-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d01-103">Skapar en ny undantags regel lista för Application Gateway WAF</span><span class="sxs-lookup"><span data-stu-id="f0d01-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="f0d01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0d01-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0d01-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0d01-105">DESCRIPTION</span></span>
<span data-ttu-id="f0d01-106">**New-AzApplicationGatewayFirewallExclusionConfig-** cmdlet en ny lista över undantags regler för Application Gateway-WAF.</span><span class="sxs-lookup"><span data-stu-id="f0d01-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="f0d01-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0d01-107">EXAMPLES</span></span>

### <span data-ttu-id="f0d01-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f0d01-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="f0d01-109">Det här kommandot skapar en ny lista med undantags regel listor för variabeln med namnet RequestHeaderNames och operatorn StartsWith och Selector.</span><span class="sxs-lookup"><span data-stu-id="f0d01-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="f0d01-110">Konfigurationen för exkluderings lista sparas i $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="f0d01-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="f0d01-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0d01-111">PARAMETERS</span></span>

### <span data-ttu-id="f0d01-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d01-112">-DefaultProfile</span></span>
<span data-ttu-id="f0d01-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d01-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0d01-114">-Operatör</span><span class="sxs-lookup"><span data-stu-id="f0d01-114">-Operator</span></span>
<span data-ttu-id="f0d01-115">Om variabeln är en samling kan du använda den på väljaren för att ange vilka element i samlingen detta undantag gäller.</span><span class="sxs-lookup"><span data-stu-id="f0d01-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d01-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="f0d01-116">-Selector</span></span>
<span data-ttu-id="f0d01-117">När variabeln är en samling används operatorn för att ange vilka element i samlingen detta undantag gäller.</span><span class="sxs-lookup"><span data-stu-id="f0d01-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d01-118">-Variabel</span><span class="sxs-lookup"><span data-stu-id="f0d01-118">-Variable</span></span>
<span data-ttu-id="f0d01-119">Den variabel som ska uteslutas.</span><span class="sxs-lookup"><span data-stu-id="f0d01-119">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d01-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d01-120">CommonParameters</span></span>
<span data-ttu-id="f0d01-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d01-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d01-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d01-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d01-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0d01-123">INPUTS</span></span>

### <span data-ttu-id="f0d01-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="f0d01-124">None</span></span>

## <span data-ttu-id="f0d01-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0d01-125">OUTPUTS</span></span>

### <span data-ttu-id="f0d01-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="f0d01-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="f0d01-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0d01-127">NOTES</span></span>

## <span data-ttu-id="f0d01-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0d01-128">RELATED LINKS</span></span>
