---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: b5170ef175b93bc977ba047d4188d51de2858e63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323226"
---
# <span data-ttu-id="30df3-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="30df3-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="30df3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30df3-102">SYNOPSIS</span></span>
<span data-ttu-id="30df3-103">Ändrar en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="30df3-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="30df3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30df3-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30df3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30df3-105">DESCRIPTION</span></span>
<span data-ttu-id="30df3-106">Cmdleten **set-AzExpressRoutePort** sparar den ändrade ExpressRoutePort till Azure.</span><span class="sxs-lookup"><span data-stu-id="30df3-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="30df3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30df3-107">EXAMPLES</span></span>

### <span data-ttu-id="30df3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="30df3-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="30df3-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="30df3-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="30df3-110">Ändrar administratörs tillståndet för en länk för en ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="30df3-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="30df3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30df3-111">PARAMETERS</span></span>

### <span data-ttu-id="30df3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30df3-112">-AsJob</span></span>
<span data-ttu-id="30df3-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="30df3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30df3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30df3-114">-DefaultProfile</span></span>
<span data-ttu-id="30df3-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30df3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30df3-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="30df3-116">-ExpressRoutePort</span></span>
<span data-ttu-id="30df3-117">ExpressRoutePort-objektet.</span><span class="sxs-lookup"><span data-stu-id="30df3-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="30df3-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30df3-118">-Confirm</span></span>
<span data-ttu-id="30df3-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30df3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30df3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30df3-120">-WhatIf</span></span>
<span data-ttu-id="30df3-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30df3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30df3-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30df3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30df3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30df3-123">CommonParameters</span></span>
<span data-ttu-id="30df3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30df3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30df3-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30df3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30df3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30df3-126">INPUTS</span></span>

### <span data-ttu-id="30df3-127">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="30df3-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="30df3-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30df3-128">OUTPUTS</span></span>

### <span data-ttu-id="30df3-129">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="30df3-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="30df3-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30df3-130">NOTES</span></span>

## <span data-ttu-id="30df3-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30df3-131">RELATED LINKS</span></span>

[<span data-ttu-id="30df3-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="30df3-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="30df3-133">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="30df3-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="30df3-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="30df3-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
