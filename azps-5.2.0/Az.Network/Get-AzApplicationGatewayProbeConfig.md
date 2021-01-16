---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389607"
---
# <span data-ttu-id="1f6da-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1f6da-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="1f6da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f6da-102">SYNOPSIS</span></span>
<span data-ttu-id="1f6da-103">Hämtar en befintlig Health PROBE-konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="1f6da-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="1f6da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f6da-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f6da-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f6da-105">DESCRIPTION</span></span>
<span data-ttu-id="1f6da-106">Den Get-AzApplicationGatewayProbeConfig cmdleten hämtar en befintlig Health PROBE-konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="1f6da-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="1f6da-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f6da-107">EXAMPLES</span></span>

### <span data-ttu-id="1f6da-108">Exempel 1: Hämta en befintlig sond från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="1f6da-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="1f6da-109">Det här kommandot får hälso avsökningen med namnet Probe02 från programgatewayen heter Gateway.</span><span class="sxs-lookup"><span data-stu-id="1f6da-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="1f6da-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f6da-110">PARAMETERS</span></span>

### <span data-ttu-id="1f6da-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f6da-111">-ApplicationGateway</span></span>
<span data-ttu-id="1f6da-112">Anger den Programgateway som denna cmdlet ska ha en PROBE-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="1f6da-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="1f6da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f6da-113">-DefaultProfile</span></span>
<span data-ttu-id="1f6da-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f6da-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f6da-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f6da-115">-Name</span></span>
<span data-ttu-id="1f6da-116">Anger namnet på sonden.</span><span class="sxs-lookup"><span data-stu-id="1f6da-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="1f6da-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f6da-117">CommonParameters</span></span>
<span data-ttu-id="1f6da-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f6da-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f6da-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f6da-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f6da-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f6da-120">INPUTS</span></span>

### <span data-ttu-id="1f6da-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f6da-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1f6da-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f6da-122">OUTPUTS</span></span>

### <span data-ttu-id="1f6da-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="1f6da-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="1f6da-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f6da-124">NOTES</span></span>

## <span data-ttu-id="1f6da-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f6da-125">RELATED LINKS</span></span>

[<span data-ttu-id="1f6da-126">Lägga till en sond i en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1f6da-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="1f6da-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1f6da-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="1f6da-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1f6da-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="1f6da-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1f6da-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="1f6da-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1f6da-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

