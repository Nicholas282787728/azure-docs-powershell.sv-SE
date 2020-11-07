---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 7b82cf189d912d000c143b20cca76c4f2683b7d1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930146"
---
# <span data-ttu-id="4b0d3-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4b0d3-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="4b0d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b0d3-102">SYNOPSIS</span></span>
<span data-ttu-id="4b0d3-103">Tar bort en adresspool från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4b0d3-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b0d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b0d3-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b0d3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b0d3-105">DESCRIPTION</span></span>
<span data-ttu-id="4b0d3-106">Cmdleten **Remove-AzureRmApplicationGatewayBackendAddressPool** tar bort en backend-adresspool från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4b0d3-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="4b0d3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b0d3-107">EXAMPLES</span></span>

### <span data-ttu-id="4b0d3-108">Exempel 1: ta bort en adresspool från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="4b0d3-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="4b0d3-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen som heter ResourceGroup01 och sparar den i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="4b0d3-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="4b0d3-110">Det andra kommandot tar bort adresspoolen som heter BackEndPool02 från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4b0d3-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="4b0d3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b0d3-111">PARAMETERS</span></span>

### <span data-ttu-id="4b0d3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b0d3-112">-ApplicationGateway</span></span>
<span data-ttu-id="4b0d3-113">Anger den Programgateway från vilken denna cmdlet tar bort en backend-adresspool.</span><span class="sxs-lookup"><span data-stu-id="4b0d3-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="4b0d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b0d3-114">-DefaultProfile</span></span>
<span data-ttu-id="4b0d3-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b0d3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b0d3-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="4b0d3-116">-Name</span></span>
<span data-ttu-id="4b0d3-117">Anger namnet på backend-adresspoolen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="4b0d3-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4b0d3-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4b0d3-118">-Confirm</span></span>
<span data-ttu-id="4b0d3-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4b0d3-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0d3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b0d3-120">-WhatIf</span></span>
<span data-ttu-id="4b0d3-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4b0d3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b0d3-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4b0d3-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b0d3-123">CommonParameters</span></span>
<span data-ttu-id="4b0d3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b0d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b0d3-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b0d3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b0d3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b0d3-126">INPUTS</span></span>

### <span data-ttu-id="4b0d3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4b0d3-127">System.String</span></span>

## <span data-ttu-id="4b0d3-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b0d3-128">OUTPUTS</span></span>

### <span data-ttu-id="4b0d3-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4b0d3-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="4b0d3-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b0d3-130">NOTES</span></span>

## <span data-ttu-id="4b0d3-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b0d3-131">RELATED LINKS</span></span>

[<span data-ttu-id="4b0d3-132">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4b0d3-132">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4b0d3-133">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4b0d3-133">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4b0d3-134">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4b0d3-134">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4b0d3-135">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4b0d3-135">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


