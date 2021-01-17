---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: cf9e847454fc638afc3c25cc3b5d8f0e78ef2fb0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403072"
---
# <span data-ttu-id="0422c-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0422c-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="0422c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0422c-102">SYNOPSIS</span></span>
<span data-ttu-id="0422c-103">Uppdaterar autoskalans konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="0422c-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="0422c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0422c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0422c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0422c-105">DESCRIPTION</span></span>
<span data-ttu-id="0422c-106">Cmdleten **set-AzApplicationGatewayAutoscaleConfiguration** ändrar den befintliga autoskalans konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="0422c-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="0422c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0422c-107">EXAMPLES</span></span>

### <span data-ttu-id="0422c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0422c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="0422c-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="0422c-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="0422c-110">Det andra kommandot uppdaterar autoskalans konfiguration från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0422c-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="0422c-111">Det tredje kommandot uppdaterar programgatewayen på Azure.</span><span class="sxs-lookup"><span data-stu-id="0422c-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="0422c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0422c-112">PARAMETERS</span></span>

### <span data-ttu-id="0422c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0422c-113">-ApplicationGateway</span></span>
<span data-ttu-id="0422c-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0422c-114">The applicationGateway</span></span>

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

### <span data-ttu-id="0422c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0422c-115">-DefaultProfile</span></span>
<span data-ttu-id="0422c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0422c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0422c-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="0422c-117">-MaxCapacity</span></span>
<span data-ttu-id="0422c-118">Maximal kapacitet för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="0422c-118">Maximum capacity for application gateway.</span></span>

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

### <span data-ttu-id="0422c-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="0422c-119">-MinCapacity</span></span>
<span data-ttu-id="0422c-120">Minsta kapacitet för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="0422c-120">Minimum capacity for application gateway.</span></span>

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

### <span data-ttu-id="0422c-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0422c-121">-Confirm</span></span>
<span data-ttu-id="0422c-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0422c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0422c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0422c-123">-WhatIf</span></span>
<span data-ttu-id="0422c-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0422c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0422c-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0422c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0422c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0422c-126">CommonParameters</span></span>
<span data-ttu-id="0422c-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0422c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0422c-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0422c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0422c-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0422c-129">INPUTS</span></span>

### <span data-ttu-id="0422c-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0422c-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0422c-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0422c-131">OUTPUTS</span></span>

### <span data-ttu-id="0422c-132">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0422c-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0422c-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0422c-133">NOTES</span></span>

## <span data-ttu-id="0422c-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0422c-134">RELATED LINKS</span></span>

[<span data-ttu-id="0422c-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0422c-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="0422c-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0422c-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="0422c-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0422c-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
