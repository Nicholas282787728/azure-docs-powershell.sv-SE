---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260385"
---
# <span data-ttu-id="99e70-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="99e70-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="99e70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99e70-102">SYNOPSIS</span></span>
<span data-ttu-id="99e70-103">uppdatera en befintlig Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="99e70-103">update an existing application insights resource</span></span>

## <span data-ttu-id="99e70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99e70-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99e70-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99e70-105">DESCRIPTION</span></span>
<span data-ttu-id="99e70-106">uppdatera en befintlig Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="99e70-106">update an existing application insights resource</span></span>

## <span data-ttu-id="99e70-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99e70-107">EXAMPLES</span></span>

### <span data-ttu-id="99e70-108">Exempel 1 komponent för uppdatering av Application Insights</span><span class="sxs-lookup"><span data-stu-id="99e70-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="99e70-109">uppdatera Application Insights-komponenten "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery båda till "Disabled"</span><span class="sxs-lookup"><span data-stu-id="99e70-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="99e70-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99e70-110">PARAMETERS</span></span>

### <span data-ttu-id="99e70-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e70-111">-DefaultProfile</span></span>
<span data-ttu-id="99e70-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="99e70-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99e70-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="99e70-113">-Name</span></span>
<span data-ttu-id="99e70-114">Resurs namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="99e70-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="99e70-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="99e70-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="99e70-116">Nätverks åtkomst typen för att få åtkomst till program insikter.</span><span class="sxs-lookup"><span data-stu-id="99e70-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="99e70-117">Värdet ska vara Enabled eller disabled</span><span class="sxs-lookup"><span data-stu-id="99e70-117">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e70-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="99e70-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="99e70-119">Typen nätverks åtkomst för åtkomst till Application Insights-fråga.</span><span class="sxs-lookup"><span data-stu-id="99e70-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="99e70-120">Värdet ska vara Enabled eller disabled</span><span class="sxs-lookup"><span data-stu-id="99e70-120">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e70-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99e70-121">-ResourceGroupName</span></span>
<span data-ttu-id="99e70-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="99e70-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="99e70-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="99e70-123">-RetentionInDays</span></span>
<span data-ttu-id="99e70-124">Bevarande i dagar, 90 som standard.</span><span class="sxs-lookup"><span data-stu-id="99e70-124">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e70-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="99e70-125">-Tag</span></span>
<span data-ttu-id="99e70-126">Komponent-taggar.</span><span class="sxs-lookup"><span data-stu-id="99e70-126">Component Tags.</span></span>

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

### <span data-ttu-id="99e70-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="99e70-127">-Confirm</span></span>
<span data-ttu-id="99e70-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="99e70-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99e70-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99e70-129">-WhatIf</span></span>
<span data-ttu-id="99e70-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="99e70-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99e70-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="99e70-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99e70-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e70-132">CommonParameters</span></span>
<span data-ttu-id="99e70-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99e70-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e70-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99e70-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e70-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99e70-135">INPUTS</span></span>

### <span data-ttu-id="99e70-136">System. String</span><span class="sxs-lookup"><span data-stu-id="99e70-136">System.String</span></span>

## <span data-ttu-id="99e70-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99e70-137">OUTPUTS</span></span>

### <span data-ttu-id="99e70-138">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="99e70-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="99e70-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99e70-139">NOTES</span></span>

## <span data-ttu-id="99e70-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99e70-140">RELATED LINKS</span></span>