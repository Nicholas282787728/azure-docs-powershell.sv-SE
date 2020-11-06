---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 564c586218297b8a22f0763a6747b6b451018a5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574605"
---
# <span data-ttu-id="c42aa-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c42aa-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="c42aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c42aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c42aa-103">Hämtar HTTP-lyssnaren för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c42aa-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c42aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c42aa-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c42aa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c42aa-105">DESCRIPTION</span></span>
<span data-ttu-id="c42aa-106">Cmdleten **Get-AzureRmApplicationGatewayHttpListener** hämtar http-lyssnaren för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c42aa-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="c42aa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c42aa-107">EXAMPLES</span></span>

### <span data-ttu-id="c42aa-108">Exempel 1: skaffa en viss HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="c42aa-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="c42aa-109">Det här kommandot får en HTTP-lyssnare som heter Listener01.</span><span class="sxs-lookup"><span data-stu-id="c42aa-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="c42aa-110">Exempel 2: Hämta en lista med HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="c42aa-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="c42aa-111">Det här kommandot får en lista med HTTP-lyssnare.</span><span class="sxs-lookup"><span data-stu-id="c42aa-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="c42aa-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c42aa-112">PARAMETERS</span></span>

### <span data-ttu-id="c42aa-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c42aa-113">-ApplicationGateway</span></span>
<span data-ttu-id="c42aa-114">Anger det Application Gateway-objekt som innehåller HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="c42aa-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="c42aa-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c42aa-115">-Name</span></span>
<span data-ttu-id="c42aa-116">Anger namnet på den HTTP-lyssnare som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="c42aa-116">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="c42aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c42aa-117">-DefaultProfile</span></span>
<span data-ttu-id="c42aa-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c42aa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c42aa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c42aa-119">CommonParameters</span></span>
<span data-ttu-id="c42aa-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c42aa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c42aa-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c42aa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c42aa-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c42aa-122">INPUTS</span></span>

### <span data-ttu-id="c42aa-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c42aa-123">System.String</span></span>

## <span data-ttu-id="c42aa-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c42aa-124">OUTPUTS</span></span>

### <span data-ttu-id="c42aa-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c42aa-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="c42aa-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c42aa-126">NOTES</span></span>

## <span data-ttu-id="c42aa-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c42aa-127">RELATED LINKS</span></span>

[<span data-ttu-id="c42aa-128">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c42aa-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="c42aa-129">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c42aa-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="c42aa-130">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c42aa-130">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="c42aa-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c42aa-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


