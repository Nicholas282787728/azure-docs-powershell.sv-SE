---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: 79b61f5d96307afea47851b210fc1a1ee97acf61
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930549"
---
# <span data-ttu-id="6e802-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6e802-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="6e802-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e802-102">SYNOPSIS</span></span>
<span data-ttu-id="6e802-103">Hämtar HTTP-lyssnaren för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="6e802-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e802-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e802-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e802-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e802-105">DESCRIPTION</span></span>
<span data-ttu-id="6e802-106">Cmdleten **Get-AzureRmApplicationGatewayHttpListener** hämtar http-lyssnaren för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="6e802-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="6e802-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e802-107">EXAMPLES</span></span>

### <span data-ttu-id="6e802-108">Exempel 1: skaffa en viss HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="6e802-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="6e802-109">Det här kommandot får en HTTP-lyssnare som heter Listener01.</span><span class="sxs-lookup"><span data-stu-id="6e802-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="6e802-110">Exempel 2: Hämta en lista med HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="6e802-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="6e802-111">Det här kommandot får en lista med HTTP-lyssnare.</span><span class="sxs-lookup"><span data-stu-id="6e802-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="6e802-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e802-112">PARAMETERS</span></span>

### <span data-ttu-id="6e802-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6e802-113">-ApplicationGateway</span></span>
<span data-ttu-id="6e802-114">Anger det Application Gateway-objekt som innehåller HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="6e802-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="6e802-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e802-115">-DefaultProfile</span></span>
<span data-ttu-id="6e802-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6e802-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e802-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="6e802-117">-Name</span></span>
<span data-ttu-id="6e802-118">Anger namnet på den HTTP-lyssnare som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="6e802-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="6e802-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e802-119">CommonParameters</span></span>
<span data-ttu-id="6e802-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e802-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e802-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e802-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e802-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e802-122">INPUTS</span></span>

### <span data-ttu-id="6e802-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6e802-123">System.String</span></span>

## <span data-ttu-id="6e802-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e802-124">OUTPUTS</span></span>

### <span data-ttu-id="6e802-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6e802-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="6e802-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e802-126">NOTES</span></span>

## <span data-ttu-id="6e802-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e802-127">RELATED LINKS</span></span>

[<span data-ttu-id="6e802-128">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6e802-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="6e802-129">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6e802-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="6e802-130">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6e802-130">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="6e802-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6e802-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


