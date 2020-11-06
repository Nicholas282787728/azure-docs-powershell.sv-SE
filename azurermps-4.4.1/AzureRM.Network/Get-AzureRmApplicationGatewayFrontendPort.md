---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: f0a897dfcc68d2313326d974d1b5a172bd79db6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574606"
---
# <span data-ttu-id="178c3-101">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="178c3-101">Get-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="178c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="178c3-102">SYNOPSIS</span></span>
<span data-ttu-id="178c3-103">Hämtar front porten för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="178c3-103">Gets the front-end port of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="178c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="178c3-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="178c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="178c3-105">DESCRIPTION</span></span>
<span data-ttu-id="178c3-106">Cmdleten **Get-AzureRmApplicationGatewayFrontendPort** får fram front porten för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="178c3-106">The **Get-AzureRmApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="178c3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="178c3-107">EXAMPLES</span></span>

### <span data-ttu-id="178c3-108">Exempel 1: skaffa en viss front port</span><span class="sxs-lookup"><span data-stu-id="178c3-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzureRmApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="178c3-109">Det första kommandot får en Programgateway som heter ApplicationGateway01 från resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="178c3-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="178c3-110">Det andra kommandot får fram porten som heter FrontEndPort01 från $AppGw och lagrar den i $FrontEndPort-variabeln.</span><span class="sxs-lookup"><span data-stu-id="178c3-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="178c3-111">Exempel 2: Hämta en lista över front portar</span><span class="sxs-lookup"><span data-stu-id="178c3-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzureRmApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="178c3-112">Det första kommandot får en Programgateway som heter ApplicationGateway01 från resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="178c3-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="178c3-113">Det andra kommandot får en lista över front portarna från $AppGw och lagrar dem i $FrontEndPorts-variabeln.</span><span class="sxs-lookup"><span data-stu-id="178c3-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="178c3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="178c3-114">PARAMETERS</span></span>

### <span data-ttu-id="178c3-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="178c3-115">-ApplicationGateway</span></span>
<span data-ttu-id="178c3-116">Anger den Application Gateway-objekt som innehåller front porten.</span><span class="sxs-lookup"><span data-stu-id="178c3-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="178c3-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="178c3-117">-Name</span></span>
<span data-ttu-id="178c3-118">Anger namnet på front porten som ska visas.</span><span class="sxs-lookup"><span data-stu-id="178c3-118">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="178c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178c3-119">-DefaultProfile</span></span>
<span data-ttu-id="178c3-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="178c3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="178c3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178c3-121">CommonParameters</span></span>
<span data-ttu-id="178c3-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="178c3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178c3-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="178c3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178c3-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="178c3-124">INPUTS</span></span>

### <span data-ttu-id="178c3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="178c3-125">System.String</span></span>

## <span data-ttu-id="178c3-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="178c3-126">OUTPUTS</span></span>

### <span data-ttu-id="178c3-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="178c3-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="178c3-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="178c3-128">NOTES</span></span>

## <span data-ttu-id="178c3-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="178c3-129">RELATED LINKS</span></span>

[<span data-ttu-id="178c3-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="178c3-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="178c3-131">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="178c3-131">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="178c3-132">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="178c3-132">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="178c3-133">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="178c3-133">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


