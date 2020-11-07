---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: e0ca615d856e7905127c488c17c039b23051cc0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922458"
---
# <span data-ttu-id="14e67-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="14e67-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="14e67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14e67-102">SYNOPSIS</span></span>
<span data-ttu-id="14e67-103">Lägger till en frontend-port till en programport.</span><span class="sxs-lookup"><span data-stu-id="14e67-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="14e67-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14e67-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14e67-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14e67-105">DESCRIPTION</span></span>
<span data-ttu-id="14e67-106">Cmdleten **Add-AzApplicationGatewayFrontendPort** lägger till en frontend-port till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="14e67-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="14e67-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14e67-107">EXAMPLES</span></span>

### <span data-ttu-id="14e67-108">Exempel 1: lägga till en front port i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="14e67-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $ AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="14e67-109">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="14e67-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="14e67-110">Det andra kommandot lägger till port 80 som front port för programgatewayen som lagras i $AppGw och namnger porten FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="14e67-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="14e67-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14e67-111">PARAMETERS</span></span>

### <span data-ttu-id="14e67-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14e67-112">-ApplicationGateway</span></span>
<span data-ttu-id="14e67-113">Anger den Programgateway till vilken denna cmdlet lägger till en front port.</span><span class="sxs-lookup"><span data-stu-id="14e67-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="14e67-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e67-114">-DefaultProfile</span></span>
<span data-ttu-id="14e67-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14e67-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14e67-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="14e67-116">-Name</span></span>
<span data-ttu-id="14e67-117">Anger namnet på front porten.</span><span class="sxs-lookup"><span data-stu-id="14e67-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="14e67-118">-Port</span><span class="sxs-lookup"><span data-stu-id="14e67-118">-Port</span></span>
<span data-ttu-id="14e67-119">Anger port numret.</span><span class="sxs-lookup"><span data-stu-id="14e67-119">Specifies the port number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e67-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e67-120">CommonParameters</span></span>
<span data-ttu-id="14e67-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14e67-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e67-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14e67-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e67-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14e67-123">INPUTS</span></span>

### <span data-ttu-id="14e67-124">System. String</span><span class="sxs-lookup"><span data-stu-id="14e67-124">System.String</span></span>

## <span data-ttu-id="14e67-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14e67-125">OUTPUTS</span></span>

### <span data-ttu-id="14e67-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14e67-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14e67-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14e67-127">NOTES</span></span>

## <span data-ttu-id="14e67-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14e67-128">RELATED LINKS</span></span>

[<span data-ttu-id="14e67-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="14e67-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="14e67-130">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="14e67-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="14e67-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="14e67-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="14e67-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="14e67-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


