---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: ec1bba32027d3ec96aef61f3abec7d51cec5c35b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417752"
---
# <span data-ttu-id="d5439-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="d5439-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="d5439-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5439-102">SYNOPSIS</span></span>
<span data-ttu-id="d5439-103">Skapa mål objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="d5439-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="d5439-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5439-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5439-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5439-105">DESCRIPTION</span></span>
<span data-ttu-id="d5439-106">Med New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet skapas målobjektet för utdata för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="d5439-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="d5439-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5439-107">EXAMPLES</span></span>

### <span data-ttu-id="d5439-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d5439-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="d5439-109">Typ: "arbets yta" WorkspaceSettings: {"WorkspaceResourceId": "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="d5439-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="d5439-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5439-110">PARAMETERS</span></span>

### <span data-ttu-id="d5439-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5439-111">-DefaultProfile</span></span>
<span data-ttu-id="d5439-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5439-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5439-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="d5439-113">-OutputType</span></span>
<span data-ttu-id="d5439-114">Typ av mål för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="d5439-114">Connection monitor output destination type.</span></span> <span data-ttu-id="d5439-115">För närvarande \" stöds endast arbets ytan \" .</span><span class="sxs-lookup"><span data-stu-id="d5439-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="d5439-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="d5439-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="d5439-117">Resurs-ID för logganalys-arbetsytan.</span><span class="sxs-lookup"><span data-stu-id="d5439-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="d5439-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d5439-118">-Confirm</span></span>
<span data-ttu-id="d5439-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d5439-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5439-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5439-120">-WhatIf</span></span>
<span data-ttu-id="d5439-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d5439-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5439-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d5439-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5439-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5439-123">CommonParameters</span></span>
<span data-ttu-id="d5439-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5439-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5439-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5439-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5439-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5439-126">INPUTS</span></span>

### <span data-ttu-id="d5439-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="d5439-127">None</span></span>

## <span data-ttu-id="d5439-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5439-128">OUTPUTS</span></span>

### <span data-ttu-id="d5439-129">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="d5439-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="d5439-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5439-130">NOTES</span></span>

## <span data-ttu-id="d5439-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5439-131">RELATED LINKS</span></span>
