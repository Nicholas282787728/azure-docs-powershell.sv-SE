---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: 859ef684424069bb5fc4c5b45de3e722f0921705
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929329"
---
# <span data-ttu-id="4ee8a-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4ee8a-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="4ee8a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ee8a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee8a-103">Tar bort en regel för en anslutningsbegäran från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4ee8a-103">Removes a request routing rule from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ee8a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ee8a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ee8a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ee8a-105">DESCRIPTION</span></span>
<span data-ttu-id="4ee8a-106">Cmdleten **Remove-AzureRmApplicationGatewayRequestRoutingRule** tar bort en regel för anslutningsbegäran från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4ee8a-106">The **Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="4ee8a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ee8a-107">EXAMPLES</span></span>

### <span data-ttu-id="4ee8a-108">Exempel 1: ta bort en regel för en anslutningsbegäran från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="4ee8a-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="4ee8a-109">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="4ee8a-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="4ee8a-110">Det andra kommandot tar bort regeln för anslutningsbegäran med namnet Rule02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4ee8a-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4ee8a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ee8a-111">PARAMETERS</span></span>

### <span data-ttu-id="4ee8a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ee8a-112">-ApplicationGateway</span></span>
<span data-ttu-id="4ee8a-113">Anger den Programgateway från vilken en anslutningsbegäran ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4ee8a-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="4ee8a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee8a-114">-DefaultProfile</span></span>
<span data-ttu-id="4ee8a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ee8a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ee8a-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ee8a-116">-Name</span></span>
<span data-ttu-id="4ee8a-117">Anger namnet på regeln för anslutningsbegäran som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="4ee8a-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee8a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee8a-118">CommonParameters</span></span>
<span data-ttu-id="4ee8a-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee8a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee8a-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee8a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee8a-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ee8a-121">INPUTS</span></span>

### <span data-ttu-id="4ee8a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="4ee8a-122">System.String</span></span>

## <span data-ttu-id="4ee8a-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ee8a-123">OUTPUTS</span></span>

### <span data-ttu-id="4ee8a-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4ee8a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="4ee8a-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ee8a-125">NOTES</span></span>

## <span data-ttu-id="4ee8a-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ee8a-126">RELATED LINKS</span></span>

[<span data-ttu-id="4ee8a-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4ee8a-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4ee8a-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4ee8a-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4ee8a-129">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4ee8a-129">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4ee8a-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4ee8a-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


