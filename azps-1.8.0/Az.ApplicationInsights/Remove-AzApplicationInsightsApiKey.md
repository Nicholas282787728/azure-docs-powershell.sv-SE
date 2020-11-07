---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 2dde5a98f244be794eedb744623137b674a38548
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754887"
---
# <span data-ttu-id="629e8-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="629e8-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="629e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="629e8-102">SYNOPSIS</span></span>
<span data-ttu-id="629e8-103">Ta bort en API-Server för Application Insights för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="629e8-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="629e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="629e8-104">SYNTAX</span></span>

### <span data-ttu-id="629e8-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="629e8-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="629e8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="629e8-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="629e8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="629e8-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="629e8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="629e8-108">DESCRIPTION</span></span>
<span data-ttu-id="629e8-109">Ta bort en API-Server för Application Insights för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="629e8-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="629e8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="629e8-110">EXAMPLES</span></span>

### <span data-ttu-id="629e8-111">Exempel 1 ta bort en API-Server för Application Insights för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="629e8-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="629e8-112">Ta bort specifika Application Insights API-tangenten det ID är "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" för Resource "test" i resurs gruppen "testGroup".</span><span class="sxs-lookup"><span data-stu-id="629e8-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="629e8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="629e8-113">PARAMETERS</span></span>

### <span data-ttu-id="629e8-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="629e8-114">-ApiKeyId</span></span>
<span data-ttu-id="629e8-115">Application Insights API-ID.</span><span class="sxs-lookup"><span data-stu-id="629e8-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="629e8-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="629e8-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="629e8-117">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="629e8-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="629e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="629e8-118">-DefaultProfile</span></span>
<span data-ttu-id="629e8-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="629e8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="629e8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="629e8-120">-Name</span></span>
<span data-ttu-id="629e8-121">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="629e8-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="629e8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="629e8-122">-PassThru</span></span>
<span data-ttu-id="629e8-123">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="629e8-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="629e8-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="629e8-124">This parameter is optional.</span></span> <span data-ttu-id="629e8-125">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="629e8-125">Default value is false.</span></span>

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

### <span data-ttu-id="629e8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="629e8-126">-ResourceGroupName</span></span>
<span data-ttu-id="629e8-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="629e8-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="629e8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="629e8-128">-ResourceId</span></span>
<span data-ttu-id="629e8-129">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="629e8-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="629e8-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="629e8-130">-Confirm</span></span>
<span data-ttu-id="629e8-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="629e8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="629e8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="629e8-132">-WhatIf</span></span>
<span data-ttu-id="629e8-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="629e8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="629e8-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="629e8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="629e8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="629e8-135">CommonParameters</span></span>
<span data-ttu-id="629e8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="629e8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="629e8-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="629e8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="629e8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="629e8-138">INPUTS</span></span>

### <span data-ttu-id="629e8-139">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="629e8-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="629e8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="629e8-140">System.String</span></span>

## <span data-ttu-id="629e8-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="629e8-141">OUTPUTS</span></span>

### <span data-ttu-id="629e8-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="629e8-142">System.Boolean</span></span>

## <span data-ttu-id="629e8-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="629e8-143">NOTES</span></span>

## <span data-ttu-id="629e8-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="629e8-144">RELATED LINKS</span></span>
