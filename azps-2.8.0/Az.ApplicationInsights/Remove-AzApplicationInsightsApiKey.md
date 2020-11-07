---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: fdd51d73b121feddaf20bbbe48184cc7f565d458
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745623"
---
# <span data-ttu-id="b986c-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="b986c-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="b986c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b986c-102">SYNOPSIS</span></span>
<span data-ttu-id="b986c-103">Ta bort en API-Server för Application Insights för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="b986c-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="b986c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b986c-104">SYNTAX</span></span>

### <span data-ttu-id="b986c-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b986c-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b986c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b986c-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b986c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b986c-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b986c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b986c-108">DESCRIPTION</span></span>
<span data-ttu-id="b986c-109">Ta bort en API-Server för Application Insights för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="b986c-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="b986c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b986c-110">EXAMPLES</span></span>

### <span data-ttu-id="b986c-111">Exempel 1 ta bort en API-Server för Application Insights för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="b986c-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="b986c-112">Ta bort specifika Application Insights API-tangenten det ID är "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" för Resource "test" i resurs gruppen "testGroup".</span><span class="sxs-lookup"><span data-stu-id="b986c-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="b986c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b986c-113">PARAMETERS</span></span>

### <span data-ttu-id="b986c-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="b986c-114">-ApiKeyId</span></span>
<span data-ttu-id="b986c-115">Application Insights API-ID.</span><span class="sxs-lookup"><span data-stu-id="b986c-115">Application Insights API Key ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b986c-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b986c-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="b986c-117">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="b986c-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="b986c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b986c-118">-DefaultProfile</span></span>
<span data-ttu-id="b986c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b986c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b986c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b986c-120">-Name</span></span>
<span data-ttu-id="b986c-121">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="b986c-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="b986c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b986c-122">-PassThru</span></span>
<span data-ttu-id="b986c-123">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="b986c-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="b986c-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b986c-124">This parameter is optional.</span></span> <span data-ttu-id="b986c-125">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="b986c-125">Default value is false.</span></span>

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

### <span data-ttu-id="b986c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b986c-126">-ResourceGroupName</span></span>
<span data-ttu-id="b986c-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b986c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b986c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b986c-128">-ResourceId</span></span>
<span data-ttu-id="b986c-129">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="b986c-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="b986c-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b986c-130">-Confirm</span></span>
<span data-ttu-id="b986c-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b986c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b986c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b986c-132">-WhatIf</span></span>
<span data-ttu-id="b986c-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b986c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b986c-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b986c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b986c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b986c-135">CommonParameters</span></span>
<span data-ttu-id="b986c-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b986c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b986c-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b986c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b986c-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b986c-138">INPUTS</span></span>

### <span data-ttu-id="b986c-139">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b986c-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="b986c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b986c-140">System.String</span></span>

## <span data-ttu-id="b986c-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b986c-141">OUTPUTS</span></span>

### <span data-ttu-id="b986c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b986c-142">System.Boolean</span></span>

## <span data-ttu-id="b986c-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b986c-143">NOTES</span></span>

## <span data-ttu-id="b986c-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b986c-144">RELATED LINKS</span></span>
