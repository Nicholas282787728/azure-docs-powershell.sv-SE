---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 6138d3d454a23cdbdbaa67d7ee668c5ffa752b4a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422944"
---
# <span data-ttu-id="6ef9d-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="6ef9d-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="6ef9d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ef9d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef9d-103">Ta bort en kontinuerlig export konfiguration i resursen Application Insights</span><span class="sxs-lookup"><span data-stu-id="6ef9d-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="6ef9d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ef9d-104">SYNTAX</span></span>

### <span data-ttu-id="6ef9d-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6ef9d-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ef9d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ef9d-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ef9d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ef9d-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ef9d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ef9d-108">DESCRIPTION</span></span>
<span data-ttu-id="6ef9d-109">Ta bort en kontinuerlig export konfiguration i resursen Application Insights</span><span class="sxs-lookup"><span data-stu-id="6ef9d-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="6ef9d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ef9d-110">EXAMPLES</span></span>

### <span data-ttu-id="6ef9d-111">Exempel 1 ta bort en kontinuerlig export konfiguration i resursen Application Insights</span><span class="sxs-lookup"><span data-stu-id="6ef9d-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="6ef9d-112">Ta bort Application Insights kontinuerligt Exportera konfiguration med export-ID "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" för resursen med namnet "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="6ef9d-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="6ef9d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ef9d-113">PARAMETERS</span></span>

### <span data-ttu-id="6ef9d-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6ef9d-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="6ef9d-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6ef9d-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="6ef9d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ef9d-116">-DefaultProfile</span></span>
<span data-ttu-id="6ef9d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6ef9d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ef9d-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="6ef9d-118">-ExportId</span></span>
<span data-ttu-id="6ef9d-119">Application Insights kontinuerligt exportera-ID.</span><span class="sxs-lookup"><span data-stu-id="6ef9d-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="6ef9d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6ef9d-120">-Name</span></span>
<span data-ttu-id="6ef9d-121">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6ef9d-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="6ef9d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ef9d-122">-PassThru</span></span>
<span data-ttu-id="6ef9d-123">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="6ef9d-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="6ef9d-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="6ef9d-124">This parameter is optional.</span></span> <span data-ttu-id="6ef9d-125">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="6ef9d-125">Default value is false.</span></span>

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

### <span data-ttu-id="6ef9d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ef9d-126">-ResourceGroupName</span></span>
<span data-ttu-id="6ef9d-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6ef9d-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="6ef9d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ef9d-128">-ResourceId</span></span>
<span data-ttu-id="6ef9d-129">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6ef9d-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="6ef9d-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6ef9d-130">-Confirm</span></span>
<span data-ttu-id="6ef9d-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6ef9d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ef9d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ef9d-132">-WhatIf</span></span>
<span data-ttu-id="6ef9d-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6ef9d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ef9d-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6ef9d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ef9d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef9d-135">CommonParameters</span></span>
<span data-ttu-id="6ef9d-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ef9d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef9d-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ef9d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef9d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ef9d-138">INPUTS</span></span>

### <span data-ttu-id="6ef9d-139">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6ef9d-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="6ef9d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6ef9d-140">System.String</span></span>

## <span data-ttu-id="6ef9d-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ef9d-141">OUTPUTS</span></span>

### <span data-ttu-id="6ef9d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ef9d-142">System.Boolean</span></span>

## <span data-ttu-id="6ef9d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ef9d-143">NOTES</span></span>

## <span data-ttu-id="6ef9d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ef9d-144">RELATED LINKS</span></span>
