---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 0cb29f9ad00c2412d9ab492bba780e977ef6b571
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757867"
---
# <span data-ttu-id="7749b-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7749b-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7749b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7749b-102">SYNOPSIS</span></span>
<span data-ttu-id="7749b-103">Hämtar HTTP-lyssnaren för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7749b-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7749b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7749b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7749b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7749b-105">DESCRIPTION</span></span>
<span data-ttu-id="7749b-106">Cmdleten **Get-AzureRmApplicationGatewayHttpListener** hämtar http-lyssnaren för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7749b-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="7749b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7749b-107">EXAMPLES</span></span>

### <span data-ttu-id="7749b-108">Exempel 1: skaffa en viss HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="7749b-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="7749b-109">Det här kommandot får en HTTP-lyssnare som heter Listener01.</span><span class="sxs-lookup"><span data-stu-id="7749b-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="7749b-110">Exempel 2: Hämta en lista med HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="7749b-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="7749b-111">Det här kommandot får en lista med HTTP-lyssnare.</span><span class="sxs-lookup"><span data-stu-id="7749b-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="7749b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7749b-112">PARAMETERS</span></span>

### <span data-ttu-id="7749b-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7749b-113">-ApplicationGateway</span></span>
<span data-ttu-id="7749b-114">Anger det Application Gateway-objekt som innehåller HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="7749b-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="7749b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7749b-115">-DefaultProfile</span></span>
<span data-ttu-id="7749b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7749b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7749b-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="7749b-117">-Name</span></span>
<span data-ttu-id="7749b-118">Anger namnet på den HTTP-lyssnare som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="7749b-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7749b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7749b-119">CommonParameters</span></span>
<span data-ttu-id="7749b-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7749b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7749b-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7749b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7749b-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7749b-122">INPUTS</span></span>

### <span data-ttu-id="7749b-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7749b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="7749b-124">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7749b-124">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="7749b-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7749b-125">OUTPUTS</span></span>

### <span data-ttu-id="7749b-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7749b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7749b-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7749b-127">NOTES</span></span>

## <span data-ttu-id="7749b-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7749b-128">RELATED LINKS</span></span>

[<span data-ttu-id="7749b-129">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7749b-129">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="7749b-130">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7749b-130">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="7749b-131">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7749b-131">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="7749b-132">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7749b-132">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


