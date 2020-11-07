---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: a60fa54e5d705a71407f2c56986200c897b838e3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929685"
---
# <span data-ttu-id="0abde-101">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0abde-101">Remove-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="0abde-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0abde-102">SYNOPSIS</span></span>
<span data-ttu-id="0abde-103">Tar bort en HTTP-lyssnare från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="0abde-103">Removes an HTTP listener from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0abde-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0abde-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0abde-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0abde-105">DESCRIPTION</span></span>
<span data-ttu-id="0abde-106">Cmdleten **Remove-AzureRmApplicationGatewayHttpListener** tar bort en http-lyssnare från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0abde-106">The **Remove-AzureRmApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="0abde-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0abde-107">EXAMPLES</span></span>

### <span data-ttu-id="0abde-108">Exempel 1: ta bort en HTTP-lyssnare för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="0abde-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="0abde-109">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="0abde-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="0abde-110">Med det andra kommandot tas HTTP-lyssnaren bort med namnet Listener02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0abde-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="0abde-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0abde-111">PARAMETERS</span></span>

### <span data-ttu-id="0abde-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0abde-112">-ApplicationGateway</span></span>
<span data-ttu-id="0abde-113">Anger den Programgateway från vilken du vill ta bort en HTTP-lyssnare.</span><span class="sxs-lookup"><span data-stu-id="0abde-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="0abde-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0abde-114">-DefaultProfile</span></span>
<span data-ttu-id="0abde-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0abde-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0abde-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0abde-116">-Name</span></span>
<span data-ttu-id="0abde-117">Anger namnet på den HTTP-lyssnare som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0abde-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0abde-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0abde-118">CommonParameters</span></span>
<span data-ttu-id="0abde-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0abde-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0abde-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0abde-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0abde-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0abde-121">INPUTS</span></span>

### <span data-ttu-id="0abde-122">System. String</span><span class="sxs-lookup"><span data-stu-id="0abde-122">System.String</span></span>

## <span data-ttu-id="0abde-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0abde-123">OUTPUTS</span></span>

### <span data-ttu-id="0abde-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0abde-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="0abde-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0abde-125">NOTES</span></span>

## <span data-ttu-id="0abde-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0abde-126">RELATED LINKS</span></span>

[<span data-ttu-id="0abde-127">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0abde-127">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="0abde-128">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0abde-128">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="0abde-129">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0abde-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="0abde-130">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0abde-130">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


