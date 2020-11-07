---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 0df6ae98692b7497448b0d3f15e88f1a18a87ae8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753978"
---
# <span data-ttu-id="5d175-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5d175-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="5d175-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d175-102">SYNOPSIS</span></span>
<span data-ttu-id="5d175-103">Lägger till ett anpassat fel i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="5d175-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="5d175-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d175-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d175-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d175-105">DESCRIPTION</span></span>
<span data-ttu-id="5d175-106">Cmdleten **Add-AzApplicationGatewayCustomError** lägger till ett anpassat fel till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="5d175-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="5d175-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d175-107">EXAMPLES</span></span>

### <span data-ttu-id="5d175-108">Exempel 1: lägger till ett anpassat fel till en Application Gateway-nivå</span><span class="sxs-lookup"><span data-stu-id="5d175-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="5d175-109">Det här kommandot lägger till ett anpassat fel med HTTP-statuskod 502 till Programgateway $appgw och returnerar den uppdaterade gatewayen.</span><span class="sxs-lookup"><span data-stu-id="5d175-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="5d175-110">Exempel 2: lägger till ett anpassat fel till lyssnar nivå för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5d175-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
PS C:\> $resourceGroup = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $listenerName = "listenerName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $rg
PS C:\> $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
PS C:\> $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="5d175-111">Det här kommandot lägger till ett anpassat fel med HTTP-statuskod 502 till Application Gateway $appgw på lyssnar nivån och returnerar den uppdaterade gatewayen.</span><span class="sxs-lookup"><span data-stu-id="5d175-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="5d175-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d175-112">PARAMETERS</span></span>

### <span data-ttu-id="5d175-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5d175-113">-ApplicationGateway</span></span>
<span data-ttu-id="5d175-114">Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5d175-114">The Application Gateway</span></span>

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

### <span data-ttu-id="5d175-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="5d175-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="5d175-116">Felsida URL för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5d175-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="5d175-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d175-117">-DefaultProfile</span></span>
<span data-ttu-id="5d175-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5d175-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d175-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="5d175-119">-StatusCode</span></span>
<span data-ttu-id="5d175-120">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5d175-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="5d175-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d175-121">CommonParameters</span></span>
<span data-ttu-id="5d175-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d175-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d175-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d175-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d175-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d175-124">INPUTS</span></span>

### <span data-ttu-id="5d175-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5d175-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5d175-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d175-126">OUTPUTS</span></span>

### <span data-ttu-id="5d175-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5d175-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="5d175-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d175-128">NOTES</span></span>

## <span data-ttu-id="5d175-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d175-129">RELATED LINKS</span></span>

[<span data-ttu-id="5d175-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5d175-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="5d175-131">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5d175-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="5d175-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5d175-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="5d175-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5d175-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)