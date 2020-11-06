---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 2d7fa9dd9030f1e5878293276a248c2f6718efe5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580059"
---
# <span data-ttu-id="ff04d-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff04d-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ff04d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff04d-102">SYNOPSIS</span></span>
<span data-ttu-id="ff04d-103">Uppdaterar autoskalans konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ff04d-103">Updates Autoscale Configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff04d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff04d-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 -MinCapacity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff04d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff04d-105">DESCRIPTION</span></span>
<span data-ttu-id="ff04d-106">Cmdleten **set-AzureRmApplicationGatewayAutoscaleConfiguration** ändrar den befintliga autoskalans konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ff04d-106">The **Set-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="ff04d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff04d-107">EXAMPLES</span></span>

### <span data-ttu-id="ff04d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ff04d-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="ff04d-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="ff04d-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="ff04d-110">Det andra kommandot uppdaterar autoskalans konfiguration från applicationg Gateway.</span><span class="sxs-lookup"><span data-stu-id="ff04d-110">The second command updates the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="ff04d-111">Det tredje kommandot uppdaterar programgatewayen på Azure.</span><span class="sxs-lookup"><span data-stu-id="ff04d-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="ff04d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff04d-112">PARAMETERS</span></span>

### <span data-ttu-id="ff04d-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff04d-113">-ApplicationGateway</span></span>
<span data-ttu-id="ff04d-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff04d-114">The applicationGateway</span></span>

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

### <span data-ttu-id="ff04d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff04d-115">-DefaultProfile</span></span>
<span data-ttu-id="ff04d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff04d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff04d-117">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="ff04d-117">-MinCapacity</span></span>
<span data-ttu-id="ff04d-118">Minsta capcity för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ff04d-118">Minimum capcity for application gateway.</span></span>

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

### <span data-ttu-id="ff04d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff04d-119">-Confirm</span></span>
<span data-ttu-id="ff04d-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff04d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff04d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff04d-121">-WhatIf</span></span>
<span data-ttu-id="ff04d-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff04d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff04d-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff04d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff04d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff04d-124">CommonParameters</span></span>
<span data-ttu-id="ff04d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff04d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff04d-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff04d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff04d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff04d-127">INPUTS</span></span>

### <span data-ttu-id="ff04d-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff04d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ff04d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff04d-129">OUTPUTS</span></span>

### <span data-ttu-id="ff04d-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff04d-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ff04d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff04d-131">NOTES</span></span>

## <span data-ttu-id="ff04d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff04d-132">RELATED LINKS</span></span>
