---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: bfaf9773582b201de8f6066a30a55c0fd5f5b7ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102665"
---
# <span data-ttu-id="752ae-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="752ae-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="752ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="752ae-102">SYNOPSIS</span></span>
<span data-ttu-id="752ae-103">Ändrar SKU för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="752ae-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="752ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="752ae-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="752ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="752ae-105">DESCRIPTION</span></span>
<span data-ttu-id="752ae-106">Cmdleten **set-AzApplicationGatewaySku** ändrar lagerhållnings enhet (SKU) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="752ae-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="752ae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="752ae-107">EXAMPLES</span></span>

### <span data-ttu-id="752ae-108">Exempel 1: uppdatera Application Gateway SKU</span><span class="sxs-lookup"><span data-stu-id="752ae-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="752ae-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="752ae-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="752ae-110">Det andra kommandot uppdaterar SKU för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="752ae-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="752ae-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="752ae-111">PARAMETERS</span></span>

### <span data-ttu-id="752ae-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="752ae-112">-ApplicationGateway</span></span>
<span data-ttu-id="752ae-113">Anger det Application Gateway-objekt som den här cmdleten associerar SKU med.</span><span class="sxs-lookup"><span data-stu-id="752ae-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="752ae-114">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="752ae-114">-Capacity</span></span>
<span data-ttu-id="752ae-115">Anger antalet instanser för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="752ae-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="752ae-116">-DefaultProfile</span></span>
<span data-ttu-id="752ae-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="752ae-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="752ae-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="752ae-118">-Name</span></span>
<span data-ttu-id="752ae-119">Anger namnet på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="752ae-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="752ae-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="752ae-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="752ae-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="752ae-121">Standard_Small</span></span>
- <span data-ttu-id="752ae-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="752ae-122">Standard_Medium</span></span>
- <span data-ttu-id="752ae-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="752ae-123">Standard_Large</span></span>
- <span data-ttu-id="752ae-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="752ae-124">WAF_Medium</span></span>
- <span data-ttu-id="752ae-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="752ae-125">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752ae-126">-Tier</span><span class="sxs-lookup"><span data-stu-id="752ae-126">-Tier</span></span>
<span data-ttu-id="752ae-127">Anger nivån för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="752ae-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="752ae-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="752ae-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="752ae-129">Standar</span><span class="sxs-lookup"><span data-stu-id="752ae-129">Standard</span></span>
- <span data-ttu-id="752ae-130">WAF</span><span class="sxs-lookup"><span data-stu-id="752ae-130">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, WAF, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752ae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="752ae-131">CommonParameters</span></span>
<span data-ttu-id="752ae-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="752ae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="752ae-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="752ae-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="752ae-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="752ae-134">INPUTS</span></span>

### <span data-ttu-id="752ae-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="752ae-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="752ae-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="752ae-136">OUTPUTS</span></span>

### <span data-ttu-id="752ae-137">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="752ae-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="752ae-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="752ae-138">NOTES</span></span>

## <span data-ttu-id="752ae-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="752ae-139">RELATED LINKS</span></span>

[<span data-ttu-id="752ae-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="752ae-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="752ae-141">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="752ae-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


