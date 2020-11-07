---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 25602712a792a1de7b79ce00baf5074ebb8177a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747957"
---
# <span data-ttu-id="4d496-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d496-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="4d496-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d496-102">SYNOPSIS</span></span>
<span data-ttu-id="4d496-103">Tar bort autoskalans konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4d496-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="4d496-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d496-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d496-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d496-105">DESCRIPTION</span></span>
<span data-ttu-id="4d496-106">Cmdleten **Remove-AzApplicationGatewayAutoscaleConfiguration** tar bort autoskalans konfiguration från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4d496-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="4d496-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d496-107">EXAMPLES</span></span>

### <span data-ttu-id="4d496-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4d496-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="4d496-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="4d496-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="4d496-110">Det andra kommandot tar bort autoskalans konfiguration från applicationg Gateway.</span><span class="sxs-lookup"><span data-stu-id="4d496-110">The second command removes the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="4d496-111">Det tredje kommandot uppdaterar programgatewayen på Azure.</span><span class="sxs-lookup"><span data-stu-id="4d496-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="4d496-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d496-112">PARAMETERS</span></span>

### <span data-ttu-id="4d496-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d496-113">-ApplicationGateway</span></span>
<span data-ttu-id="4d496-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d496-114">The applicationGateway</span></span>

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

### <span data-ttu-id="4d496-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d496-115">-DefaultProfile</span></span>
<span data-ttu-id="4d496-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d496-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d496-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4d496-117">-Force</span></span>
<span data-ttu-id="4d496-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4d496-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4d496-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d496-119">-Confirm</span></span>
<span data-ttu-id="4d496-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d496-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d496-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d496-121">-WhatIf</span></span>
<span data-ttu-id="4d496-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d496-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d496-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d496-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d496-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d496-124">CommonParameters</span></span>
<span data-ttu-id="4d496-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d496-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d496-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d496-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d496-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d496-127">INPUTS</span></span>

### <span data-ttu-id="4d496-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d496-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4d496-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d496-129">OUTPUTS</span></span>

### <span data-ttu-id="4d496-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d496-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4d496-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d496-131">NOTES</span></span>

## <span data-ttu-id="4d496-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d496-132">RELATED LINKS</span></span>

[<span data-ttu-id="4d496-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d496-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="4d496-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d496-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="4d496-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d496-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)