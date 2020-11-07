---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 6b54c300eb6e37544246b785fe30b2a3dcb67b9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757278"
---
# <span data-ttu-id="842a0-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="842a0-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="842a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="842a0-102">SYNOPSIS</span></span>
<span data-ttu-id="842a0-103">Skapar ett hälso avsöknings svar som används av hälso sökning för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="842a0-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="842a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="842a0-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="842a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="842a0-105">DESCRIPTION</span></span>
<span data-ttu-id="842a0-106">Cmdleten **Add-AzureRmApplicationGatewayProbeHealthResponseMatch** skapar ett hälso avsöknings svar som används av hälso sökning för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="842a0-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="842a0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="842a0-107">EXAMPLES</span></span>

### <span data-ttu-id="842a0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="842a0-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="842a0-109">Det här kommandot skapar ett sjukvårds svar som kan skickas till ProbeConfig som en parameter.</span><span class="sxs-lookup"><span data-stu-id="842a0-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="842a0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="842a0-110">PARAMETERS</span></span>

### <span data-ttu-id="842a0-111">-Body</span><span class="sxs-lookup"><span data-stu-id="842a0-111">-Body</span></span>
<span data-ttu-id="842a0-112">Brödtext som måste ingå i sjukvården.</span><span class="sxs-lookup"><span data-stu-id="842a0-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="842a0-113">Standardvärdet är inte ifyllt</span><span class="sxs-lookup"><span data-stu-id="842a0-113">Default value is empty</span></span>

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

### <span data-ttu-id="842a0-114">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="842a0-114">-StatusCode</span></span>
<span data-ttu-id="842a0-115">Tillåtna intervall med felfria status koder. Standard intervallet för felfria status koder är 200-399</span><span class="sxs-lookup"><span data-stu-id="842a0-115">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="842a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="842a0-116">-DefaultProfile</span></span>
<span data-ttu-id="842a0-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="842a0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="842a0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="842a0-118">CommonParameters</span></span>
<span data-ttu-id="842a0-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="842a0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="842a0-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="842a0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="842a0-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="842a0-121">INPUTS</span></span>

### <span data-ttu-id="842a0-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="842a0-122">None</span></span>

## <span data-ttu-id="842a0-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="842a0-123">OUTPUTS</span></span>

### <span data-ttu-id="842a0-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="842a0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="842a0-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="842a0-125">NOTES</span></span>

## <span data-ttu-id="842a0-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="842a0-126">RELATED LINKS</span></span>

