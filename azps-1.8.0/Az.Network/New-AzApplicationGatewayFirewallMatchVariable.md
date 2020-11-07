---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: 05a1929f79799be8006ae82c4948dc0a81839040
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748140"
---
# <span data-ttu-id="b44cb-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="b44cb-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="b44cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b44cb-102">SYNOPSIS</span></span>
<span data-ttu-id="b44cb-103">Skapar en träff-variabel för brand Väggs villkor.</span><span class="sxs-lookup"><span data-stu-id="b44cb-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="b44cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b44cb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b44cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b44cb-105">DESCRIPTION</span></span>
<span data-ttu-id="b44cb-106">**New-AzApplicationGatewayFirewallMatchVariable** skapar en match-variabel för brand Väggs villkor.</span><span class="sxs-lookup"><span data-stu-id="b44cb-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="b44cb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b44cb-107">EXAMPLES</span></span>

### <span data-ttu-id="b44cb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b44cb-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzureRmApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="b44cb-109">Kommandot skapar en ny matcha-variabel med namnet på begärandehuvuden och väljaren för innehålls längd.</span><span class="sxs-lookup"><span data-stu-id="b44cb-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="b44cb-110">Den nya matcha-variabeln sparas i $variable.</span><span class="sxs-lookup"><span data-stu-id="b44cb-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="b44cb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b44cb-111">PARAMETERS</span></span>

### <span data-ttu-id="b44cb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b44cb-112">-DefaultProfile</span></span>
<span data-ttu-id="b44cb-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b44cb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b44cb-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="b44cb-114">-Selector</span></span>
<span data-ttu-id="b44cb-115">Beskriver fältet i matchVariable-samlingen.</span><span class="sxs-lookup"><span data-stu-id="b44cb-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="b44cb-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="b44cb-116">-VariableName</span></span>
<span data-ttu-id="b44cb-117">Matcha variabel.</span><span class="sxs-lookup"><span data-stu-id="b44cb-117">Match Variable.</span></span>

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

### <span data-ttu-id="b44cb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b44cb-118">CommonParameters</span></span>
<span data-ttu-id="b44cb-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b44cb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b44cb-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b44cb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b44cb-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b44cb-121">INPUTS</span></span>

### <span data-ttu-id="b44cb-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="b44cb-122">None</span></span>

## <span data-ttu-id="b44cb-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b44cb-123">OUTPUTS</span></span>

### <span data-ttu-id="b44cb-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="b44cb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="b44cb-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b44cb-125">NOTES</span></span>

## <span data-ttu-id="b44cb-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b44cb-126">RELATED LINKS</span></span>
