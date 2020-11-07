---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: 19b89ad855aa6b611a7dc008ae0ddfcc06b75f59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917637"
---
# <span data-ttu-id="df5a7-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="df5a7-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="df5a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="df5a7-103">Ta bort en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="df5a7-103">Remove an application insights resource</span></span>

## <span data-ttu-id="df5a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df5a7-104">SYNTAX</span></span>

### <span data-ttu-id="df5a7-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="df5a7-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df5a7-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df5a7-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df5a7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df5a7-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df5a7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df5a7-108">DESCRIPTION</span></span>
<span data-ttu-id="df5a7-109">Ta bort en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="df5a7-109">Remove an application insights resource</span></span>

## <span data-ttu-id="df5a7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df5a7-110">EXAMPLES</span></span>

### <span data-ttu-id="df5a7-111">Exempel 1 ta bort en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="df5a7-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="df5a7-112">Ta bort en applciation Insights-resurs med namnet "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="df5a7-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="df5a7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df5a7-113">PARAMETERS</span></span>

### <span data-ttu-id="df5a7-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="df5a7-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="df5a7-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="df5a7-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df5a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df5a7-116">-DefaultProfile</span></span>
<span data-ttu-id="df5a7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df5a7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df5a7-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="df5a7-118">-Name</span></span>
<span data-ttu-id="df5a7-119">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="df5a7-119">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df5a7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df5a7-120">-PassThru</span></span>
<span data-ttu-id="df5a7-121">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="df5a7-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="df5a7-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="df5a7-122">This parameter is optional.</span></span> <span data-ttu-id="df5a7-123">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="df5a7-123">Default value is false.</span></span>

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

### <span data-ttu-id="df5a7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df5a7-124">-ResourceGroupName</span></span>
<span data-ttu-id="df5a7-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="df5a7-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df5a7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df5a7-126">-ResourceId</span></span>
<span data-ttu-id="df5a7-127">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="df5a7-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df5a7-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="df5a7-128">-Confirm</span></span>
<span data-ttu-id="df5a7-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="df5a7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df5a7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df5a7-130">-WhatIf</span></span>
<span data-ttu-id="df5a7-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="df5a7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df5a7-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="df5a7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df5a7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5a7-133">CommonParameters</span></span>
<span data-ttu-id="df5a7-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df5a7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5a7-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df5a7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5a7-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df5a7-136">INPUTS</span></span>

### <span data-ttu-id="df5a7-137">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="df5a7-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="df5a7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="df5a7-138">System.String</span></span>

## <span data-ttu-id="df5a7-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df5a7-139">OUTPUTS</span></span>

### <span data-ttu-id="df5a7-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df5a7-140">System.Boolean</span></span>

## <span data-ttu-id="df5a7-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df5a7-141">NOTES</span></span>

## <span data-ttu-id="df5a7-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df5a7-142">RELATED LINKS</span></span>
