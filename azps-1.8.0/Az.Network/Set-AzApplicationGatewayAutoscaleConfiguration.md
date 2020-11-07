---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 931d130ae40e6b7b0331c0aa3a50d28655dec8f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747795"
---
# <span data-ttu-id="24599-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="24599-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="24599-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24599-102">SYNOPSIS</span></span>
<span data-ttu-id="24599-103">Uppdaterar autoskalans konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="24599-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="24599-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24599-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24599-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24599-105">DESCRIPTION</span></span>
<span data-ttu-id="24599-106">Cmdleten **set-AzApplicationGatewayAutoscaleConfiguration** ändrar den befintliga autoskalans konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="24599-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="24599-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24599-107">EXAMPLES</span></span>

### <span data-ttu-id="24599-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="24599-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="24599-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="24599-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="24599-110">Det andra kommandot uppdaterar autoskalans konfiguration från applicationg Gateway.</span><span class="sxs-lookup"><span data-stu-id="24599-110">The second command updates the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="24599-111">Det tredje kommandot uppdaterar programgatewayen på Azure.</span><span class="sxs-lookup"><span data-stu-id="24599-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="24599-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24599-112">PARAMETERS</span></span>

### <span data-ttu-id="24599-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24599-113">-ApplicationGateway</span></span>
<span data-ttu-id="24599-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24599-114">The applicationGateway</span></span>

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

### <span data-ttu-id="24599-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24599-115">-DefaultProfile</span></span>
<span data-ttu-id="24599-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24599-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24599-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="24599-117">-MaxCapacity</span></span>
<span data-ttu-id="24599-118">Maximal capcity för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="24599-118">Maximum capcity for application gateway.</span></span>

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

### <span data-ttu-id="24599-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="24599-119">-MinCapacity</span></span>
<span data-ttu-id="24599-120">Minsta capcity för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="24599-120">Minimum capcity for application gateway.</span></span>

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

### <span data-ttu-id="24599-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24599-121">-Confirm</span></span>
<span data-ttu-id="24599-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24599-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24599-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24599-123">-WhatIf</span></span>
<span data-ttu-id="24599-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24599-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24599-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24599-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24599-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24599-126">CommonParameters</span></span>
<span data-ttu-id="24599-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24599-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24599-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24599-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24599-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24599-129">INPUTS</span></span>

### <span data-ttu-id="24599-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24599-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="24599-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24599-131">OUTPUTS</span></span>

### <span data-ttu-id="24599-132">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24599-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="24599-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24599-133">NOTES</span></span>

## <span data-ttu-id="24599-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24599-134">RELATED LINKS</span></span>

[<span data-ttu-id="24599-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="24599-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="24599-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="24599-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="24599-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="24599-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
