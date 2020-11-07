---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: f5e4dcd4f898ed16099bb0c2f80a3fc642fdd73a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756486"
---
# <span data-ttu-id="4fc1a-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4fc1a-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="4fc1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4fc1a-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc1a-103">Tar bort en adresspool från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4fc1a-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fc1a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4fc1a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fc1a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4fc1a-105">DESCRIPTION</span></span>
<span data-ttu-id="4fc1a-106">Cmdleten **Remove-AzureRmApplicationGatewayBackendAddressPool** tar bort en backend-adresspool från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4fc1a-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="4fc1a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4fc1a-107">EXAMPLES</span></span>

### <span data-ttu-id="4fc1a-108">Exempel 1: ta bort en adresspool från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="4fc1a-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="4fc1a-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen som heter ResourceGroup01 och sparar den i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="4fc1a-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="4fc1a-110">Det andra kommandot tar bort adresspoolen som heter BackEndPool02 från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4fc1a-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="4fc1a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4fc1a-111">PARAMETERS</span></span>

### <span data-ttu-id="4fc1a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fc1a-112">-ApplicationGateway</span></span>
<span data-ttu-id="4fc1a-113">Anger den Programgateway från vilken denna cmdlet tar bort en backend-adresspool.</span><span class="sxs-lookup"><span data-stu-id="4fc1a-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="4fc1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc1a-114">-DefaultProfile</span></span>
<span data-ttu-id="4fc1a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4fc1a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fc1a-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="4fc1a-116">-Name</span></span>
<span data-ttu-id="4fc1a-117">Anger namnet på backend-adresspoolen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="4fc1a-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4fc1a-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4fc1a-118">-Confirm</span></span>
<span data-ttu-id="4fc1a-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4fc1a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fc1a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fc1a-120">-WhatIf</span></span>
<span data-ttu-id="4fc1a-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4fc1a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fc1a-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4fc1a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fc1a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc1a-123">CommonParameters</span></span>
<span data-ttu-id="4fc1a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fc1a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc1a-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc1a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc1a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4fc1a-126">INPUTS</span></span>

### <span data-ttu-id="4fc1a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4fc1a-127">System.String</span></span>

## <span data-ttu-id="4fc1a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4fc1a-128">OUTPUTS</span></span>

### <span data-ttu-id="4fc1a-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4fc1a-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="4fc1a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4fc1a-130">NOTES</span></span>

## <span data-ttu-id="4fc1a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4fc1a-131">RELATED LINKS</span></span>

[<span data-ttu-id="4fc1a-132">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4fc1a-132">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4fc1a-133">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4fc1a-133">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4fc1a-134">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4fc1a-134">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4fc1a-135">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4fc1a-135">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


