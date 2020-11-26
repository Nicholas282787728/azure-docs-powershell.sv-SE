---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 5bf9106ccfd780fcfcdb7c86b6b86cdee82aba43
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271808"
---
# <span data-ttu-id="ecb1b-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecb1b-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ecb1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecb1b-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb1b-103">Skapar en Autoskala-konfiguration för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ecb1b-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="ecb1b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecb1b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecb1b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecb1b-105">DESCRIPTION</span></span>
<span data-ttu-id="ecb1b-106">Cmdleten **New-AzApplicationGatewayAutoscaleConfiguration** skapar en konfiguration för automatisk skalning för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ecb1b-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="ecb1b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecb1b-107">EXAMPLES</span></span>

### <span data-ttu-id="ecb1b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ecb1b-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="ecb1b-109">Det första kommandot skapar en Autoskala-konfiguration med minsta kapacitet 3.</span><span class="sxs-lookup"><span data-stu-id="ecb1b-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="ecb1b-110">Det andra kommandot skapar en Programgateway med den autoskalningsinställning som du konfigurerar.</span><span class="sxs-lookup"><span data-stu-id="ecb1b-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="ecb1b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecb1b-111">PARAMETERS</span></span>

### <span data-ttu-id="ecb1b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb1b-112">-DefaultProfile</span></span>
<span data-ttu-id="ecb1b-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ecb1b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecb1b-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="ecb1b-114">-MaxCapacity</span></span>
<span data-ttu-id="ecb1b-115">Högst kapacitets enheter som alltid är tillgängliga [och debiterade] för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ecb1b-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="ecb1b-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="ecb1b-116">-MinCapacity</span></span>
<span data-ttu-id="ecb1b-117">Minsta kapacitets enheter som alltid är tillgängliga [och debiterade] för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ecb1b-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="ecb1b-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ecb1b-118">-Confirm</span></span>
<span data-ttu-id="ecb1b-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ecb1b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecb1b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecb1b-120">-WhatIf</span></span>
<span data-ttu-id="ecb1b-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ecb1b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecb1b-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ecb1b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecb1b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb1b-123">CommonParameters</span></span>
<span data-ttu-id="ecb1b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecb1b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb1b-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecb1b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb1b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecb1b-126">INPUTS</span></span>

### <span data-ttu-id="ecb1b-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="ecb1b-127">None</span></span>

## <span data-ttu-id="ecb1b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecb1b-128">OUTPUTS</span></span>

### <span data-ttu-id="ecb1b-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecb1b-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ecb1b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecb1b-130">NOTES</span></span>

## <span data-ttu-id="ecb1b-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecb1b-131">RELATED LINKS</span></span>

[<span data-ttu-id="ecb1b-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecb1b-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ecb1b-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecb1b-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ecb1b-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecb1b-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)