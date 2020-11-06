---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
ms.openlocfilehash: 46f73d2a58fe5f1109de6a15a5cb39e3b568a4b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580744"
---
# <span data-ttu-id="6e812-101">Set-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6e812-101">Set-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="6e812-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e812-102">SYNOPSIS</span></span>
<span data-ttu-id="6e812-103">Ändrar en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="6e812-103">Modifies an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e812-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e812-104">SYNTAX</span></span>

```
Set-AzureRmExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e812-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e812-105">DESCRIPTION</span></span>
<span data-ttu-id="6e812-106">Cmdleten **set-AzureRmExpressRoutePort** sparar den ändrade ExpressRoutePort till Azure.</span><span class="sxs-lookup"><span data-stu-id="6e812-106">The **Set-AzureRmExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="6e812-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e812-107">EXAMPLES</span></span>

### <span data-ttu-id="6e812-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6e812-108">Example 1</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="6e812-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6e812-109">Example 2</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -InputObject $erport
```

<span data-ttu-id="6e812-110">Ändrar administratörs tillståndet för en länk för en ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6e812-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="6e812-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e812-111">PARAMETERS</span></span>

### <span data-ttu-id="6e812-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e812-112">-AsJob</span></span>
<span data-ttu-id="6e812-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6e812-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e812-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e812-114">-DefaultProfile</span></span>
<span data-ttu-id="6e812-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6e812-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e812-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6e812-116">-ExpressRoutePort</span></span>
<span data-ttu-id="6e812-117">ExpressRoutePort-objektet.</span><span class="sxs-lookup"><span data-stu-id="6e812-117">The ExpressRoutePort object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e812-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6e812-118">-Confirm</span></span>
<span data-ttu-id="6e812-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6e812-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e812-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e812-120">-WhatIf</span></span>
<span data-ttu-id="6e812-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6e812-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e812-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6e812-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e812-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e812-123">CommonParameters</span></span>
<span data-ttu-id="6e812-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e812-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e812-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e812-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e812-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e812-126">INPUTS</span></span>

### <span data-ttu-id="6e812-127">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6e812-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="6e812-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e812-128">OUTPUTS</span></span>

### <span data-ttu-id="6e812-129">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6e812-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="6e812-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e812-130">NOTES</span></span>

## <span data-ttu-id="6e812-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e812-131">RELATED LINKS</span></span>
