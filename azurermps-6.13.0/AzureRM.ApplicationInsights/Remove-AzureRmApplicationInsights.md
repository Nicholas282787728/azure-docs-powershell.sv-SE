---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
ms.openlocfilehash: 72a5affb91cbd2c1dfbe78cc7ee86da799b6ae50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573027"
---
# <span data-ttu-id="08e1c-101">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="08e1c-101">Remove-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="08e1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="08e1c-103">Ta bort en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="08e1c-103">Remove an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08e1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08e1c-104">SYNTAX</span></span>

### <span data-ttu-id="08e1c-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="08e1c-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08e1c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08e1c-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08e1c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08e1c-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08e1c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08e1c-108">DESCRIPTION</span></span>
<span data-ttu-id="08e1c-109">Ta bort en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="08e1c-109">Remove an application insights resource</span></span>

## <span data-ttu-id="08e1c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08e1c-110">EXAMPLES</span></span>

### <span data-ttu-id="08e1c-111">Exempel 1 ta bort en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="08e1c-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="08e1c-112">Ta bort en applciation Insights-resurs med namnet "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="08e1c-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="08e1c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08e1c-113">PARAMETERS</span></span>

### <span data-ttu-id="08e1c-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="08e1c-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="08e1c-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="08e1c-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="08e1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e1c-116">-DefaultProfile</span></span>
<span data-ttu-id="08e1c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08e1c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08e1c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="08e1c-118">-Name</span></span>
<span data-ttu-id="08e1c-119">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="08e1c-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="08e1c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08e1c-120">-PassThru</span></span>
<span data-ttu-id="08e1c-121">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="08e1c-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="08e1c-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="08e1c-122">This parameter is optional.</span></span> <span data-ttu-id="08e1c-123">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="08e1c-123">Default value is false.</span></span>

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

### <span data-ttu-id="08e1c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e1c-124">-ResourceGroupName</span></span>
<span data-ttu-id="08e1c-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="08e1c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="08e1c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08e1c-126">-ResourceId</span></span>
<span data-ttu-id="08e1c-127">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="08e1c-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="08e1c-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="08e1c-128">-Confirm</span></span>
<span data-ttu-id="08e1c-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="08e1c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08e1c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08e1c-130">-WhatIf</span></span>
<span data-ttu-id="08e1c-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="08e1c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08e1c-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="08e1c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08e1c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e1c-133">CommonParameters</span></span>
<span data-ttu-id="08e1c-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e1c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e1c-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08e1c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e1c-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08e1c-136">INPUTS</span></span>

### <span data-ttu-id="08e1c-137">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="08e1c-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="08e1c-138">Parametrar: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="08e1c-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="08e1c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="08e1c-139">System.String</span></span>

## <span data-ttu-id="08e1c-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08e1c-140">OUTPUTS</span></span>

### <span data-ttu-id="08e1c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08e1c-141">System.Boolean</span></span>

## <span data-ttu-id="08e1c-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08e1c-142">NOTES</span></span>

## <span data-ttu-id="08e1c-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08e1c-143">RELATED LINKS</span></span>
