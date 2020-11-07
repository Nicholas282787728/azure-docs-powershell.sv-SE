---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: b3e2b3ea03ca0bae0db1bea1606e4ae6b94a597e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922320"
---
# <span data-ttu-id="1da2b-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1da2b-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="1da2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1da2b-102">SYNOPSIS</span></span>
<span data-ttu-id="1da2b-103">Hämtar en befintlig Health PROBE-konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="1da2b-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="1da2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1da2b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1da2b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1da2b-105">DESCRIPTION</span></span>
<span data-ttu-id="1da2b-106">Den Get-AzApplicationGatewayProbeConfig cmdleten hämtar en befintlig Health PROBE-konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="1da2b-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="1da2b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1da2b-107">EXAMPLES</span></span>

### <span data-ttu-id="1da2b-108">Exempel 1: Hämta en befintlig sond från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="1da2b-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="1da2b-109">Det här kommandot får hälso avsökningen med namnet Probe02 från programgatewayen heter Gateway.</span><span class="sxs-lookup"><span data-stu-id="1da2b-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="1da2b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1da2b-110">PARAMETERS</span></span>

### <span data-ttu-id="1da2b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1da2b-111">-ApplicationGateway</span></span>
<span data-ttu-id="1da2b-112">Anger den Programgateway som denna cmdlet ska ha en PROBE-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="1da2b-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1da2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da2b-113">-DefaultProfile</span></span>
<span data-ttu-id="1da2b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1da2b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1da2b-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="1da2b-115">-Name</span></span>
<span data-ttu-id="1da2b-116">Anger namnet på sonden.</span><span class="sxs-lookup"><span data-stu-id="1da2b-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="1da2b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da2b-117">CommonParameters</span></span>
<span data-ttu-id="1da2b-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1da2b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da2b-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1da2b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da2b-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1da2b-120">INPUTS</span></span>

### <span data-ttu-id="1da2b-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1da2b-121">PSApplicationGateway</span></span>
<span data-ttu-id="1da2b-122">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="1da2b-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="1da2b-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1da2b-123">OUTPUTS</span></span>

### <span data-ttu-id="1da2b-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="1da2b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="1da2b-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. Network. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="1da2b-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="1da2b-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1da2b-126">NOTES</span></span>

## <span data-ttu-id="1da2b-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1da2b-127">RELATED LINKS</span></span>

[<span data-ttu-id="1da2b-128">Lägga till en sond i en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1da2b-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="1da2b-129">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1da2b-129">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="1da2b-130">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1da2b-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="1da2b-131">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1da2b-131">Remove-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="1da2b-132">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1da2b-132">Set-AzApplicationGatewayProbeConfig</span></span>]()

