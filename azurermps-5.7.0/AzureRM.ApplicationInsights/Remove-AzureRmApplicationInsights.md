---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
ms.openlocfilehash: a440dd37d26bf65f4deb8c7e4c4535f6460f76be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756822"
---
# <span data-ttu-id="fae7c-101">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fae7c-101">Remove-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="fae7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fae7c-102">SYNOPSIS</span></span>
<span data-ttu-id="fae7c-103">Ta bort en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="fae7c-103">Remove an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fae7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fae7c-104">SYNTAX</span></span>

### <span data-ttu-id="fae7c-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fae7c-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fae7c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fae7c-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fae7c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fae7c-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fae7c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fae7c-108">DESCRIPTION</span></span>
<span data-ttu-id="fae7c-109">Ta bort en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="fae7c-109">Remove an application insights resource</span></span>

## <span data-ttu-id="fae7c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fae7c-110">EXAMPLES</span></span>

### <span data-ttu-id="fae7c-111">Exempel 1 ta bort en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="fae7c-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="fae7c-112">Ta bort en applciation Insights-resurs med namnet "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="fae7c-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="fae7c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fae7c-113">PARAMETERS</span></span>

### <span data-ttu-id="fae7c-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="fae7c-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="fae7c-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="fae7c-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="fae7c-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fae7c-116">-Confirm</span></span>
<span data-ttu-id="fae7c-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fae7c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fae7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae7c-118">-DefaultProfile</span></span>
<span data-ttu-id="fae7c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fae7c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fae7c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="fae7c-120">-Name</span></span>
<span data-ttu-id="fae7c-121">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="fae7c-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="fae7c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fae7c-122">-PassThru</span></span>
<span data-ttu-id="fae7c-123">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="fae7c-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="fae7c-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fae7c-124">This parameter is optional.</span></span> <span data-ttu-id="fae7c-125">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="fae7c-125">Default value is false.</span></span>

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

### <span data-ttu-id="fae7c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae7c-126">-ResourceGroupName</span></span>
<span data-ttu-id="fae7c-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fae7c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="fae7c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fae7c-128">-ResourceId</span></span>
<span data-ttu-id="fae7c-129">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="fae7c-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="fae7c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fae7c-130">-WhatIf</span></span>
<span data-ttu-id="fae7c-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fae7c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fae7c-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fae7c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fae7c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae7c-133">CommonParameters</span></span>
<span data-ttu-id="fae7c-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fae7c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae7c-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fae7c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae7c-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fae7c-136">INPUTS</span></span>

### <span data-ttu-id="fae7c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fae7c-137">System.String</span></span>

## <span data-ttu-id="fae7c-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fae7c-138">OUTPUTS</span></span>

### <span data-ttu-id="fae7c-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="fae7c-139">System.Object</span></span>

## <span data-ttu-id="fae7c-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fae7c-140">NOTES</span></span>

## <span data-ttu-id="fae7c-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fae7c-141">RELATED LINKS</span></span>

