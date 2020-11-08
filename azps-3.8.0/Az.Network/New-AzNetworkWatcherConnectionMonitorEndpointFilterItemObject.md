---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointfilteritemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
ms.openlocfilehash: c06052ee28d849c5d07a941366efd15cbfeefe25
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088756"
---
# <span data-ttu-id="abc1d-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span><span class="sxs-lookup"><span data-stu-id="abc1d-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span></span>

## <span data-ttu-id="abc1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abc1d-102">SYNOPSIS</span></span>
<span data-ttu-id="abc1d-103">Skapar ett objekt för slut punkts filter för anslutning.</span><span class="sxs-lookup"><span data-stu-id="abc1d-103">Creates a connection monitor endpoint filter item.</span></span>

## <span data-ttu-id="abc1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abc1d-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abc1d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abc1d-105">DESCRIPTION</span></span>
<span data-ttu-id="abc1d-106">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject cmdlet skapar ett slut punkts filter objekt.</span><span class="sxs-lookup"><span data-stu-id="abc1d-106">The New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject cmdlet creates endpoint filter item.</span></span>

## <span data-ttu-id="abc1d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abc1d-107">EXAMPLES</span></span>

### <span data-ttu-id="abc1d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="abc1d-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "10.0.0.1"
```

<span data-ttu-id="abc1d-109">Typ: AgentAddress: 10.0.0.1</span><span class="sxs-lookup"><span data-stu-id="abc1d-109">Type    : AgentAddress Address : 10.0.0.1</span></span>

## <span data-ttu-id="abc1d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abc1d-110">PARAMETERS</span></span>

### <span data-ttu-id="abc1d-111">-Adress</span><span class="sxs-lookup"><span data-stu-id="abc1d-111">-Address</span></span>
<span data-ttu-id="abc1d-112">Adressen för filter posten.</span><span class="sxs-lookup"><span data-stu-id="abc1d-112">The address of the filter item.</span></span>

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

### <span data-ttu-id="abc1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc1d-113">-DefaultProfile</span></span>
<span data-ttu-id="abc1d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="abc1d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abc1d-115">– Skriv</span><span class="sxs-lookup"><span data-stu-id="abc1d-115">-Type</span></span>
<span data-ttu-id="abc1d-116">Objekt typen som ingår i filtret.</span><span class="sxs-lookup"><span data-stu-id="abc1d-116">The type of item included in the filter.</span></span> <span data-ttu-id="abc1d-117">För närvarande stöds endast "AgentAddress".</span><span class="sxs-lookup"><span data-stu-id="abc1d-117">Currently only 'AgentAddress' is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abc1d-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="abc1d-118">-Confirm</span></span>
<span data-ttu-id="abc1d-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="abc1d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc1d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc1d-120">-WhatIf</span></span>
<span data-ttu-id="abc1d-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="abc1d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abc1d-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="abc1d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc1d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc1d-123">CommonParameters</span></span>
<span data-ttu-id="abc1d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abc1d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc1d-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abc1d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc1d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abc1d-126">INPUTS</span></span>

### <span data-ttu-id="abc1d-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="abc1d-127">None</span></span>

## <span data-ttu-id="abc1d-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abc1d-128">OUTPUTS</span></span>

### <span data-ttu-id="abc1d-129">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorEndpointFilterItem</span><span class="sxs-lookup"><span data-stu-id="abc1d-129">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorEndpointFilterItem</span></span>

## <span data-ttu-id="abc1d-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abc1d-130">NOTES</span></span>

## <span data-ttu-id="abc1d-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abc1d-131">RELATED LINKS</span></span>
