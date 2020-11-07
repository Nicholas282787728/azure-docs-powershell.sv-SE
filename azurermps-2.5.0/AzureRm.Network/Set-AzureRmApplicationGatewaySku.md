---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysku
schema: 2.0.0
ms.openlocfilehash: ccefc75d28ee49f12dd1f72d03512e3850298986
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929669"
---
# <span data-ttu-id="4605e-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="4605e-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="4605e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4605e-102">SYNOPSIS</span></span>
<span data-ttu-id="4605e-103">Ändrar SKU för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4605e-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4605e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4605e-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4605e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4605e-105">DESCRIPTION</span></span>
<span data-ttu-id="4605e-106">Cmdleten **set-AzureRmApplicationGatewaySku** ändrar lagerhållnings enhet (SKU) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4605e-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="4605e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4605e-107">EXAMPLES</span></span>

### <span data-ttu-id="4605e-108">Exempel 1: uppdatera Application Gateway SKU</span><span class="sxs-lookup"><span data-stu-id="4605e-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="4605e-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="4605e-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="4605e-110">Det andra kommandot uppdaterar SKU för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="4605e-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="4605e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4605e-111">PARAMETERS</span></span>

### <span data-ttu-id="4605e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4605e-112">-ApplicationGateway</span></span>
<span data-ttu-id="4605e-113">Anger det Application Gateway-objekt som den här cmdleten associerar SKU med.</span><span class="sxs-lookup"><span data-stu-id="4605e-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="4605e-114">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="4605e-114">-Capacity</span></span>
<span data-ttu-id="4605e-115">Anger antalet instanser för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="4605e-115">Specifies the instance count of the application gateway.</span></span>

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

### <span data-ttu-id="4605e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4605e-116">-DefaultProfile</span></span>
<span data-ttu-id="4605e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4605e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4605e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4605e-118">-Name</span></span>
<span data-ttu-id="4605e-119">Anger namnet på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="4605e-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="4605e-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4605e-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4605e-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="4605e-121">Standard_Small</span></span>
- <span data-ttu-id="4605e-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="4605e-122">Standard_Medium</span></span>
- <span data-ttu-id="4605e-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="4605e-123">Standard_Large</span></span>
- <span data-ttu-id="4605e-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="4605e-124">WAF_Medium</span></span>
- <span data-ttu-id="4605e-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="4605e-125">WAF_Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4605e-126">-Tier</span><span class="sxs-lookup"><span data-stu-id="4605e-126">-Tier</span></span>
<span data-ttu-id="4605e-127">Anger nivån för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="4605e-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="4605e-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4605e-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4605e-129">Standar</span><span class="sxs-lookup"><span data-stu-id="4605e-129">Standard</span></span>
- <span data-ttu-id="4605e-130">WAF</span><span class="sxs-lookup"><span data-stu-id="4605e-130">WAF</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4605e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4605e-131">CommonParameters</span></span>
<span data-ttu-id="4605e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4605e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4605e-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4605e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4605e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4605e-134">INPUTS</span></span>

### <span data-ttu-id="4605e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4605e-135">System.String</span></span>

## <span data-ttu-id="4605e-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4605e-136">OUTPUTS</span></span>

### <span data-ttu-id="4605e-137">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4605e-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4605e-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4605e-138">NOTES</span></span>

## <span data-ttu-id="4605e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4605e-139">RELATED LINKS</span></span>

[<span data-ttu-id="4605e-140">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="4605e-140">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="4605e-141">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="4605e-141">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


