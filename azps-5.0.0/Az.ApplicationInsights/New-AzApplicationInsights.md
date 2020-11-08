---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 3faa93ced76fee1a1023011e1570c3819f6c2013
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270152"
---
# <span data-ttu-id="9f358-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="9f358-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="9f358-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f358-102">SYNOPSIS</span></span>
<span data-ttu-id="9f358-103">Skapa en ny Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="9f358-103">Create a new application insights resource</span></span>

## <span data-ttu-id="9f358-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f358-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f358-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f358-105">DESCRIPTION</span></span>
<span data-ttu-id="9f358-106">Skapa en ny Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="9f358-106">Create a new application insights resource</span></span>

## <span data-ttu-id="9f358-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f358-107">EXAMPLES</span></span>

### <span data-ttu-id="9f358-108">Exempel 1 Skapa en ny Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="9f358-108">Example 1 Create a new application insights resource</span></span>
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
PublicNetworkAccessForIngestion : Enabled
PublicNetworkAccessForQuery     : Enabled
PrivateLinkScopedResources      :
```

<span data-ttu-id="9f358-109">Lägga till en ny Application Insights-resurs med namnet "test" i resurs gruppen "testgroup" med typen "Java"</span><span class="sxs-lookup"><span data-stu-id="9f358-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="9f358-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f358-110">PARAMETERS</span></span>

### <span data-ttu-id="9f358-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f358-111">-DefaultProfile</span></span>
<span data-ttu-id="9f358-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f358-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f358-113">-Sort</span><span class="sxs-lookup"><span data-stu-id="9f358-113">-Kind</span></span>
<span data-ttu-id="9f358-114">Program typ.</span><span class="sxs-lookup"><span data-stu-id="9f358-114">Application kind.</span></span>

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

### <span data-ttu-id="9f358-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="9f358-115">-Location</span></span>
<span data-ttu-id="9f358-116">Resurs plats för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9f358-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="9f358-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="9f358-117">-Name</span></span>
<span data-ttu-id="9f358-118">Resurs namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9f358-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="9f358-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="9f358-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="9f358-120">Nätverks åtkomst typen för att få åtkomst till program insikter.</span><span class="sxs-lookup"><span data-stu-id="9f358-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="9f358-121">Värdet ska vara Enabled eller disabled</span><span class="sxs-lookup"><span data-stu-id="9f358-121">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f358-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="9f358-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="9f358-123">Typen nätverks åtkomst för åtkomst till Application Insights-fråga.</span><span class="sxs-lookup"><span data-stu-id="9f358-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="9f358-124">Värdet ska vara Enabled eller disabled</span><span class="sxs-lookup"><span data-stu-id="9f358-124">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f358-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f358-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f358-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="9f358-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="9f358-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9f358-127">-RetentionInDays</span></span>
<span data-ttu-id="9f358-128">Bevarande i dagar, 90 som standard.</span><span class="sxs-lookup"><span data-stu-id="9f358-128">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f358-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9f358-129">-Tag</span></span>
<span data-ttu-id="9f358-130">Komponent-taggar.</span><span class="sxs-lookup"><span data-stu-id="9f358-130">Component Tags.</span></span>

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

### <span data-ttu-id="9f358-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9f358-131">-Confirm</span></span>
<span data-ttu-id="9f358-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9f358-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f358-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f358-133">-WhatIf</span></span>
<span data-ttu-id="9f358-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9f358-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f358-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9f358-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f358-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f358-136">CommonParameters</span></span>
<span data-ttu-id="9f358-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f358-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f358-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f358-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f358-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f358-139">INPUTS</span></span>

### <span data-ttu-id="9f358-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="9f358-140">None</span></span>

## <span data-ttu-id="9f358-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f358-141">OUTPUTS</span></span>

### <span data-ttu-id="9f358-142">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9f358-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="9f358-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f358-143">NOTES</span></span>

## <span data-ttu-id="9f358-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f358-144">RELATED LINKS</span></span>
