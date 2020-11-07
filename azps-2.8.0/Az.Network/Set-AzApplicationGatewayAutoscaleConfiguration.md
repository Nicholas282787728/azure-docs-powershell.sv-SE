---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: ad8795016fc10212a885267d23a61ddc7224c906
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918967"
---
# <span data-ttu-id="79a63-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="79a63-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="79a63-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79a63-102">SYNOPSIS</span></span>
<span data-ttu-id="79a63-103">Uppdaterar autoskalans konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="79a63-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="79a63-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79a63-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79a63-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79a63-105">DESCRIPTION</span></span>
<span data-ttu-id="79a63-106">Cmdleten **set-AzApplicationGatewayAutoscaleConfiguration** ändrar den befintliga autoskalans konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="79a63-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="79a63-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79a63-107">EXAMPLES</span></span>

### <span data-ttu-id="79a63-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="79a63-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="79a63-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="79a63-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="79a63-110">Det andra kommandot uppdaterar autoskalans konfiguration från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="79a63-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="79a63-111">Det tredje kommandot uppdaterar programgatewayen på Azure.</span><span class="sxs-lookup"><span data-stu-id="79a63-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="79a63-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79a63-112">PARAMETERS</span></span>

### <span data-ttu-id="79a63-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79a63-113">-ApplicationGateway</span></span>
<span data-ttu-id="79a63-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79a63-114">The applicationGateway</span></span>

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

### <span data-ttu-id="79a63-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a63-115">-DefaultProfile</span></span>
<span data-ttu-id="79a63-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79a63-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79a63-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="79a63-117">-MaxCapacity</span></span>
<span data-ttu-id="79a63-118">Maximal kapacitet för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="79a63-118">Maximum capacity for application gateway.</span></span>

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

### <span data-ttu-id="79a63-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="79a63-119">-MinCapacity</span></span>
<span data-ttu-id="79a63-120">Minsta kapacitet för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="79a63-120">Minimum capacity for application gateway.</span></span>

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

### <span data-ttu-id="79a63-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="79a63-121">-Confirm</span></span>
<span data-ttu-id="79a63-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="79a63-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79a63-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a63-123">-WhatIf</span></span>
<span data-ttu-id="79a63-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="79a63-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79a63-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="79a63-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79a63-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a63-126">CommonParameters</span></span>
<span data-ttu-id="79a63-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a63-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a63-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79a63-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a63-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79a63-129">INPUTS</span></span>

### <span data-ttu-id="79a63-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79a63-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79a63-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79a63-131">OUTPUTS</span></span>

### <span data-ttu-id="79a63-132">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79a63-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79a63-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79a63-133">NOTES</span></span>

## <span data-ttu-id="79a63-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79a63-134">RELATED LINKS</span></span>

[<span data-ttu-id="79a63-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="79a63-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="79a63-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="79a63-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="79a63-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="79a63-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
