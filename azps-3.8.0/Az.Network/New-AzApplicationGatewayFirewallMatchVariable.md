---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092550"
---
# <span data-ttu-id="dccdc-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="dccdc-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="dccdc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dccdc-102">SYNOPSIS</span></span>
<span data-ttu-id="dccdc-103">Skapar en träff-variabel för brand Väggs villkor.</span><span class="sxs-lookup"><span data-stu-id="dccdc-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="dccdc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dccdc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dccdc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dccdc-105">DESCRIPTION</span></span>
<span data-ttu-id="dccdc-106">**New-AzApplicationGatewayFirewallMatchVariable** skapar en match-variabel för brand Väggs villkor.</span><span class="sxs-lookup"><span data-stu-id="dccdc-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="dccdc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dccdc-107">EXAMPLES</span></span>

### <span data-ttu-id="dccdc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dccdc-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="dccdc-109">Kommandot skapar en ny matcha-variabel med namnet på begärandehuvuden och väljaren för innehålls längd.</span><span class="sxs-lookup"><span data-stu-id="dccdc-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="dccdc-110">Den nya matcha-variabeln sparas i $variable.</span><span class="sxs-lookup"><span data-stu-id="dccdc-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="dccdc-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dccdc-111">PARAMETERS</span></span>

### <span data-ttu-id="dccdc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dccdc-112">-DefaultProfile</span></span>
<span data-ttu-id="dccdc-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dccdc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dccdc-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="dccdc-114">-Selector</span></span>
<span data-ttu-id="dccdc-115">Beskriver fältet i matchVariable-samlingen.</span><span class="sxs-lookup"><span data-stu-id="dccdc-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="dccdc-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="dccdc-116">-VariableName</span></span>
<span data-ttu-id="dccdc-117">Matcha variabel.</span><span class="sxs-lookup"><span data-stu-id="dccdc-117">Match Variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeaders, RequestBody, RequestCookies

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dccdc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dccdc-118">CommonParameters</span></span>
<span data-ttu-id="dccdc-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dccdc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dccdc-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dccdc-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dccdc-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dccdc-121">INPUTS</span></span>

### <span data-ttu-id="dccdc-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="dccdc-122">None</span></span>

## <span data-ttu-id="dccdc-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dccdc-123">OUTPUTS</span></span>

### <span data-ttu-id="dccdc-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="dccdc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="dccdc-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dccdc-125">NOTES</span></span>

## <span data-ttu-id="dccdc-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dccdc-126">RELATED LINKS</span></span>