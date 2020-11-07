---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 286afc05e9b7c825f183aabe7a78c965c790cb02
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931325"
---
# <span data-ttu-id="743d5-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="743d5-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="743d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="743d5-102">SYNOPSIS</span></span>
<span data-ttu-id="743d5-103">Hämtar en befintlig konfiguration för omdirigering från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="743d5-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="743d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="743d5-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="743d5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="743d5-105">DESCRIPTION</span></span>
<span data-ttu-id="743d5-106">Cmdleten **Get-AzureRmApplicationGatewayRedirectConfiguration** hämtar en befintlig konfiguration för omdirigering från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="743d5-106">The **Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="743d5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="743d5-107">EXAMPLES</span></span>

### <span data-ttu-id="743d5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="743d5-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="743d5-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="743d5-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="743d5-110">Det andra kommandot får till gång till omdirigeringsvariabler med namnet Redirect01 från Application Gateway som lagras i variabeln $AppGW.</span><span class="sxs-lookup"><span data-stu-id="743d5-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="743d5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="743d5-111">PARAMETERS</span></span>

### <span data-ttu-id="743d5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="743d5-112">-ApplicationGateway</span></span>
<span data-ttu-id="743d5-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="743d5-113">The applicationGateway</span></span>

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

### <span data-ttu-id="743d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743d5-114">-DefaultProfile</span></span>
<span data-ttu-id="743d5-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="743d5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="743d5-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="743d5-116">-Name</span></span>
<span data-ttu-id="743d5-117">Namnet på regeln för anslutningsbegäran</span><span class="sxs-lookup"><span data-stu-id="743d5-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="743d5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743d5-118">CommonParameters</span></span>
<span data-ttu-id="743d5-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="743d5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743d5-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="743d5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743d5-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="743d5-121">INPUTS</span></span>

### <span data-ttu-id="743d5-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="743d5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="743d5-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="743d5-123">OUTPUTS</span></span>

### <span data-ttu-id="743d5-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="743d5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="743d5-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. commands. Network, version = 4.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="743d5-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="743d5-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="743d5-126">NOTES</span></span>

## <span data-ttu-id="743d5-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="743d5-127">RELATED LINKS</span></span>

