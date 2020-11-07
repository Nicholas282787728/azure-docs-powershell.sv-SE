---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 487a3cd096f1d27852f4472d478977ac0cbe2ccc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757551"
---
# <span data-ttu-id="3fa10-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3fa10-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="3fa10-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3fa10-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa10-103">Ändrar SKU för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3fa10-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fa10-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3fa10-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fa10-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3fa10-105">DESCRIPTION</span></span>
<span data-ttu-id="3fa10-106">Cmdleten **set-AzureRmApplicationGatewaySku** ändrar lagerhållnings enhet (SKU) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3fa10-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="3fa10-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3fa10-107">EXAMPLES</span></span>

### <span data-ttu-id="3fa10-108">Exempel 1: uppdatera Application Gateway SKU</span><span class="sxs-lookup"><span data-stu-id="3fa10-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="3fa10-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="3fa10-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3fa10-110">Det andra kommandot uppdaterar SKU för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3fa10-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="3fa10-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3fa10-111">PARAMETERS</span></span>

### <span data-ttu-id="3fa10-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3fa10-112">-ApplicationGateway</span></span>
<span data-ttu-id="3fa10-113">Anger det Application Gateway-objekt som den här cmdleten associerar SKU med.</span><span class="sxs-lookup"><span data-stu-id="3fa10-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="3fa10-114">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="3fa10-114">-Capacity</span></span>
<span data-ttu-id="3fa10-115">Anger antalet instanser för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3fa10-115">Specifies the instance count of the application gateway.</span></span>

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

### <span data-ttu-id="3fa10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa10-116">-DefaultProfile</span></span>
<span data-ttu-id="3fa10-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3fa10-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fa10-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="3fa10-118">-Name</span></span>
<span data-ttu-id="3fa10-119">Anger namnet på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3fa10-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="3fa10-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3fa10-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3fa10-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="3fa10-121">Standard_Small</span></span>
- <span data-ttu-id="3fa10-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="3fa10-122">Standard_Medium</span></span>
- <span data-ttu-id="3fa10-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="3fa10-123">Standard_Large</span></span>
- <span data-ttu-id="3fa10-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="3fa10-124">WAF_Medium</span></span>
- <span data-ttu-id="3fa10-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="3fa10-125">WAF_Large</span></span>

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

### <span data-ttu-id="3fa10-126">-Tier</span><span class="sxs-lookup"><span data-stu-id="3fa10-126">-Tier</span></span>
<span data-ttu-id="3fa10-127">Anger nivån för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3fa10-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="3fa10-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3fa10-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3fa10-129">Standar</span><span class="sxs-lookup"><span data-stu-id="3fa10-129">Standard</span></span>
- <span data-ttu-id="3fa10-130">WAF</span><span class="sxs-lookup"><span data-stu-id="3fa10-130">WAF</span></span>

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

### <span data-ttu-id="3fa10-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa10-131">CommonParameters</span></span>
<span data-ttu-id="3fa10-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fa10-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa10-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fa10-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa10-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3fa10-134">INPUTS</span></span>

### <span data-ttu-id="3fa10-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3fa10-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="3fa10-136">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3fa10-136">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="3fa10-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3fa10-137">OUTPUTS</span></span>

### <span data-ttu-id="3fa10-138">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3fa10-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3fa10-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3fa10-139">NOTES</span></span>

## <span data-ttu-id="3fa10-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3fa10-140">RELATED LINKS</span></span>

[<span data-ttu-id="3fa10-141">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3fa10-141">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="3fa10-142">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3fa10-142">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


