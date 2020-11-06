---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 81928913565c6e95f3768ccd5c05e8baa2c14b74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586187"
---
# <span data-ttu-id="748fe-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="748fe-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="748fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="748fe-102">SYNOPSIS</span></span>
<span data-ttu-id="748fe-103">Tar bort en SSL-princip från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="748fe-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="748fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="748fe-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="748fe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="748fe-105">DESCRIPTION</span></span>
<span data-ttu-id="748fe-106">Remove-AzureRmApplicationGatewaySslPolicy cmdlet tar bort SSL-princip från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="748fe-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="748fe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="748fe-107">EXAMPLES</span></span>

### <span data-ttu-id="748fe-108">Exempel 1: ta bort en SSL-princip från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="748fe-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="748fe-109">Det här kommandot tar bort SSL-principen från den Programgateway som heter ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="748fe-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="748fe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="748fe-110">PARAMETERS</span></span>

### <span data-ttu-id="748fe-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="748fe-111">-ApplicationGateway</span></span>
<span data-ttu-id="748fe-112">Anger den Programgateway som den här cmdleten tar bort SSL-principer från.</span><span class="sxs-lookup"><span data-stu-id="748fe-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="748fe-113">-Force</span><span class="sxs-lookup"><span data-stu-id="748fe-113">-Force</span></span>
<span data-ttu-id="748fe-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="748fe-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="748fe-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="748fe-115">-Confirm</span></span>
<span data-ttu-id="748fe-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="748fe-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="748fe-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="748fe-117">-WhatIf</span></span>
<span data-ttu-id="748fe-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="748fe-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="748fe-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="748fe-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="748fe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="748fe-120">-DefaultProfile</span></span>
<span data-ttu-id="748fe-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="748fe-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="748fe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="748fe-122">CommonParameters</span></span>
<span data-ttu-id="748fe-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="748fe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="748fe-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="748fe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="748fe-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="748fe-125">INPUTS</span></span>

### <span data-ttu-id="748fe-126">System. String</span><span class="sxs-lookup"><span data-stu-id="748fe-126">System.String</span></span>

## <span data-ttu-id="748fe-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="748fe-127">OUTPUTS</span></span>

### <span data-ttu-id="748fe-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="748fe-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="748fe-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="748fe-129">NOTES</span></span>
<span data-ttu-id="748fe-130">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="748fe-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="748fe-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="748fe-131">RELATED LINKS</span></span>

[<span data-ttu-id="748fe-132">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="748fe-132">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="748fe-133">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="748fe-133">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="748fe-134">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="748fe-134">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

