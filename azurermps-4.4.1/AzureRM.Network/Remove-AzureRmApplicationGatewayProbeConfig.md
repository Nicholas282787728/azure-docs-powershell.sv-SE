---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: df81af46023c1e28ecfe39cf880f45cd9b2319ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757776"
---
# <span data-ttu-id="8b7a5-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8b7a5-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="8b7a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b7a5-102">SYNOPSIS</span></span>
<span data-ttu-id="8b7a5-103">Tar bort en hälso sökning från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8b7a5-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b7a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b7a5-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b7a5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b7a5-105">DESCRIPTION</span></span>
<span data-ttu-id="8b7a5-106">Remove-AzureRmApplicationGatewayProbeConfig cmdlet tar bort en Heath PROBE från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8b7a5-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="8b7a5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b7a5-107">EXAMPLES</span></span>

### <span data-ttu-id="8b7a5-108">Exempel 1: ta bort en hälso sökning från en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8b7a5-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="8b7a5-109">Det här kommandot tar bort hälso avsökningen med namnet Probe04 från gatewayen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="8b7a5-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="8b7a5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b7a5-110">PARAMETERS</span></span>

### <span data-ttu-id="8b7a5-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b7a5-111">-ApplicationGateway</span></span>
<span data-ttu-id="8b7a5-112">Anger den Programgateway som denna cmdlet tar bort en sond för.</span><span class="sxs-lookup"><span data-stu-id="8b7a5-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b7a5-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b7a5-113">-Name</span></span>
<span data-ttu-id="8b7a5-114">Anger namnet på den sond som cmdleten tas bort för.</span><span class="sxs-lookup"><span data-stu-id="8b7a5-114">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="8b7a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b7a5-115">-DefaultProfile</span></span>
<span data-ttu-id="8b7a5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b7a5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b7a5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b7a5-117">CommonParameters</span></span>
<span data-ttu-id="8b7a5-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b7a5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b7a5-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b7a5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b7a5-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b7a5-120">INPUTS</span></span>

### <span data-ttu-id="8b7a5-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b7a5-121">PSApplicationGateway</span></span>
<span data-ttu-id="8b7a5-122">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="8b7a5-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="8b7a5-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b7a5-123">OUTPUTS</span></span>

### <span data-ttu-id="8b7a5-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b7a5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8b7a5-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b7a5-125">NOTES</span></span>

## <span data-ttu-id="8b7a5-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b7a5-126">RELATED LINKS</span></span>

[<span data-ttu-id="8b7a5-127">Ta bort en sond från en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8b7a5-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="8b7a5-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8b7a5-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="8b7a5-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8b7a5-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="8b7a5-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8b7a5-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="8b7a5-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8b7a5-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

