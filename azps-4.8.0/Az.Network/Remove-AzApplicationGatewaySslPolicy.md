---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: ac48531402f474db07ed811b6c2dac2f9a1f233f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261835"
---
# <span data-ttu-id="8227d-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8227d-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="8227d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8227d-102">SYNOPSIS</span></span>
<span data-ttu-id="8227d-103">Tar bort en SSL-princip från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8227d-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="8227d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8227d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8227d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8227d-105">DESCRIPTION</span></span>
<span data-ttu-id="8227d-106">Remove-AzApplicationGatewaySslPolicy cmdlet tar bort SSL-princip från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8227d-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="8227d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8227d-107">EXAMPLES</span></span>

### <span data-ttu-id="8227d-108">Exempel 1: ta bort en SSL-princip från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="8227d-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="8227d-109">Det här kommandot tar bort SSL-principen från den Programgateway som heter ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="8227d-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="8227d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8227d-110">PARAMETERS</span></span>

### <span data-ttu-id="8227d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8227d-111">-ApplicationGateway</span></span>
<span data-ttu-id="8227d-112">Anger den Programgateway som den här cmdleten tar bort SSL-principer från.</span><span class="sxs-lookup"><span data-stu-id="8227d-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="8227d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8227d-113">-DefaultProfile</span></span>
<span data-ttu-id="8227d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8227d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8227d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8227d-115">-Force</span></span>
<span data-ttu-id="8227d-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8227d-116">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8227d-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8227d-117">-Confirm</span></span>
<span data-ttu-id="8227d-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8227d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8227d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8227d-119">-WhatIf</span></span>
<span data-ttu-id="8227d-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8227d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8227d-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8227d-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8227d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8227d-122">CommonParameters</span></span>
<span data-ttu-id="8227d-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8227d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8227d-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8227d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8227d-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8227d-125">INPUTS</span></span>

### <span data-ttu-id="8227d-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8227d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8227d-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8227d-127">OUTPUTS</span></span>

### <span data-ttu-id="8227d-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8227d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8227d-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8227d-129">NOTES</span></span>
<span data-ttu-id="8227d-130">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="8227d-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8227d-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8227d-131">RELATED LINKS</span></span>

[<span data-ttu-id="8227d-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8227d-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="8227d-133">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8227d-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="8227d-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8227d-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

