---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 2afb8ebfa1305e736a226f48022f4c56ded2d809
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091872"
---
# <span data-ttu-id="41818-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="41818-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="41818-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41818-102">SYNOPSIS</span></span>
<span data-ttu-id="41818-103">Skapa en Application Insights-API-Server för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="41818-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="41818-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41818-104">SYNTAX</span></span>

### <span data-ttu-id="41818-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="41818-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41818-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41818-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41818-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41818-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41818-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41818-108">DESCRIPTION</span></span>
<span data-ttu-id="41818-109">Skapa en Application Insights-API-nycklar för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="41818-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="41818-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41818-110">EXAMPLES</span></span>

### <span data-ttu-id="41818-111">Exempel 1 Skapa en ny API-Server för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="41818-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="41818-112">Skapa Application Insights API-beskrivning som "testapiKey" med behörigheter "ReadTelemetry", "WriteAnnotations" för resurs "test" i resurs gruppen "testGroup".</span><span class="sxs-lookup"><span data-stu-id="41818-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="41818-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41818-113">PARAMETERS</span></span>

### <span data-ttu-id="41818-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="41818-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="41818-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="41818-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="41818-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41818-116">-DefaultProfile</span></span>
<span data-ttu-id="41818-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="41818-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41818-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="41818-118">-Description</span></span>
<span data-ttu-id="41818-119">Beskrivning som hjälper dig att identifiera denna API-funktion.</span><span class="sxs-lookup"><span data-stu-id="41818-119">Description to help identify this API key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41818-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="41818-120">-Name</span></span>
<span data-ttu-id="41818-121">Komponent namn.</span><span class="sxs-lookup"><span data-stu-id="41818-121">Component Name.</span></span>

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

### <span data-ttu-id="41818-122">-Behörigheter</span><span class="sxs-lookup"><span data-stu-id="41818-122">-Permissions</span></span>
<span data-ttu-id="41818-123">Behörigheter som API-nycklar tillåter att appar gör.</span><span class="sxs-lookup"><span data-stu-id="41818-123">Permissions that API key allow apps to do.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41818-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41818-124">-ResourceGroupName</span></span>
<span data-ttu-id="41818-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="41818-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="41818-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41818-126">-ResourceId</span></span>
<span data-ttu-id="41818-127">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="41818-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="41818-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="41818-128">-Confirm</span></span>
<span data-ttu-id="41818-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="41818-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41818-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41818-130">-WhatIf</span></span>
<span data-ttu-id="41818-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="41818-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41818-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="41818-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41818-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41818-133">CommonParameters</span></span>
<span data-ttu-id="41818-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41818-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41818-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41818-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41818-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41818-136">INPUTS</span></span>

### <span data-ttu-id="41818-137">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="41818-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="41818-138">System. String</span><span class="sxs-lookup"><span data-stu-id="41818-138">System.String</span></span>

## <span data-ttu-id="41818-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41818-139">OUTPUTS</span></span>

### <span data-ttu-id="41818-140">Microsoft. Azure. commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="41818-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="41818-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41818-141">NOTES</span></span>

## <span data-ttu-id="41818-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41818-142">RELATED LINKS</span></span>