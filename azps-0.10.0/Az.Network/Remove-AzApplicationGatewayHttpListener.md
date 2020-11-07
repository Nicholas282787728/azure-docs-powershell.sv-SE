---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: c3bc83f3f38c8a9b3c34e990e5729648a3677dd8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922060"
---
# <span data-ttu-id="268e2-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="268e2-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="268e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="268e2-102">SYNOPSIS</span></span>
<span data-ttu-id="268e2-103">Tar bort en HTTP-lyssnare från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="268e2-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="268e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="268e2-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="268e2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="268e2-105">DESCRIPTION</span></span>
<span data-ttu-id="268e2-106">Cmdleten **Remove-AzApplicationGatewayHttpListener** tar bort en http-lyssnare från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="268e2-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="268e2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="268e2-107">EXAMPLES</span></span>

### <span data-ttu-id="268e2-108">Exempel 1: ta bort en HTTP-lyssnare för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="268e2-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="268e2-109">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="268e2-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="268e2-110">Med det andra kommandot tas HTTP-lyssnaren bort med namnet Listener02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="268e2-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="268e2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="268e2-111">PARAMETERS</span></span>

### <span data-ttu-id="268e2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="268e2-112">-ApplicationGateway</span></span>
<span data-ttu-id="268e2-113">Anger den Programgateway från vilken du vill ta bort en HTTP-lyssnare.</span><span class="sxs-lookup"><span data-stu-id="268e2-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="268e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268e2-114">-DefaultProfile</span></span>
<span data-ttu-id="268e2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="268e2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="268e2-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="268e2-116">-Name</span></span>
<span data-ttu-id="268e2-117">Anger namnet på den HTTP-lyssnare som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="268e2-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="268e2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268e2-118">CommonParameters</span></span>
<span data-ttu-id="268e2-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="268e2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268e2-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="268e2-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268e2-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="268e2-121">INPUTS</span></span>

### <span data-ttu-id="268e2-122">System. String</span><span class="sxs-lookup"><span data-stu-id="268e2-122">System.String</span></span>

## <span data-ttu-id="268e2-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="268e2-123">OUTPUTS</span></span>

### <span data-ttu-id="268e2-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="268e2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="268e2-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="268e2-125">NOTES</span></span>

## <span data-ttu-id="268e2-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="268e2-126">RELATED LINKS</span></span>

[<span data-ttu-id="268e2-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="268e2-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="268e2-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="268e2-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="268e2-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="268e2-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="268e2-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="268e2-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


