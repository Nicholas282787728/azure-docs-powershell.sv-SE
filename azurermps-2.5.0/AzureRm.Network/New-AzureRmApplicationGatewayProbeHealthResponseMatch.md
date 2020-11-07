---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobehealthresponsematch
schema: 2.0.0
ms.openlocfilehash: 8781b52c3ed50a2a533b90815f1637ebcfe6df52
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928713"
---
# <span data-ttu-id="eea91-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="eea91-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="eea91-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eea91-102">SYNOPSIS</span></span>
<span data-ttu-id="eea91-103">Skapar ett hälso avsöknings svar som används av hälso sökning för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="eea91-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eea91-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eea91-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eea91-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eea91-105">DESCRIPTION</span></span>
<span data-ttu-id="eea91-106">Cmdleten **Add-AzureRmApplicationGatewayProbeHealthResponseMatch** skapar ett hälso avsöknings svar som används av hälso sökning för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="eea91-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="eea91-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eea91-107">EXAMPLES</span></span>

### <span data-ttu-id="eea91-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eea91-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="eea91-109">Det här kommandot skapar ett sjukvårds svar som kan skickas till ProbeConfig som en parameter.</span><span class="sxs-lookup"><span data-stu-id="eea91-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="eea91-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eea91-110">PARAMETERS</span></span>

### <span data-ttu-id="eea91-111">-Body</span><span class="sxs-lookup"><span data-stu-id="eea91-111">-Body</span></span>
<span data-ttu-id="eea91-112">Brödtext som måste ingå i sjukvården.</span><span class="sxs-lookup"><span data-stu-id="eea91-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="eea91-113">Standardvärdet är inte ifyllt</span><span class="sxs-lookup"><span data-stu-id="eea91-113">Default value is empty</span></span>

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

### <span data-ttu-id="eea91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea91-114">-DefaultProfile</span></span>
<span data-ttu-id="eea91-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eea91-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eea91-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="eea91-116">-StatusCode</span></span>
<span data-ttu-id="eea91-117">Tillåtna intervall med felfria status koder. Standard intervallet för felfria status koder är 200-399</span><span class="sxs-lookup"><span data-stu-id="eea91-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="eea91-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea91-118">CommonParameters</span></span>
<span data-ttu-id="eea91-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea91-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea91-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea91-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea91-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eea91-121">INPUTS</span></span>

### <span data-ttu-id="eea91-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="eea91-122">None</span></span>

## <span data-ttu-id="eea91-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eea91-123">OUTPUTS</span></span>

### <span data-ttu-id="eea91-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="eea91-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="eea91-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eea91-125">NOTES</span></span>

## <span data-ttu-id="eea91-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eea91-126">RELATED LINKS</span></span>

