---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 5b4f0568574b6ec6994d0c195568306e9d2e4a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758036"
---
# <span data-ttu-id="7e45a-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7e45a-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="7e45a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e45a-102">SYNOPSIS</span></span>
<span data-ttu-id="7e45a-103">Tar bort en regel för en anslutningsbegäran från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7e45a-103">Removes a request routing rule from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e45a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e45a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e45a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e45a-105">DESCRIPTION</span></span>
<span data-ttu-id="7e45a-106">Cmdleten **Remove-AzureRmApplicationGatewayRequestRoutingRule** tar bort en regel för anslutningsbegäran från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7e45a-106">The **Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="7e45a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e45a-107">EXAMPLES</span></span>

### <span data-ttu-id="7e45a-108">Exempel 1: ta bort en regel för en anslutningsbegäran från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="7e45a-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="7e45a-109">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="7e45a-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="7e45a-110">Det andra kommandot tar bort regeln för anslutningsbegäran med namnet Rule02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7e45a-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="7e45a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e45a-111">PARAMETERS</span></span>

### <span data-ttu-id="7e45a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e45a-112">-ApplicationGateway</span></span>
<span data-ttu-id="7e45a-113">Anger den Programgateway från vilken en anslutningsbegäran ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7e45a-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="7e45a-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e45a-114">-Name</span></span>
<span data-ttu-id="7e45a-115">Anger namnet på regeln för anslutningsbegäran som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="7e45a-115">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="7e45a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e45a-116">-DefaultProfile</span></span>
<span data-ttu-id="7e45a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e45a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e45a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e45a-118">CommonParameters</span></span>
<span data-ttu-id="7e45a-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e45a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e45a-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e45a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e45a-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e45a-121">INPUTS</span></span>

### <span data-ttu-id="7e45a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="7e45a-122">System.String</span></span>

## <span data-ttu-id="7e45a-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e45a-123">OUTPUTS</span></span>

### <span data-ttu-id="7e45a-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7e45a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="7e45a-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e45a-125">NOTES</span></span>

## <span data-ttu-id="7e45a-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e45a-126">RELATED LINKS</span></span>

[<span data-ttu-id="7e45a-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7e45a-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7e45a-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7e45a-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7e45a-129">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7e45a-129">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7e45a-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7e45a-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


