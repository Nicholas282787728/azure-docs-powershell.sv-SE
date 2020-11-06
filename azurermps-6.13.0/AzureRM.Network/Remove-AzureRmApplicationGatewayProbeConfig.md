---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 40a7e63150384ac3fa2c330c079d5377c836d52e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576192"
---
# <span data-ttu-id="7e2a1-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7e2a1-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="7e2a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e2a1-102">SYNOPSIS</span></span>
<span data-ttu-id="7e2a1-103">Tar bort en hälso sökning från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7e2a1-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e2a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e2a1-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e2a1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e2a1-105">DESCRIPTION</span></span>
<span data-ttu-id="7e2a1-106">Remove-AzureRmApplicationGatewayProbeConfig cmdlet tar bort en Heath PROBE från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7e2a1-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="7e2a1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e2a1-107">EXAMPLES</span></span>

### <span data-ttu-id="7e2a1-108">Exempel 1: ta bort en hälso sökning från en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7e2a1-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="7e2a1-109">Det här kommandot tar bort hälso avsökningen med namnet Probe04 från gatewayen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="7e2a1-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="7e2a1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e2a1-110">PARAMETERS</span></span>

### <span data-ttu-id="7e2a1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e2a1-111">-ApplicationGateway</span></span>
<span data-ttu-id="7e2a1-112">Anger den Programgateway som denna cmdlet tar bort en sond för.</span><span class="sxs-lookup"><span data-stu-id="7e2a1-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="7e2a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e2a1-113">-DefaultProfile</span></span>
<span data-ttu-id="7e2a1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e2a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e2a1-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e2a1-115">-Name</span></span>
<span data-ttu-id="7e2a1-116">Anger namnet på den sond som cmdleten tas bort för.</span><span class="sxs-lookup"><span data-stu-id="7e2a1-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="7e2a1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e2a1-117">CommonParameters</span></span>
<span data-ttu-id="7e2a1-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e2a1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e2a1-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e2a1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e2a1-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e2a1-120">INPUTS</span></span>

### <span data-ttu-id="7e2a1-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e2a1-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="7e2a1-122">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e2a1-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="7e2a1-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e2a1-123">OUTPUTS</span></span>

### <span data-ttu-id="7e2a1-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e2a1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7e2a1-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e2a1-125">NOTES</span></span>

## <span data-ttu-id="7e2a1-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e2a1-126">RELATED LINKS</span></span>

[<span data-ttu-id="7e2a1-127">Ta bort en sond från en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7e2a1-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="7e2a1-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7e2a1-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7e2a1-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7e2a1-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7e2a1-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7e2a1-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7e2a1-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7e2a1-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

