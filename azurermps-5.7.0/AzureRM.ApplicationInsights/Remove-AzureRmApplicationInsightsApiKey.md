---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 7fbf269b43868724b015bd087536c49ccce71f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582151"
---
# <span data-ttu-id="c19d4-101">Remove-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c19d4-101">Remove-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="c19d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c19d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c19d4-103">Ta bort en API-Server för Application Insights för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="c19d4-103">Remove an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c19d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c19d4-104">SYNTAX</span></span>

### <span data-ttu-id="c19d4-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c19d4-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19d4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c19d4-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c19d4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c19d4-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c19d4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c19d4-108">DESCRIPTION</span></span>
<span data-ttu-id="c19d4-109">Ta bort en API-Server för Application Insights för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="c19d4-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="c19d4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c19d4-110">EXAMPLES</span></span>

### <span data-ttu-id="c19d4-111">Exempel 1 ta bort en API-Server för Application Insights för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="c19d4-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="c19d4-112">Ta bort specifika Application Insights API-tangenten det ID är "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" för Resource "test" i resurs gruppen "testGroup".</span><span class="sxs-lookup"><span data-stu-id="c19d4-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="c19d4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c19d4-113">PARAMETERS</span></span>

### <span data-ttu-id="c19d4-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="c19d4-114">-ApiKeyId</span></span>
<span data-ttu-id="c19d4-115">Application Insights API-ID.</span><span class="sxs-lookup"><span data-stu-id="c19d4-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="c19d4-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c19d4-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c19d4-117">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c19d4-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c19d4-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c19d4-118">-Confirm</span></span>
<span data-ttu-id="c19d4-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c19d4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c19d4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c19d4-120">-DefaultProfile</span></span>
<span data-ttu-id="c19d4-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c19d4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c19d4-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c19d4-122">-Name</span></span>
<span data-ttu-id="c19d4-123">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c19d4-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="c19d4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c19d4-124">-PassThru</span></span>
<span data-ttu-id="c19d4-125">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="c19d4-125">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="c19d4-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c19d4-126">This parameter is optional.</span></span> <span data-ttu-id="c19d4-127">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="c19d4-127">Default value is false.</span></span>

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

### <span data-ttu-id="c19d4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c19d4-128">-ResourceGroupName</span></span>
<span data-ttu-id="c19d4-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c19d4-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="c19d4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c19d4-130">-ResourceId</span></span>
<span data-ttu-id="c19d4-131">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c19d4-131">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c19d4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c19d4-132">-WhatIf</span></span>
<span data-ttu-id="c19d4-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c19d4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c19d4-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c19d4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c19d4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c19d4-135">CommonParameters</span></span>
<span data-ttu-id="c19d4-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c19d4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c19d4-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c19d4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c19d4-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c19d4-138">INPUTS</span></span>

### <span data-ttu-id="c19d4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c19d4-139">System.String</span></span>

## <span data-ttu-id="c19d4-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c19d4-140">OUTPUTS</span></span>

### <span data-ttu-id="c19d4-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="c19d4-141">System.Object</span></span>

## <span data-ttu-id="c19d4-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c19d4-142">NOTES</span></span>

## <span data-ttu-id="c19d4-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c19d4-143">RELATED LINKS</span></span>

