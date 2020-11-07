---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 402084acc332102c8a2f003e31e140b175b6f22f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922319"
---
# <span data-ttu-id="67e49-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="67e49-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="67e49-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67e49-102">SYNOPSIS</span></span>
<span data-ttu-id="67e49-103">Hämtar regeln för anslutningsbegäran för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="67e49-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="67e49-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67e49-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67e49-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67e49-105">DESCRIPTION</span></span>
<span data-ttu-id="67e49-106">Cmdleten **Get-AzApplicationGatewayRequestRoutingRule** hämtar regeln för anslutningsbegäran för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="67e49-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="67e49-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67e49-107">EXAMPLES</span></span>

### <span data-ttu-id="67e49-108">Exempel 1: skaffa en specifik regel för en anslutningsbegäran</span><span class="sxs-lookup"><span data-stu-id="67e49-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="67e49-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="67e49-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="67e49-110">Det andra kommandot hämtar regeln för anslutningsbegäran med namnet Rule01 från Application Gateway som lagras i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="67e49-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="67e49-111">Exempel 2: få en lista över regler för routning för begäran</span><span class="sxs-lookup"><span data-stu-id="67e49-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="67e49-112">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="67e49-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="67e49-113">Det andra kommandot får en lista med routningsregler för routning från Application Gateway som lagras i variabeln $AppGW.</span><span class="sxs-lookup"><span data-stu-id="67e49-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="67e49-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67e49-114">PARAMETERS</span></span>

### <span data-ttu-id="67e49-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67e49-115">-ApplicationGateway</span></span>
<span data-ttu-id="67e49-116">Anger det Application Gateway-objekt som innehåller routningsregler för begäran.</span><span class="sxs-lookup"><span data-stu-id="67e49-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="67e49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e49-117">-DefaultProfile</span></span>
<span data-ttu-id="67e49-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67e49-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67e49-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="67e49-119">-Name</span></span>
<span data-ttu-id="67e49-120">Anger namnet på regeln för anslutningsbegäran som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="67e49-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="67e49-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e49-121">CommonParameters</span></span>
<span data-ttu-id="67e49-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67e49-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e49-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e49-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e49-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67e49-124">INPUTS</span></span>

### <span data-ttu-id="67e49-125">System. String</span><span class="sxs-lookup"><span data-stu-id="67e49-125">System.String</span></span>

## <span data-ttu-id="67e49-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67e49-126">OUTPUTS</span></span>

### <span data-ttu-id="67e49-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="67e49-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="67e49-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67e49-128">NOTES</span></span>

## <span data-ttu-id="67e49-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67e49-129">RELATED LINKS</span></span>

[<span data-ttu-id="67e49-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="67e49-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="67e49-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="67e49-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="67e49-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="67e49-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="67e49-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="67e49-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


