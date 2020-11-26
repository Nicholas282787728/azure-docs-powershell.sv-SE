---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: ea5de8ddd36d315381d4f60ee0fa1ce7dc49adc2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258576"
---
# <span data-ttu-id="97b24-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="97b24-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="97b24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97b24-102">SYNOPSIS</span></span>
<span data-ttu-id="97b24-103">Starta om en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="97b24-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="97b24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97b24-104">SYNTAX</span></span>

### <span data-ttu-id="97b24-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="97b24-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97b24-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97b24-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97b24-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97b24-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97b24-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97b24-108">DESCRIPTION</span></span>
<span data-ttu-id="97b24-109">Starta om en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="97b24-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="97b24-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97b24-110">EXAMPLES</span></span>

### <span data-ttu-id="97b24-111">Starta om en specifik signal tjänst</span><span class="sxs-lookup"><span data-stu-id="97b24-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="97b24-112">Standard resurs gruppen kan anges via \` set-AzDefault-ResourceGroupName myResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="97b24-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="97b24-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97b24-113">PARAMETERS</span></span>

### <span data-ttu-id="97b24-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97b24-114">-AsJob</span></span>
<span data-ttu-id="97b24-115">Kör cmdleten i bakgrunds jobb.</span><span class="sxs-lookup"><span data-stu-id="97b24-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="97b24-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b24-116">-DefaultProfile</span></span>
<span data-ttu-id="97b24-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97b24-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97b24-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97b24-118">-InputObject</span></span>
<span data-ttu-id="97b24-119">Objektet Signalerare.</span><span class="sxs-lookup"><span data-stu-id="97b24-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="97b24-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="97b24-120">-Name</span></span>
<span data-ttu-id="97b24-121">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="97b24-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="97b24-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97b24-122">-PassThru</span></span>
<span data-ttu-id="97b24-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="97b24-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="97b24-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b24-124">-ResourceGroupName</span></span>
<span data-ttu-id="97b24-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="97b24-125">The resource group name.</span></span>
<span data-ttu-id="97b24-126">Standard alternativet används om det inte anges.</span><span class="sxs-lookup"><span data-stu-id="97b24-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="97b24-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97b24-127">-ResourceId</span></span>
<span data-ttu-id="97b24-128">Avsändnings tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="97b24-128">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="97b24-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97b24-129">-Confirm</span></span>
<span data-ttu-id="97b24-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97b24-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97b24-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97b24-131">-WhatIf</span></span>
<span data-ttu-id="97b24-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97b24-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97b24-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97b24-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97b24-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b24-134">CommonParameters</span></span>
<span data-ttu-id="97b24-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b24-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b24-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97b24-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b24-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97b24-137">INPUTS</span></span>

### <span data-ttu-id="97b24-138">System. String</span><span class="sxs-lookup"><span data-stu-id="97b24-138">System.String</span></span>

### <span data-ttu-id="97b24-139">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="97b24-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="97b24-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97b24-140">OUTPUTS</span></span>

### <span data-ttu-id="97b24-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97b24-141">System.Boolean</span></span>

## <span data-ttu-id="97b24-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97b24-142">NOTES</span></span>

## <span data-ttu-id="97b24-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97b24-143">RELATED LINKS</span></span>