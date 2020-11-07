---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: eedb3eb0df28b3f02690a2462b9367995235fcc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747933"
---
# <span data-ttu-id="c5cc0-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c5cc0-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="c5cc0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="c5cc0-103">Tar bort en hälso sökning från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c5cc0-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="c5cc0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5cc0-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5cc0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5cc0-105">DESCRIPTION</span></span>
<span data-ttu-id="c5cc0-106">Remove-AzApplicationGatewayProbeConfig cmdlet tar bort en Heath PROBE från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c5cc0-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="c5cc0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5cc0-107">EXAMPLES</span></span>

### <span data-ttu-id="c5cc0-108">Exempel 1: ta bort en hälso sökning från en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="c5cc0-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="c5cc0-109">Det här kommandot tar bort hälso avsökningen med namnet Probe04 från gatewayen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="c5cc0-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="c5cc0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5cc0-110">PARAMETERS</span></span>

### <span data-ttu-id="c5cc0-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c5cc0-111">-ApplicationGateway</span></span>
<span data-ttu-id="c5cc0-112">Anger den Programgateway som denna cmdlet tar bort en sond för.</span><span class="sxs-lookup"><span data-stu-id="c5cc0-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="c5cc0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5cc0-113">-DefaultProfile</span></span>
<span data-ttu-id="c5cc0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c5cc0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5cc0-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c5cc0-115">-Name</span></span>
<span data-ttu-id="c5cc0-116">Anger namnet på den sond som cmdleten tas bort för.</span><span class="sxs-lookup"><span data-stu-id="c5cc0-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="c5cc0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5cc0-117">CommonParameters</span></span>
<span data-ttu-id="c5cc0-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5cc0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5cc0-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5cc0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5cc0-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5cc0-120">INPUTS</span></span>

### <span data-ttu-id="c5cc0-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c5cc0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c5cc0-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5cc0-122">OUTPUTS</span></span>

### <span data-ttu-id="c5cc0-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c5cc0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c5cc0-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5cc0-124">NOTES</span></span>

## <span data-ttu-id="c5cc0-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5cc0-125">RELATED LINKS</span></span>

[<span data-ttu-id="c5cc0-126">Ta bort en sond från en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="c5cc0-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="c5cc0-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c5cc0-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="c5cc0-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c5cc0-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="c5cc0-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c5cc0-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="c5cc0-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c5cc0-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)
