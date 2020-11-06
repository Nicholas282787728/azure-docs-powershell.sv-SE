---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: ccccfe4ba17fe9d5fc9f35f6604f5f7bb9263d14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582140"
---
# <span data-ttu-id="b003b-101">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="b003b-101">Remove-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="b003b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b003b-102">SYNOPSIS</span></span>
<span data-ttu-id="b003b-103">Ta bort en cotinuous-export konfiguration i en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="b003b-103">Remove a cotinuous export configuration in an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b003b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b003b-104">SYNTAX</span></span>

### <span data-ttu-id="b003b-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b003b-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b003b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b003b-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport
 [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b003b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b003b-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b003b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b003b-108">DESCRIPTION</span></span>
<span data-ttu-id="b003b-109">Ta bort en cotinuous-export konfiguration i en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="b003b-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="b003b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b003b-110">EXAMPLES</span></span>

### <span data-ttu-id="b003b-111">Exempel 1 ta bort en cotinuous-export konfiguration i resursen Application Insights</span><span class="sxs-lookup"><span data-stu-id="b003b-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="b003b-112">Ta bort Application Insights kontinuerligt Exportera konfiguration med export-ID "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" för resursen med namnet "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="b003b-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="b003b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b003b-113">PARAMETERS</span></span>

### <span data-ttu-id="b003b-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b003b-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="b003b-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="b003b-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b003b-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b003b-116">-Confirm</span></span>
<span data-ttu-id="b003b-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b003b-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b003b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b003b-118">-DefaultProfile</span></span>
<span data-ttu-id="b003b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b003b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b003b-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="b003b-120">-ExportId</span></span>
<span data-ttu-id="b003b-121">Application Insights kontinuerligt exportera-ID.</span><span class="sxs-lookup"><span data-stu-id="b003b-121">Application Insights Continuous Export ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b003b-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b003b-122">-Name</span></span>
<span data-ttu-id="b003b-123">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="b003b-123">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b003b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b003b-124">-PassThru</span></span>
<span data-ttu-id="b003b-125">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="b003b-125">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="b003b-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b003b-126">This parameter is optional.</span></span> <span data-ttu-id="b003b-127">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="b003b-127">Default value is false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b003b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b003b-128">-ResourceGroupName</span></span>
<span data-ttu-id="b003b-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b003b-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b003b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b003b-130">-ResourceId</span></span>
<span data-ttu-id="b003b-131">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="b003b-131">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b003b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b003b-132">-WhatIf</span></span>
<span data-ttu-id="b003b-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b003b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b003b-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b003b-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b003b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b003b-135">CommonParameters</span></span>
<span data-ttu-id="b003b-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b003b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b003b-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b003b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b003b-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b003b-138">INPUTS</span></span>

### <span data-ttu-id="b003b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b003b-139">System.String</span></span>

## <span data-ttu-id="b003b-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b003b-140">OUTPUTS</span></span>

### <span data-ttu-id="b003b-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="b003b-141">System.Object</span></span>

## <span data-ttu-id="b003b-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b003b-142">NOTES</span></span>

## <span data-ttu-id="b003b-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b003b-143">RELATED LINKS</span></span>

