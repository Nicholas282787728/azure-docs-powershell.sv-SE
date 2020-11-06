---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f19a2e9f1531f6e009561a9d45ecae07d1bb0a3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582599"
---
# <span data-ttu-id="a4dcc-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4dcc-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="a4dcc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="a4dcc-103">Skapar en Autoskala-konfiguration för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="a4dcc-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4dcc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4dcc-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4dcc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4dcc-105">DESCRIPTION</span></span>
<span data-ttu-id="a4dcc-106">Cmdleten **New-AzureRmApplicationGatewayAutoscaleConfiguration** skapar en konfiguration för automatisk skalning för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a4dcc-106">The **New-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="a4dcc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4dcc-107">EXAMPLES</span></span>

### <span data-ttu-id="a4dcc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a4dcc-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="a4dcc-109">Det första kommandot skapar en Autoskala-konfiguration med minsta kapacitet 3.</span><span class="sxs-lookup"><span data-stu-id="a4dcc-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="a4dcc-110">Det andra kommandot skapar en Programgateway med den autoskalningsinställning som du konfigurerar.</span><span class="sxs-lookup"><span data-stu-id="a4dcc-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="a4dcc-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4dcc-111">PARAMETERS</span></span>

### <span data-ttu-id="a4dcc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4dcc-112">-DefaultProfile</span></span>
<span data-ttu-id="a4dcc-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4dcc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4dcc-114">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="a4dcc-114">-MinCapacity</span></span>
<span data-ttu-id="a4dcc-115">Minsta kapacitets enheter som alltid är tillgängliga [och debiterade] för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a4dcc-115">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="a4dcc-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4dcc-116">-Confirm</span></span>
<span data-ttu-id="a4dcc-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4dcc-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4dcc-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4dcc-118">-WhatIf</span></span>
<span data-ttu-id="a4dcc-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4dcc-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4dcc-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4dcc-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4dcc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4dcc-121">CommonParameters</span></span>
<span data-ttu-id="a4dcc-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4dcc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4dcc-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4dcc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4dcc-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4dcc-124">INPUTS</span></span>

### <span data-ttu-id="a4dcc-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="a4dcc-125">None</span></span>

## <span data-ttu-id="a4dcc-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4dcc-126">OUTPUTS</span></span>

### <span data-ttu-id="a4dcc-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4dcc-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="a4dcc-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4dcc-128">NOTES</span></span>

## <span data-ttu-id="a4dcc-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4dcc-129">RELATED LINKS</span></span>
