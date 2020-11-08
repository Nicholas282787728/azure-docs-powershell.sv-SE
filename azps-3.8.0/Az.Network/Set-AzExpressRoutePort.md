---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: b5170ef175b93bc977ba047d4188d51de2858e63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089055"
---
# <span data-ttu-id="2d8e1-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2d8e1-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="2d8e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="2d8e1-103">Ändrar en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="2d8e1-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="2d8e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d8e1-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d8e1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d8e1-105">DESCRIPTION</span></span>
<span data-ttu-id="2d8e1-106">Cmdleten **set-AzExpressRoutePort** sparar den ändrade ExpressRoutePort till Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8e1-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="2d8e1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d8e1-107">EXAMPLES</span></span>

### <span data-ttu-id="2d8e1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2d8e1-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="2d8e1-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2d8e1-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="2d8e1-110">Ändrar administratörs tillståndet för en länk för en ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2d8e1-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="2d8e1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d8e1-111">PARAMETERS</span></span>

### <span data-ttu-id="2d8e1-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d8e1-112">-AsJob</span></span>
<span data-ttu-id="2d8e1-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2d8e1-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d8e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d8e1-114">-DefaultProfile</span></span>
<span data-ttu-id="2d8e1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8e1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d8e1-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2d8e1-116">-ExpressRoutePort</span></span>
<span data-ttu-id="2d8e1-117">ExpressRoutePort-objektet.</span><span class="sxs-lookup"><span data-stu-id="2d8e1-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="2d8e1-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2d8e1-118">-Confirm</span></span>
<span data-ttu-id="2d8e1-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2d8e1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d8e1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d8e1-120">-WhatIf</span></span>
<span data-ttu-id="2d8e1-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2d8e1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d8e1-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2d8e1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d8e1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d8e1-123">CommonParameters</span></span>
<span data-ttu-id="2d8e1-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d8e1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d8e1-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d8e1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d8e1-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d8e1-126">INPUTS</span></span>

### <span data-ttu-id="2d8e1-127">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2d8e1-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="2d8e1-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d8e1-128">OUTPUTS</span></span>

### <span data-ttu-id="2d8e1-129">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2d8e1-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="2d8e1-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d8e1-130">NOTES</span></span>

## <span data-ttu-id="2d8e1-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d8e1-131">RELATED LINKS</span></span>

[<span data-ttu-id="2d8e1-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2d8e1-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="2d8e1-133">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2d8e1-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="2d8e1-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2d8e1-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
