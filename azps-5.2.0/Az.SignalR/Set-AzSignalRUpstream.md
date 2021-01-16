---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397091"
---
# <span data-ttu-id="783f9-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="783f9-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="783f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="783f9-102">SYNOPSIS</span></span>
<span data-ttu-id="783f9-103">Ange inställningar för en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="783f9-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="783f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="783f9-104">SYNTAX</span></span>

### <span data-ttu-id="783f9-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="783f9-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="783f9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="783f9-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="783f9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="783f9-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="783f9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="783f9-108">DESCRIPTION</span></span>
<span data-ttu-id="783f9-109">Ange inställningar för en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="783f9-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="783f9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="783f9-110">EXAMPLES</span></span>

### <span data-ttu-id="783f9-111">Ställ in två ordnade mallar</span><span class="sxs-lookup"><span data-stu-id="783f9-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="783f9-112">Följande JSON representerar den faktiska mallen för mallar.</span><span class="sxs-lookup"><span data-stu-id="783f9-112">The following JSON represents the actual templates set.</span></span> 

 `
{
    "hubPattern": "chat",
    "eventPattern": "broadcast",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections1.com"
},
{
    "hubPattern": "*",
    "eventPattern": "*",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections2.com"
}
`

### <span data-ttu-id="783f9-113">Rensa alla inställningar för uppströmning</span><span class="sxs-lookup"><span data-stu-id="783f9-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="783f9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="783f9-114">PARAMETERS</span></span>

### <span data-ttu-id="783f9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="783f9-115">-AsJob</span></span>
<span data-ttu-id="783f9-116">Kör cmdleten i bakgrunds jobb.</span><span class="sxs-lookup"><span data-stu-id="783f9-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="783f9-117">-Rensa</span><span class="sxs-lookup"><span data-stu-id="783f9-117">-Clear</span></span>
<span data-ttu-id="783f9-118">Rensa alla inställningar för direkt uppspelning.</span><span class="sxs-lookup"><span data-stu-id="783f9-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="783f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="783f9-119">-DefaultProfile</span></span>
<span data-ttu-id="783f9-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="783f9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="783f9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="783f9-121">-InputObject</span></span>
<span data-ttu-id="783f9-122">Objektet Signalerare.</span><span class="sxs-lookup"><span data-stu-id="783f9-122">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="783f9-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="783f9-123">-Name</span></span>
<span data-ttu-id="783f9-124">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="783f9-124">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="783f9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="783f9-125">-ResourceGroupName</span></span>
<span data-ttu-id="783f9-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="783f9-126">The resource group name.</span></span>
<span data-ttu-id="783f9-127">Standard alternativet används om det inte anges.</span><span class="sxs-lookup"><span data-stu-id="783f9-127">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="783f9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="783f9-128">-ResourceId</span></span>
<span data-ttu-id="783f9-129">Avsändnings tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="783f9-129">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="783f9-130">-Mall</span><span class="sxs-lookup"><span data-stu-id="783f9-130">-Template</span></span>
<span data-ttu-id="783f9-131">Mallfiler för inställningar för direkt uppspelning.</span><span class="sxs-lookup"><span data-stu-id="783f9-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="783f9-132">Nödvändig behörighet: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="783f9-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="783f9-133">Valfria tangenter: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="783f9-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="783f9-134">Exempel använda splatting syntax för att skicka parametern templates: @ {UrlTemplate = ' http://host-connections1.com ', HubPattern = ' chatt '; EventPattern = ' broadcast '}, @ {UrlTemplate = ' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="783f9-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="783f9-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="783f9-135">-Confirm</span></span>
<span data-ttu-id="783f9-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="783f9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="783f9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="783f9-137">-WhatIf</span></span>
<span data-ttu-id="783f9-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="783f9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="783f9-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="783f9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="783f9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="783f9-140">CommonParameters</span></span>
<span data-ttu-id="783f9-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="783f9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="783f9-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="783f9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="783f9-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="783f9-143">INPUTS</span></span>

### <span data-ttu-id="783f9-144">System. String</span><span class="sxs-lookup"><span data-stu-id="783f9-144">System.String</span></span>

## <span data-ttu-id="783f9-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="783f9-145">OUTPUTS</span></span>

### <span data-ttu-id="783f9-146">Microsoft. Azure. commands. signaler. Models. PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="783f9-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="783f9-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="783f9-147">NOTES</span></span>

## <span data-ttu-id="783f9-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="783f9-148">RELATED LINKS</span></span>

[<span data-ttu-id="783f9-149">Så här använder du splatting för att skicka parametrar till kommandon i PowerShell</span><span class="sxs-lookup"><span data-stu-id="783f9-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
