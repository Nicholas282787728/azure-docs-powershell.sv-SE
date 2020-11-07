---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: d82a6801c9307bac5220df2e021eb1a8c4ba0bb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755803"
---
# <span data-ttu-id="f585c-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f585c-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="f585c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f585c-102">SYNOPSIS</span></span>
<span data-ttu-id="f585c-103">Hämtar regeln för anslutningsbegäran för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f585c-103">Gets the request routing rule of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f585c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f585c-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f585c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f585c-105">DESCRIPTION</span></span>
<span data-ttu-id="f585c-106">Cmdleten **Get-AzureRmApplicationGatewayRequestRoutingRule** hämtar regeln för anslutningsbegäran för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f585c-106">The **Get-AzureRmApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="f585c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f585c-107">EXAMPLES</span></span>

### <span data-ttu-id="f585c-108">Exempel 1: skaffa en specifik regel för en anslutningsbegäran</span><span class="sxs-lookup"><span data-stu-id="f585c-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzureRmApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="f585c-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f585c-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="f585c-110">Det andra kommandot hämtar regeln för anslutningsbegäran med namnet Rule01 från Application Gateway som lagras i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f585c-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="f585c-111">Exempel 2: få en lista över regler för routning för begäran</span><span class="sxs-lookup"><span data-stu-id="f585c-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="f585c-112">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f585c-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="f585c-113">Det andra kommandot får en lista med routningsregler för routning från Application Gateway som lagras i variabeln $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f585c-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="f585c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f585c-114">PARAMETERS</span></span>

### <span data-ttu-id="f585c-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f585c-115">-ApplicationGateway</span></span>
<span data-ttu-id="f585c-116">Anger det Application Gateway-objekt som innehåller routningsregler för begäran.</span><span class="sxs-lookup"><span data-stu-id="f585c-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="f585c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f585c-117">-Name</span></span>
<span data-ttu-id="f585c-118">Anger namnet på regeln för anslutningsbegäran som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="f585c-118">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="f585c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f585c-119">-DefaultProfile</span></span>
<span data-ttu-id="f585c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f585c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f585c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f585c-121">CommonParameters</span></span>
<span data-ttu-id="f585c-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f585c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f585c-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f585c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f585c-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f585c-124">INPUTS</span></span>

### <span data-ttu-id="f585c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f585c-125">System.String</span></span>

## <span data-ttu-id="f585c-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f585c-126">OUTPUTS</span></span>

### <span data-ttu-id="f585c-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f585c-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="f585c-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f585c-128">NOTES</span></span>

## <span data-ttu-id="f585c-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f585c-129">RELATED LINKS</span></span>

[<span data-ttu-id="f585c-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f585c-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f585c-131">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f585c-131">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f585c-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f585c-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f585c-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f585c-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


