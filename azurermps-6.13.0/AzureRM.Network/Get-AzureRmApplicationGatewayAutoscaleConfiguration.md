---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f9be647a4c6cb9d5198edcc766a20b3588e7626b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574813"
---
# <span data-ttu-id="b28b9-101">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b28b9-101">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="b28b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b28b9-102">SYNOPSIS</span></span>
<span data-ttu-id="b28b9-103">Hämtar autoskalans konfiguration för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="b28b9-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b28b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b28b9-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b28b9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b28b9-105">DESCRIPTION</span></span>
<span data-ttu-id="b28b9-106">Cmdleten **Get-AzureRmApplicationGatewayAutoscaleConfiguration** hämtar autoskalans konfiguration för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="b28b9-106">The **Get-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="b28b9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b28b9-107">EXAMPLES</span></span>

### <span data-ttu-id="b28b9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b28b9-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="b28b9-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="b28b9-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="b28b9-110">Det andra kommandot extraherar autoskalans konfiguration från applicationg Gateway.</span><span class="sxs-lookup"><span data-stu-id="b28b9-110">The second command extracts out the autoscale configuration from the applicationg gateway.</span></span>

## <span data-ttu-id="b28b9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b28b9-111">PARAMETERS</span></span>

### <span data-ttu-id="b28b9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b28b9-112">-ApplicationGateway</span></span>
<span data-ttu-id="b28b9-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b28b9-113">The applicationGateway</span></span>

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

### <span data-ttu-id="b28b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b28b9-114">-DefaultProfile</span></span>
<span data-ttu-id="b28b9-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b28b9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b28b9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b28b9-116">CommonParameters</span></span>
<span data-ttu-id="b28b9-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b28b9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b28b9-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b28b9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b28b9-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b28b9-119">INPUTS</span></span>

### <span data-ttu-id="b28b9-120">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b28b9-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b28b9-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b28b9-121">OUTPUTS</span></span>

### <span data-ttu-id="b28b9-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b28b9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="b28b9-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b28b9-123">NOTES</span></span>

## <span data-ttu-id="b28b9-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b28b9-124">RELATED LINKS</span></span>
