---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: b4238f5b1492afad7d09ee9c338a346d5f54a5e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407208"
---
# <span data-ttu-id="9e93c-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e93c-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="9e93c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e93c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e93c-103">Hämtar autoskalans konfiguration för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="9e93c-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="9e93c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e93c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e93c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e93c-105">DESCRIPTION</span></span>
<span data-ttu-id="9e93c-106">Cmdleten **Get-AzApplicationGatewayAutoscaleConfiguration** hämtar autoskalans konfiguration för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="9e93c-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="9e93c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e93c-107">EXAMPLES</span></span>

### <span data-ttu-id="9e93c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9e93c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="9e93c-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="9e93c-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="9e93c-110">Det andra kommandot extraherar autoskalans konfiguration från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9e93c-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="9e93c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e93c-111">PARAMETERS</span></span>

### <span data-ttu-id="9e93c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e93c-112">-ApplicationGateway</span></span>
<span data-ttu-id="9e93c-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e93c-113">The applicationGateway</span></span>

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

### <span data-ttu-id="9e93c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e93c-114">-DefaultProfile</span></span>
<span data-ttu-id="9e93c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e93c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e93c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e93c-116">CommonParameters</span></span>
<span data-ttu-id="9e93c-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e93c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e93c-118">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e93c-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e93c-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e93c-119">INPUTS</span></span>

### <span data-ttu-id="9e93c-120">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e93c-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9e93c-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e93c-121">OUTPUTS</span></span>

### <span data-ttu-id="9e93c-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e93c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="9e93c-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e93c-123">NOTES</span></span>

## <span data-ttu-id="9e93c-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e93c-124">RELATED LINKS</span></span>

[<span data-ttu-id="9e93c-125">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e93c-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="9e93c-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e93c-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="9e93c-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e93c-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
