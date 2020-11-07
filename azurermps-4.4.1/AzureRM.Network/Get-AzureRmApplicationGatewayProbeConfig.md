---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 6583856eb6d44fa170b53a855e43db71602534a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574601"
---
# <span data-ttu-id="3e2fe-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e2fe-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="3e2fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e2fe-102">SYNOPSIS</span></span>
<span data-ttu-id="3e2fe-103">Hämtar en befintlig Health PROBE-konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3e2fe-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e2fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e2fe-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e2fe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e2fe-105">DESCRIPTION</span></span>
<span data-ttu-id="3e2fe-106">Den Get-AzureRmApplicationGatewayProbeConfig cmdleten hämtar en befintlig Health PROBE-konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3e2fe-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="3e2fe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e2fe-107">EXAMPLES</span></span>

### <span data-ttu-id="3e2fe-108">Exempel 1: Hämta en befintlig sond från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="3e2fe-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="3e2fe-109">Det här kommandot får hälso avsökningen med namnet Probe02 från programgatewayen heter Gateway.</span><span class="sxs-lookup"><span data-stu-id="3e2fe-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="3e2fe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e2fe-110">PARAMETERS</span></span>

### <span data-ttu-id="3e2fe-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e2fe-111">-ApplicationGateway</span></span>
<span data-ttu-id="3e2fe-112">Anger den Programgateway som denna cmdlet ska ha en PROBE-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="3e2fe-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="3e2fe-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e2fe-113">-Name</span></span>
<span data-ttu-id="3e2fe-114">Anger namnet på sonden.</span><span class="sxs-lookup"><span data-stu-id="3e2fe-114">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="3e2fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e2fe-115">-DefaultProfile</span></span>
<span data-ttu-id="3e2fe-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e2fe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e2fe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e2fe-117">CommonParameters</span></span>
<span data-ttu-id="3e2fe-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e2fe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e2fe-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e2fe-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e2fe-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e2fe-120">INPUTS</span></span>

### <span data-ttu-id="3e2fe-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e2fe-121">PSApplicationGateway</span></span>
<span data-ttu-id="3e2fe-122">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3e2fe-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="3e2fe-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e2fe-123">OUTPUTS</span></span>

### <span data-ttu-id="3e2fe-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="3e2fe-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="3e2fe-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. Network. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="3e2fe-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="3e2fe-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e2fe-126">NOTES</span></span>

## <span data-ttu-id="3e2fe-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e2fe-127">RELATED LINKS</span></span>

[<span data-ttu-id="3e2fe-128">Lägga till en sond i en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="3e2fe-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="3e2fe-129">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e2fe-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="3e2fe-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e2fe-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="3e2fe-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e2fe-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="3e2fe-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e2fe-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()
