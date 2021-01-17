---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397952"
---
# <span data-ttu-id="d24eb-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="d24eb-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="d24eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d24eb-102">SYNOPSIS</span></span>
<span data-ttu-id="d24eb-103">Skapar ett undantag för brand Väggs principen</span><span class="sxs-lookup"><span data-stu-id="d24eb-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="d24eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d24eb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d24eb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d24eb-105">DESCRIPTION</span></span>
<span data-ttu-id="d24eb-106">**New-AzApplicationGatewayFirewallPolicyExclusion-** cmdlet en ny lista över undantags regler för brand Väggs princip.</span><span class="sxs-lookup"><span data-stu-id="d24eb-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="d24eb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d24eb-107">EXAMPLES</span></span>

### <span data-ttu-id="d24eb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d24eb-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="d24eb-109">Det här kommandot skapar en ny uteslutning-post för variabeln med namnet RequestHeaderNames och operatorn StartsWith och Selector som heter xyz.</span><span class="sxs-lookup"><span data-stu-id="d24eb-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="d24eb-110">Undantags posten sparas i $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="d24eb-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="d24eb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d24eb-111">PARAMETERS</span></span>

### <span data-ttu-id="d24eb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24eb-112">-DefaultProfile</span></span>
<span data-ttu-id="d24eb-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d24eb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d24eb-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="d24eb-114">-MatchVariable</span></span>
<span data-ttu-id="d24eb-115">Den variabel som ska uteslutas.</span><span class="sxs-lookup"><span data-stu-id="d24eb-115">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestHeaderNames, RequestCookieNames, RequestArgNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24eb-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="d24eb-116">-Selector</span></span>
<span data-ttu-id="d24eb-117">När variabeln är en samling används operatorn för att ange vilka element i samlingen detta undantag gäller.</span><span class="sxs-lookup"><span data-stu-id="d24eb-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="d24eb-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="d24eb-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="d24eb-119">Om variabeln är en samling kan du använda den på väljaren för att ange vilka element i samlingen detta undantag gäller.</span><span class="sxs-lookup"><span data-stu-id="d24eb-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Equals, Contains, StartsWith, EndsWith, EqualsAny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24eb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24eb-120">CommonParameters</span></span>
<span data-ttu-id="d24eb-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d24eb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24eb-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d24eb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24eb-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d24eb-123">INPUTS</span></span>

### <span data-ttu-id="d24eb-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="d24eb-124">None</span></span>

## <span data-ttu-id="d24eb-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d24eb-125">OUTPUTS</span></span>

### <span data-ttu-id="d24eb-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="d24eb-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="d24eb-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d24eb-127">NOTES</span></span>

## <span data-ttu-id="d24eb-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d24eb-128">RELATED LINKS</span></span>
