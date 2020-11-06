---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 1ca390eb8c99ad991f5a15c6a3959d366ae5f983
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575197"
---
# <span data-ttu-id="a0739-101">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0739-101">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="a0739-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0739-102">SYNOPSIS</span></span>
<span data-ttu-id="a0739-103">Tar bort autoskalans konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a0739-103">Removes Autoscale Configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0739-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0739-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0739-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0739-105">DESCRIPTION</span></span>
<span data-ttu-id="a0739-106">Cmdleten **Remove-AzureRmApplicationGatewayAutoscaleConfiguration** tar bort autoskalans konfiguration från en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a0739-106">The **Remove-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="a0739-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0739-107">EXAMPLES</span></span>

### <span data-ttu-id="a0739-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a0739-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="a0739-109">Med det första kommandot hämtas programgatewayen och lagras i $gw variabel.</span><span class="sxs-lookup"><span data-stu-id="a0739-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="a0739-110">Det andra kommandot tar bort autoskalans konfiguration från applicationg Gateway.</span><span class="sxs-lookup"><span data-stu-id="a0739-110">The second command removes the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="a0739-111">Det tredje kommandot uppdaterar programgatewayen på Azure.</span><span class="sxs-lookup"><span data-stu-id="a0739-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="a0739-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0739-112">PARAMETERS</span></span>

### <span data-ttu-id="a0739-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0739-113">-ApplicationGateway</span></span>
<span data-ttu-id="a0739-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0739-114">The applicationGateway</span></span>

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

### <span data-ttu-id="a0739-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0739-115">-DefaultProfile</span></span>
<span data-ttu-id="a0739-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a0739-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0739-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a0739-117">-Force</span></span>
<span data-ttu-id="a0739-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a0739-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a0739-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a0739-119">-Confirm</span></span>
<span data-ttu-id="a0739-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a0739-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0739-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0739-121">-WhatIf</span></span>
<span data-ttu-id="a0739-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a0739-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0739-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a0739-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0739-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0739-124">CommonParameters</span></span>
<span data-ttu-id="a0739-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0739-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0739-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0739-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0739-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0739-127">INPUTS</span></span>

### <span data-ttu-id="a0739-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0739-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a0739-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0739-129">OUTPUTS</span></span>

### <span data-ttu-id="a0739-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0739-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a0739-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0739-131">NOTES</span></span>

## <span data-ttu-id="a0739-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0739-132">RELATED LINKS</span></span>
