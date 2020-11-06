---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3504e4fbdb74fffc41e3f6424540dec71bb209e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576186"
---
# <span data-ttu-id="751c7-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="751c7-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="751c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="751c7-102">SYNOPSIS</span></span>
<span data-ttu-id="751c7-103">Tar bort en SSL-princip från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="751c7-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="751c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="751c7-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="751c7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="751c7-105">DESCRIPTION</span></span>
<span data-ttu-id="751c7-106">Remove-AzureRmApplicationGatewaySslPolicy cmdlet tar bort SSL-princip från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="751c7-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="751c7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="751c7-107">EXAMPLES</span></span>

### <span data-ttu-id="751c7-108">Exempel 1: ta bort en SSL-princip från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="751c7-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="751c7-109">Det här kommandot tar bort SSL-principen från den Programgateway som heter ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="751c7-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="751c7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="751c7-110">PARAMETERS</span></span>

### <span data-ttu-id="751c7-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="751c7-111">-ApplicationGateway</span></span>
<span data-ttu-id="751c7-112">Anger den Programgateway som den här cmdleten tar bort SSL-principer från.</span><span class="sxs-lookup"><span data-stu-id="751c7-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="751c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="751c7-113">-DefaultProfile</span></span>
<span data-ttu-id="751c7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="751c7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="751c7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="751c7-115">-Force</span></span>
<span data-ttu-id="751c7-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="751c7-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="751c7-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="751c7-117">-Confirm</span></span>
<span data-ttu-id="751c7-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="751c7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="751c7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="751c7-119">-WhatIf</span></span>
<span data-ttu-id="751c7-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="751c7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="751c7-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="751c7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="751c7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="751c7-122">CommonParameters</span></span>
<span data-ttu-id="751c7-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="751c7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="751c7-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="751c7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="751c7-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="751c7-125">INPUTS</span></span>

### <span data-ttu-id="751c7-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="751c7-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="751c7-127">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="751c7-127">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="751c7-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="751c7-128">OUTPUTS</span></span>

### <span data-ttu-id="751c7-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="751c7-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="751c7-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="751c7-130">NOTES</span></span>
<span data-ttu-id="751c7-131">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="751c7-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="751c7-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="751c7-132">RELATED LINKS</span></span>

[<span data-ttu-id="751c7-133">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="751c7-133">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="751c7-134">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="751c7-134">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="751c7-135">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="751c7-135">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

