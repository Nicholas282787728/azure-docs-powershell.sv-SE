---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 550fb398dbd636ba9c43c66d31b78384610cf42b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091873"
---
# <span data-ttu-id="2266f-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2266f-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="2266f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2266f-102">SYNOPSIS</span></span>
<span data-ttu-id="2266f-103">Skapa en ny Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="2266f-103">Create a new application insights resource</span></span>

## <span data-ttu-id="2266f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2266f-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2266f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2266f-105">DESCRIPTION</span></span>
<span data-ttu-id="2266f-106">Skapa en ny Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="2266f-106">Create a new application insights resource</span></span>

## <span data-ttu-id="2266f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2266f-107">EXAMPLES</span></span>

### <span data-ttu-id="2266f-108">Exempel 1 Skapa en ny Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="2266f-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
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

<span data-ttu-id="2266f-109">Lägg till en ny Application Insights-resurs med namnet "test" i resurs gruppen "testgroup" med typen "Java".</span><span class="sxs-lookup"><span data-stu-id="2266f-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="2266f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2266f-110">PARAMETERS</span></span>

### <span data-ttu-id="2266f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2266f-111">-DefaultProfile</span></span>
<span data-ttu-id="2266f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2266f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2266f-113">-Sort</span><span class="sxs-lookup"><span data-stu-id="2266f-113">-Kind</span></span>
<span data-ttu-id="2266f-114">Program typ.</span><span class="sxs-lookup"><span data-stu-id="2266f-114">Application kind.</span></span>

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

### <span data-ttu-id="2266f-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="2266f-115">-Location</span></span>
<span data-ttu-id="2266f-116">Resurs plats för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="2266f-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="2266f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2266f-117">-Name</span></span>
<span data-ttu-id="2266f-118">Resurs namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="2266f-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="2266f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2266f-119">-ResourceGroupName</span></span>
<span data-ttu-id="2266f-120">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2266f-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="2266f-121">-Tagg</span><span class="sxs-lookup"><span data-stu-id="2266f-121">-Tag</span></span>
<span data-ttu-id="2266f-122">Komponent-taggar.</span><span class="sxs-lookup"><span data-stu-id="2266f-122">Component Tags.</span></span>

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

### <span data-ttu-id="2266f-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2266f-123">-Confirm</span></span>
<span data-ttu-id="2266f-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2266f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2266f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2266f-125">-WhatIf</span></span>
<span data-ttu-id="2266f-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2266f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2266f-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2266f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2266f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2266f-128">CommonParameters</span></span>
<span data-ttu-id="2266f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2266f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2266f-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2266f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2266f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2266f-131">INPUTS</span></span>

### <span data-ttu-id="2266f-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="2266f-132">None</span></span>

## <span data-ttu-id="2266f-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2266f-133">OUTPUTS</span></span>

### <span data-ttu-id="2266f-134">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2266f-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="2266f-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2266f-135">NOTES</span></span>

## <span data-ttu-id="2266f-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2266f-136">RELATED LINKS</span></span>
