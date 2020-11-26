---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261815"
---
# <span data-ttu-id="ed622-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="ed622-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="ed622-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed622-102">SYNOPSIS</span></span>
<span data-ttu-id="ed622-103">Tar bort en identitet från en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ed622-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="ed622-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed622-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed622-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed622-105">DESCRIPTION</span></span>
<span data-ttu-id="ed622-106">Cmdleten **Remove-AzExpressRoutePortIdentity** tar bort identiteten från ett lokalt Azure ExpressRoutePort-objekt.</span><span class="sxs-lookup"><span data-stu-id="ed622-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="ed622-107">Använd **Remove-AzExpressRoutePort** för att ta bort den från ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ed622-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="ed622-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed622-108">EXAMPLES</span></span>

### <span data-ttu-id="ed622-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ed622-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="ed622-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed622-110">PARAMETERS</span></span>

### <span data-ttu-id="ed622-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed622-111">-DefaultProfile</span></span>
<span data-ttu-id="ed622-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed622-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed622-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ed622-113">-ExpressRoutePort</span></span>
<span data-ttu-id="ed622-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ed622-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed622-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed622-115">-Confirm</span></span>
<span data-ttu-id="ed622-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed622-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed622-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed622-117">-WhatIf</span></span>
<span data-ttu-id="ed622-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed622-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed622-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed622-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed622-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed622-120">CommonParameters</span></span>
<span data-ttu-id="ed622-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed622-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed622-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed622-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="ed622-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed622-123">INPUTS</span></span>

### <span data-ttu-id="ed622-124">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ed622-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="ed622-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed622-125">OUTPUTS</span></span>

### <span data-ttu-id="ed622-126">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ed622-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="ed622-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed622-127">NOTES</span></span>

## <span data-ttu-id="ed622-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed622-128">RELATED LINKS</span></span>
[<span data-ttu-id="ed622-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="ed622-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="ed622-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="ed622-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="ed622-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="ed622-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)