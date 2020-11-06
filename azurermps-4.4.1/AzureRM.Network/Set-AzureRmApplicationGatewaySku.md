---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: b1680d18e11851718ca6d9d49acf4dc9501e1aad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577620"
---
# <span data-ttu-id="53bcf-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="53bcf-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="53bcf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="53bcf-103">Ändrar SKU för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="53bcf-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53bcf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53bcf-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53bcf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53bcf-105">DESCRIPTION</span></span>
<span data-ttu-id="53bcf-106">Cmdleten **set-AzureRmApplicationGatewaySku** ändrar lagerhållnings enhet (SKU) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="53bcf-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="53bcf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53bcf-107">EXAMPLES</span></span>

### <span data-ttu-id="53bcf-108">Exempel 1: uppdatera Application Gateway SKU</span><span class="sxs-lookup"><span data-stu-id="53bcf-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="53bcf-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="53bcf-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="53bcf-110">Det andra kommandot uppdaterar SKU för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="53bcf-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="53bcf-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53bcf-111">PARAMETERS</span></span>

### <span data-ttu-id="53bcf-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53bcf-112">-ApplicationGateway</span></span>
<span data-ttu-id="53bcf-113">Anger det Application Gateway-objekt som den här cmdleten associerar SKU med.</span><span class="sxs-lookup"><span data-stu-id="53bcf-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="53bcf-114">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="53bcf-114">-Capacity</span></span>
<span data-ttu-id="53bcf-115">Anger antalet instanser för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="53bcf-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bcf-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="53bcf-116">-Name</span></span>
<span data-ttu-id="53bcf-117">Anger namnet på programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="53bcf-117">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="53bcf-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="53bcf-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53bcf-119">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="53bcf-119">Standard_Small</span></span>
- <span data-ttu-id="53bcf-120">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="53bcf-120">Standard_Medium</span></span>
- <span data-ttu-id="53bcf-121">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="53bcf-121">Standard_Large</span></span>
- <span data-ttu-id="53bcf-122">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="53bcf-122">WAF_Medium</span></span>
- <span data-ttu-id="53bcf-123">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="53bcf-123">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bcf-124">-Tier</span><span class="sxs-lookup"><span data-stu-id="53bcf-124">-Tier</span></span>
<span data-ttu-id="53bcf-125">Anger nivån för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="53bcf-125">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="53bcf-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="53bcf-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53bcf-127">Standar</span><span class="sxs-lookup"><span data-stu-id="53bcf-127">Standard</span></span>
- <span data-ttu-id="53bcf-128">WAF</span><span class="sxs-lookup"><span data-stu-id="53bcf-128">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bcf-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bcf-129">-DefaultProfile</span></span>
<span data-ttu-id="53bcf-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53bcf-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53bcf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bcf-131">CommonParameters</span></span>
<span data-ttu-id="53bcf-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53bcf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bcf-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53bcf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bcf-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53bcf-134">INPUTS</span></span>

### <span data-ttu-id="53bcf-135">System. String</span><span class="sxs-lookup"><span data-stu-id="53bcf-135">System.String</span></span>

## <span data-ttu-id="53bcf-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53bcf-136">OUTPUTS</span></span>

### <span data-ttu-id="53bcf-137">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53bcf-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="53bcf-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53bcf-138">NOTES</span></span>

## <span data-ttu-id="53bcf-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53bcf-139">RELATED LINKS</span></span>

[<span data-ttu-id="53bcf-140">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="53bcf-140">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="53bcf-141">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="53bcf-141">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


