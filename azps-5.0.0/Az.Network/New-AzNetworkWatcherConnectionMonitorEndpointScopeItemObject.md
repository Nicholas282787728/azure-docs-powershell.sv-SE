---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: c0ca9e257c0686aa0f4589ef4166fec150f41967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323291"
---
# <span data-ttu-id="20aa6-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="20aa6-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="20aa6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="20aa6-103">Skapar en objekt för slut punkts omfattning för anslutning.</span><span class="sxs-lookup"><span data-stu-id="20aa6-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="20aa6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20aa6-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20aa6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20aa6-105">DESCRIPTION</span></span>
<span data-ttu-id="20aa6-106">Den New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet skapar ett objekt för slut punkts omfattning.</span><span class="sxs-lookup"><span data-stu-id="20aa6-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="20aa6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20aa6-107">EXAMPLES</span></span>

### <span data-ttu-id="20aa6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="20aa6-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="20aa6-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20aa6-109">PARAMETERS</span></span>

### <span data-ttu-id="20aa6-110">-Adress</span><span class="sxs-lookup"><span data-stu-id="20aa6-110">-Address</span></span>
<span data-ttu-id="20aa6-111">Adress för scope-posten.</span><span class="sxs-lookup"><span data-stu-id="20aa6-111">The address of the scope item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20aa6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20aa6-112">-DefaultProfile</span></span>
<span data-ttu-id="20aa6-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20aa6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20aa6-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20aa6-114">-Confirm</span></span>
<span data-ttu-id="20aa6-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20aa6-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20aa6-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20aa6-116">-WhatIf</span></span>
<span data-ttu-id="20aa6-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20aa6-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20aa6-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20aa6-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20aa6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20aa6-119">CommonParameters</span></span>
<span data-ttu-id="20aa6-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20aa6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20aa6-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20aa6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20aa6-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20aa6-122">INPUTS</span></span>

### <span data-ttu-id="20aa6-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="20aa6-123">None</span></span>

## <span data-ttu-id="20aa6-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20aa6-124">OUTPUTS</span></span>

### <span data-ttu-id="20aa6-125">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="20aa6-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="20aa6-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20aa6-126">NOTES</span></span>

## <span data-ttu-id="20aa6-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20aa6-127">RELATED LINKS</span></span>
