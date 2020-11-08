---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 9f5c09e87e8d02276352cd10c2a7aba937822af2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088746"
---
# <span data-ttu-id="d25b1-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="d25b1-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="d25b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d25b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d25b1-103">Skapa mål objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="d25b1-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="d25b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d25b1-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d25b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d25b1-105">DESCRIPTION</span></span>
<span data-ttu-id="d25b1-106">Med New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet skapas målobjektet för utdata för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="d25b1-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="d25b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d25b1-107">EXAMPLES</span></span>

### <span data-ttu-id="d25b1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d25b1-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -ResourcWorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="d25b1-109">Typ: "arbets yta" WorkspaceSettings: {"WorkspaceResourceId": "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="d25b1-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="d25b1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d25b1-110">PARAMETERS</span></span>

### <span data-ttu-id="d25b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d25b1-111">-DefaultProfile</span></span>
<span data-ttu-id="d25b1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d25b1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d25b1-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="d25b1-113">-OutputType</span></span>
<span data-ttu-id="d25b1-114">Typ av mål för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="d25b1-114">Connection monitor output destination type.</span></span> <span data-ttu-id="d25b1-115">För närvarande \" stöds endast arbets ytan \" .</span><span class="sxs-lookup"><span data-stu-id="d25b1-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="d25b1-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="d25b1-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="d25b1-117">Resurs-ID för logganalys-arbetsytan.</span><span class="sxs-lookup"><span data-stu-id="d25b1-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="d25b1-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d25b1-118">-Confirm</span></span>
<span data-ttu-id="d25b1-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d25b1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d25b1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d25b1-120">-WhatIf</span></span>
<span data-ttu-id="d25b1-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d25b1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d25b1-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d25b1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d25b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25b1-123">CommonParameters</span></span>
<span data-ttu-id="d25b1-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d25b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25b1-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d25b1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25b1-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d25b1-126">INPUTS</span></span>

### <span data-ttu-id="d25b1-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="d25b1-127">None</span></span>

## <span data-ttu-id="d25b1-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d25b1-128">OUTPUTS</span></span>

### <span data-ttu-id="d25b1-129">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="d25b1-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="d25b1-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d25b1-130">NOTES</span></span>

## <span data-ttu-id="d25b1-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d25b1-131">RELATED LINKS</span></span>
