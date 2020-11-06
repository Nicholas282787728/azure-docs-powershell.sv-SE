---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: b9a26a1279b89609728837def1997ac5735ddaea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575366"
---
# <span data-ttu-id="7e9f5-101">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="7e9f5-101">Remove-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="7e9f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e9f5-102">SYNOPSIS</span></span>
<span data-ttu-id="7e9f5-103">Ta bort en cotinuous-export konfiguration i en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="7e9f5-103">Remove a cotinuous export configuration in an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e9f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e9f5-104">SYNTAX</span></span>

### <span data-ttu-id="7e9f5-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7e9f5-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e9f5-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e9f5-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport
 [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e9f5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e9f5-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e9f5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e9f5-108">DESCRIPTION</span></span>
<span data-ttu-id="7e9f5-109">Ta bort en cotinuous-export konfiguration i en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="7e9f5-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="7e9f5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e9f5-110">EXAMPLES</span></span>

### <span data-ttu-id="7e9f5-111">Exempel 1 ta bort en cotinuous-export konfiguration i resursen Application Insights</span><span class="sxs-lookup"><span data-stu-id="7e9f5-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="7e9f5-112">Ta bort Application Insights kontinuerligt Exportera konfiguration med export-ID "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" för resursen med namnet "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="7e9f5-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="7e9f5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e9f5-113">PARAMETERS</span></span>

### <span data-ttu-id="7e9f5-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7e9f5-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="7e9f5-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="7e9f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e9f5-116">-DefaultProfile</span></span>
<span data-ttu-id="7e9f5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e9f5-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="7e9f5-118">-ExportId</span></span>
<span data-ttu-id="7e9f5-119">Application Insights kontinuerligt exportera-ID.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="7e9f5-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e9f5-120">-Name</span></span>
<span data-ttu-id="7e9f5-121">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="7e9f5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e9f5-122">-PassThru</span></span>
<span data-ttu-id="7e9f5-123">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="7e9f5-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-124">This parameter is optional.</span></span> <span data-ttu-id="7e9f5-125">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-125">Default value is false.</span></span>

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

### <span data-ttu-id="7e9f5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e9f5-126">-ResourceGroupName</span></span>
<span data-ttu-id="7e9f5-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="7e9f5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e9f5-128">-ResourceId</span></span>
<span data-ttu-id="7e9f5-129">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="7e9f5-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7e9f5-130">-Confirm</span></span>
<span data-ttu-id="7e9f5-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e9f5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e9f5-132">-WhatIf</span></span>
<span data-ttu-id="7e9f5-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e9f5-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e9f5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e9f5-135">CommonParameters</span></span>
<span data-ttu-id="7e9f5-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e9f5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e9f5-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e9f5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e9f5-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e9f5-138">INPUTS</span></span>

### <span data-ttu-id="7e9f5-139">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7e9f5-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="7e9f5-140">Parametrar: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e9f5-140">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="7e9f5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7e9f5-141">System.String</span></span>

## <span data-ttu-id="7e9f5-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e9f5-142">OUTPUTS</span></span>

### <span data-ttu-id="7e9f5-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e9f5-143">System.Boolean</span></span>

## <span data-ttu-id="7e9f5-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e9f5-144">NOTES</span></span>

## <span data-ttu-id="7e9f5-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e9f5-145">RELATED LINKS</span></span>
