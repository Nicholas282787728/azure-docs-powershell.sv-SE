---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 2730e3ba1e85a876940492b4abfd4fbe5dbca956
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581731"
---
# <span data-ttu-id="e5694-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e5694-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="e5694-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5694-102">SYNOPSIS</span></span>
<span data-ttu-id="e5694-103">Hämtar en befintlig Health PROBE-konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e5694-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5694-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5694-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5694-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5694-105">DESCRIPTION</span></span>
<span data-ttu-id="e5694-106">Den Get-AzureRmApplicationGatewayProbeConfig cmdleten hämtar en befintlig Health PROBE-konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e5694-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="e5694-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5694-107">EXAMPLES</span></span>

### <span data-ttu-id="e5694-108">Exempel 1: Hämta en befintlig sond från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="e5694-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="e5694-109">Det här kommandot får hälso avsökningen med namnet Probe02 från programgatewayen heter Gateway.</span><span class="sxs-lookup"><span data-stu-id="e5694-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="e5694-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5694-110">PARAMETERS</span></span>

### <span data-ttu-id="e5694-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5694-111">-ApplicationGateway</span></span>
<span data-ttu-id="e5694-112">Anger den Programgateway som denna cmdlet ska ha en PROBE-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="e5694-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="e5694-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5694-113">-DefaultProfile</span></span>
<span data-ttu-id="e5694-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5694-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5694-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5694-115">-Name</span></span>
<span data-ttu-id="e5694-116">Anger namnet på sonden.</span><span class="sxs-lookup"><span data-stu-id="e5694-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="e5694-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5694-117">CommonParameters</span></span>
<span data-ttu-id="e5694-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5694-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5694-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5694-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5694-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5694-120">INPUTS</span></span>

### <span data-ttu-id="e5694-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5694-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="e5694-122">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e5694-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="e5694-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5694-123">OUTPUTS</span></span>

### <span data-ttu-id="e5694-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="e5694-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="e5694-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5694-125">NOTES</span></span>

## <span data-ttu-id="e5694-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5694-126">RELATED LINKS</span></span>

[<span data-ttu-id="e5694-127">Lägga till en sond i en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e5694-127">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="e5694-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e5694-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e5694-129">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e5694-129">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e5694-130">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e5694-130">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e5694-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e5694-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

