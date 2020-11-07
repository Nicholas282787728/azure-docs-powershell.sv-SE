---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: d3ca233ba82d1ee485e93a898726087f5cc69415
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747954"
---
# <span data-ttu-id="6666b-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6666b-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="6666b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6666b-102">SYNOPSIS</span></span>
<span data-ttu-id="6666b-103">Tar bort en adresspool från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="6666b-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="6666b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6666b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6666b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6666b-105">DESCRIPTION</span></span>
<span data-ttu-id="6666b-106">Cmdleten **Remove-AzApplicationGatewayBackendAddressPool** tar bort en backend-adresspool från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6666b-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="6666b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6666b-107">EXAMPLES</span></span>

### <span data-ttu-id="6666b-108">Exempel 1: ta bort en adresspool från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="6666b-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="6666b-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen som heter ResourceGroup01 och sparar den i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="6666b-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="6666b-110">Det andra kommandot tar bort adresspoolen som heter BackEndPool02 från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6666b-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="6666b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6666b-111">PARAMETERS</span></span>

### <span data-ttu-id="6666b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6666b-112">-ApplicationGateway</span></span>
<span data-ttu-id="6666b-113">Anger den Programgateway från vilken denna cmdlet tar bort en backend-adresspool.</span><span class="sxs-lookup"><span data-stu-id="6666b-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="6666b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6666b-114">-DefaultProfile</span></span>
<span data-ttu-id="6666b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6666b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6666b-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="6666b-116">-Name</span></span>
<span data-ttu-id="6666b-117">Anger namnet på backend-adresspoolen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="6666b-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6666b-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6666b-118">-Confirm</span></span>
<span data-ttu-id="6666b-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6666b-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6666b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6666b-120">-WhatIf</span></span>
<span data-ttu-id="6666b-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6666b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6666b-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6666b-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6666b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6666b-123">CommonParameters</span></span>
<span data-ttu-id="6666b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6666b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6666b-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6666b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6666b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6666b-126">INPUTS</span></span>

### <span data-ttu-id="6666b-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6666b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6666b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6666b-128">OUTPUTS</span></span>

### <span data-ttu-id="6666b-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6666b-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="6666b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6666b-130">NOTES</span></span>

## <span data-ttu-id="6666b-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6666b-131">RELATED LINKS</span></span>

[<span data-ttu-id="6666b-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6666b-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6666b-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6666b-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6666b-134">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6666b-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6666b-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6666b-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


