---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: de019ffd1bc3be0e66cef6e8a15912f18b05f770
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931321"
---
# <span data-ttu-id="68834-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="68834-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="68834-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68834-102">SYNOPSIS</span></span>
<span data-ttu-id="68834-103">Hämtar regeln för anslutningsbegäran för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="68834-103">Gets the request routing rule of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68834-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68834-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68834-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68834-105">DESCRIPTION</span></span>
<span data-ttu-id="68834-106">Cmdleten **Get-AzureRmApplicationGatewayRequestRoutingRule** hämtar regeln för anslutningsbegäran för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="68834-106">The **Get-AzureRmApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="68834-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68834-107">EXAMPLES</span></span>

### <span data-ttu-id="68834-108">Exempel 1: skaffa en specifik regel för en anslutningsbegäran</span><span class="sxs-lookup"><span data-stu-id="68834-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzureRmApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="68834-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="68834-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="68834-110">Det andra kommandot hämtar regeln för anslutningsbegäran med namnet Rule01 från Application Gateway som lagras i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="68834-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="68834-111">Exempel 2: få en lista över regler för routning för begäran</span><span class="sxs-lookup"><span data-stu-id="68834-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="68834-112">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="68834-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="68834-113">Det andra kommandot får en lista med routningsregler för routning från Application Gateway som lagras i variabeln $AppGW.</span><span class="sxs-lookup"><span data-stu-id="68834-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="68834-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68834-114">PARAMETERS</span></span>

### <span data-ttu-id="68834-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68834-115">-ApplicationGateway</span></span>
<span data-ttu-id="68834-116">Anger det Application Gateway-objekt som innehåller routningsregler för begäran.</span><span class="sxs-lookup"><span data-stu-id="68834-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="68834-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68834-117">-DefaultProfile</span></span>
<span data-ttu-id="68834-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="68834-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68834-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="68834-119">-Name</span></span>
<span data-ttu-id="68834-120">Anger namnet på regeln för anslutningsbegäran som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="68834-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="68834-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68834-121">CommonParameters</span></span>
<span data-ttu-id="68834-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68834-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68834-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68834-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68834-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68834-124">INPUTS</span></span>

### <span data-ttu-id="68834-125">System. String</span><span class="sxs-lookup"><span data-stu-id="68834-125">System.String</span></span>

## <span data-ttu-id="68834-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68834-126">OUTPUTS</span></span>

### <span data-ttu-id="68834-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="68834-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="68834-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68834-128">NOTES</span></span>

## <span data-ttu-id="68834-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68834-129">RELATED LINKS</span></span>

[<span data-ttu-id="68834-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="68834-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="68834-131">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="68834-131">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="68834-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="68834-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="68834-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="68834-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


