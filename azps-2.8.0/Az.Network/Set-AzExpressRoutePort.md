---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: fe1182f165e347b312288d56604fddad6bad68da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917918"
---
# <span data-ttu-id="24d40-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="24d40-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="24d40-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24d40-102">SYNOPSIS</span></span>
<span data-ttu-id="24d40-103">Ändrar en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="24d40-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="24d40-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24d40-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24d40-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24d40-105">DESCRIPTION</span></span>
<span data-ttu-id="24d40-106">Cmdleten **set-AzExpressRoutePort** sparar den ändrade ExpressRoutePort till Azure.</span><span class="sxs-lookup"><span data-stu-id="24d40-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="24d40-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24d40-107">EXAMPLES</span></span>

### <span data-ttu-id="24d40-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="24d40-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="24d40-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="24d40-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="24d40-110">Ändrar administratörs tillståndet för en länk för en ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="24d40-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="24d40-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24d40-111">PARAMETERS</span></span>

### <span data-ttu-id="24d40-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24d40-112">-AsJob</span></span>
<span data-ttu-id="24d40-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="24d40-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24d40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d40-114">-DefaultProfile</span></span>
<span data-ttu-id="24d40-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24d40-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24d40-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="24d40-116">-ExpressRoutePort</span></span>
<span data-ttu-id="24d40-117">ExpressRoutePort-objektet.</span><span class="sxs-lookup"><span data-stu-id="24d40-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="24d40-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24d40-118">-Confirm</span></span>
<span data-ttu-id="24d40-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24d40-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24d40-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d40-120">-WhatIf</span></span>
<span data-ttu-id="24d40-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24d40-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24d40-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24d40-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24d40-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d40-123">CommonParameters</span></span>
<span data-ttu-id="24d40-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24d40-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d40-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d40-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d40-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24d40-126">INPUTS</span></span>

### <span data-ttu-id="24d40-127">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="24d40-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="24d40-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24d40-128">OUTPUTS</span></span>

### <span data-ttu-id="24d40-129">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="24d40-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="24d40-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24d40-130">NOTES</span></span>

## <span data-ttu-id="24d40-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24d40-131">RELATED LINKS</span></span>

[<span data-ttu-id="24d40-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="24d40-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="24d40-133">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="24d40-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="24d40-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="24d40-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
