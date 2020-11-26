---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 370965325a265ef4c2b7fa5e0070ae705099e2c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269209"
---
# <span data-ttu-id="7d015-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="7d015-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="7d015-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d015-102">SYNOPSIS</span></span>
<span data-ttu-id="7d015-103">Skapar en ny undantags regel lista för Application Gateway WAF</span><span class="sxs-lookup"><span data-stu-id="7d015-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="7d015-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d015-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d015-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d015-105">DESCRIPTION</span></span>
<span data-ttu-id="7d015-106">**New-AzApplicationGatewayFirewallExclusionConfig-** cmdlet en ny lista över undantags regler för Application Gateway-WAF.</span><span class="sxs-lookup"><span data-stu-id="7d015-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="7d015-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d015-107">EXAMPLES</span></span>

### <span data-ttu-id="7d015-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7d015-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="7d015-109">Det här kommandot skapar en ny lista med undantags regel listor för variabeln med namnet RequestHeaderNames och operatorn StartsWith och Selector.</span><span class="sxs-lookup"><span data-stu-id="7d015-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="7d015-110">Konfigurationen för exkluderings lista sparas i $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="7d015-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="7d015-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d015-111">PARAMETERS</span></span>

### <span data-ttu-id="7d015-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d015-112">-DefaultProfile</span></span>
<span data-ttu-id="7d015-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d015-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d015-114">-Operatör</span><span class="sxs-lookup"><span data-stu-id="7d015-114">-Operator</span></span>
<span data-ttu-id="7d015-115">Om variabeln är en samling kan du använda den på väljaren för att ange vilka element i samlingen detta undantag gäller.</span><span class="sxs-lookup"><span data-stu-id="7d015-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="7d015-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="7d015-116">-Selector</span></span>
<span data-ttu-id="7d015-117">När variabeln är en samling används operatorn för att ange vilka element i samlingen detta undantag gäller.</span><span class="sxs-lookup"><span data-stu-id="7d015-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="7d015-118">-Variabel</span><span class="sxs-lookup"><span data-stu-id="7d015-118">-Variable</span></span>
<span data-ttu-id="7d015-119">Den variabel som ska uteslutas.</span><span class="sxs-lookup"><span data-stu-id="7d015-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="7d015-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d015-120">CommonParameters</span></span>
<span data-ttu-id="7d015-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d015-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d015-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d015-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d015-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d015-123">INPUTS</span></span>

### <span data-ttu-id="7d015-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="7d015-124">None</span></span>

## <span data-ttu-id="7d015-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d015-125">OUTPUTS</span></span>

### <span data-ttu-id="7d015-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="7d015-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="7d015-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d015-127">NOTES</span></span>

## <span data-ttu-id="7d015-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d015-128">RELATED LINKS</span></span>