---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
ms.openlocfilehash: 48922d3e0cbf8cf322d25657c76ee01e0ee238b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574053"
---
# <span data-ttu-id="6eaa1-101">New-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6eaa1-101">New-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="6eaa1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6eaa1-102">SYNOPSIS</span></span>
<span data-ttu-id="6eaa1-103">Skapa en ny Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="6eaa1-103">Create a new application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6eaa1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6eaa1-104">SYNTAX</span></span>

```
New-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Kind <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6eaa1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6eaa1-105">DESCRIPTION</span></span>
<span data-ttu-id="6eaa1-106">Skapa en ny Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="6eaa1-106">Create a new application insights resource</span></span>

## <span data-ttu-id="6eaa1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6eaa1-107">EXAMPLES</span></span>

### <span data-ttu-id="6eaa1-108">Exempel 1 Skapa en ny Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="6eaa1-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzureRmApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
```

<span data-ttu-id="6eaa1-109">Lägg till en ny Application Insights-resurs med namnet "test" i resurs gruppen "testgroup" med typen "Java".</span><span class="sxs-lookup"><span data-stu-id="6eaa1-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="6eaa1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6eaa1-110">PARAMETERS</span></span>

### <span data-ttu-id="6eaa1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eaa1-111">-DefaultProfile</span></span>
<span data-ttu-id="6eaa1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6eaa1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eaa1-113">-Sort</span><span class="sxs-lookup"><span data-stu-id="6eaa1-113">-Kind</span></span>
<span data-ttu-id="6eaa1-114">Program typ.</span><span class="sxs-lookup"><span data-stu-id="6eaa1-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eaa1-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="6eaa1-115">-Location</span></span>
<span data-ttu-id="6eaa1-116">Resurs plats för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6eaa1-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="6eaa1-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="6eaa1-117">-Name</span></span>
<span data-ttu-id="6eaa1-118">Resurs namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6eaa1-118">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eaa1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eaa1-119">-ResourceGroupName</span></span>
<span data-ttu-id="6eaa1-120">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6eaa1-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eaa1-121">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6eaa1-121">-Tag</span></span>
<span data-ttu-id="6eaa1-122">Komponent-taggar.</span><span class="sxs-lookup"><span data-stu-id="6eaa1-122">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eaa1-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6eaa1-123">-Confirm</span></span>
<span data-ttu-id="6eaa1-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6eaa1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eaa1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eaa1-125">-WhatIf</span></span>
<span data-ttu-id="6eaa1-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6eaa1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6eaa1-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6eaa1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eaa1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eaa1-128">CommonParameters</span></span>
<span data-ttu-id="6eaa1-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eaa1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eaa1-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eaa1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eaa1-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6eaa1-131">INPUTS</span></span>

### <span data-ttu-id="6eaa1-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="6eaa1-132">None</span></span>

## <span data-ttu-id="6eaa1-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6eaa1-133">OUTPUTS</span></span>

### <span data-ttu-id="6eaa1-134">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6eaa1-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="6eaa1-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6eaa1-135">NOTES</span></span>

## <span data-ttu-id="6eaa1-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6eaa1-136">RELATED LINKS</span></span>
