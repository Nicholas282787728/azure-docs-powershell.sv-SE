---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 41693da553178bdd45d19da498a5774ef8d2fa60
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922161"
---
# <span data-ttu-id="90afa-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="90afa-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="90afa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90afa-102">SYNOPSIS</span></span>
<span data-ttu-id="90afa-103">Skapar ett hälso avsöknings svar som används av hälso sökning för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="90afa-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="90afa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90afa-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90afa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90afa-105">DESCRIPTION</span></span>
<span data-ttu-id="90afa-106">Cmdleten **Add-AzApplicationGatewayProbeHealthResponseMatch** skapar ett hälso avsöknings svar som används av hälso sökning för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="90afa-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="90afa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90afa-107">EXAMPLES</span></span>

### <span data-ttu-id="90afa-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="90afa-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="90afa-109">Det här kommandot skapar ett sjukvårds svar som kan skickas till ProbeConfig som en parameter.</span><span class="sxs-lookup"><span data-stu-id="90afa-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="90afa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90afa-110">PARAMETERS</span></span>

### <span data-ttu-id="90afa-111">-Body</span><span class="sxs-lookup"><span data-stu-id="90afa-111">-Body</span></span>
<span data-ttu-id="90afa-112">Brödtext som måste ingå i sjukvården.</span><span class="sxs-lookup"><span data-stu-id="90afa-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="90afa-113">Standardvärdet är inte ifyllt</span><span class="sxs-lookup"><span data-stu-id="90afa-113">Default value is empty</span></span>

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

### <span data-ttu-id="90afa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90afa-114">-DefaultProfile</span></span>
<span data-ttu-id="90afa-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90afa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90afa-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="90afa-116">-StatusCode</span></span>
<span data-ttu-id="90afa-117">Tillåtna intervall med felfria status koder. Standard intervallet för felfria status koder är 200-399</span><span class="sxs-lookup"><span data-stu-id="90afa-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90afa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90afa-118">CommonParameters</span></span>
<span data-ttu-id="90afa-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90afa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90afa-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90afa-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90afa-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90afa-121">INPUTS</span></span>

### <span data-ttu-id="90afa-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="90afa-122">None</span></span>

## <span data-ttu-id="90afa-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90afa-123">OUTPUTS</span></span>

### <span data-ttu-id="90afa-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="90afa-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="90afa-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90afa-125">NOTES</span></span>

## <span data-ttu-id="90afa-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90afa-126">RELATED LINKS</span></span>

