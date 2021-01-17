---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: edc0309b5e1a0c8b17d400e965074d38ca02bb80
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398683"
---
# <span data-ttu-id="7fca6-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="7fca6-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="7fca6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fca6-102">SYNOPSIS</span></span>
<span data-ttu-id="7fca6-103">Skapar ett hälso avsöknings svar som används av hälso sökning för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7fca6-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="7fca6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fca6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fca6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fca6-105">DESCRIPTION</span></span>
<span data-ttu-id="7fca6-106">Cmdleten **Add-AzApplicationGatewayProbeHealthResponseMatch** skapar ett hälso avsöknings svar som används av hälso sökning för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7fca6-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="7fca6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fca6-107">EXAMPLES</span></span>

### <span data-ttu-id="7fca6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7fca6-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="7fca6-109">Det här kommandot skapar ett sjukvårds svar som kan skickas till ProbeConfig som en parameter.</span><span class="sxs-lookup"><span data-stu-id="7fca6-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="7fca6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fca6-110">PARAMETERS</span></span>

### <span data-ttu-id="7fca6-111">-Body</span><span class="sxs-lookup"><span data-stu-id="7fca6-111">-Body</span></span>
<span data-ttu-id="7fca6-112">Brödtext som måste ingå i sjukvården.</span><span class="sxs-lookup"><span data-stu-id="7fca6-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="7fca6-113">Standardvärdet är inte ifyllt</span><span class="sxs-lookup"><span data-stu-id="7fca6-113">Default value is empty</span></span>

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

### <span data-ttu-id="7fca6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fca6-114">-DefaultProfile</span></span>
<span data-ttu-id="7fca6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7fca6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fca6-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7fca6-116">-StatusCode</span></span>
<span data-ttu-id="7fca6-117">Tillåtna intervall med felfria status koder. Standard intervallet för felfria status koder är 200-399</span><span class="sxs-lookup"><span data-stu-id="7fca6-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fca6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fca6-118">CommonParameters</span></span>
<span data-ttu-id="7fca6-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fca6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fca6-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fca6-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fca6-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fca6-121">INPUTS</span></span>

### <span data-ttu-id="7fca6-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="7fca6-122">None</span></span>

## <span data-ttu-id="7fca6-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fca6-123">OUTPUTS</span></span>

### <span data-ttu-id="7fca6-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="7fca6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="7fca6-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fca6-125">NOTES</span></span>

## <span data-ttu-id="7fca6-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fca6-126">RELATED LINKS</span></span>
