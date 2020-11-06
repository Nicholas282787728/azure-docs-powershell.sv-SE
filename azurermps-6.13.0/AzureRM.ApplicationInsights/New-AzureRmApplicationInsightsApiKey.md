---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: c60caa54f11fb2466631cf956cdc374b72265443
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575370"
---
# <span data-ttu-id="eef33-101">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="eef33-101">New-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="eef33-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eef33-102">SYNOPSIS</span></span>
<span data-ttu-id="eef33-103">Skapa en Application Insights-API-Server för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="eef33-103">Create an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eef33-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eef33-104">SYNTAX</span></span>

### <span data-ttu-id="eef33-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="eef33-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eef33-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eef33-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eef33-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eef33-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eef33-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eef33-108">DESCRIPTION</span></span>
<span data-ttu-id="eef33-109">Skapa en Application Insights-API-nycklar för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="eef33-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="eef33-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eef33-110">EXAMPLES</span></span>

### <span data-ttu-id="eef33-111">Exempel 1 Skapa en ny API-Server för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="eef33-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="eef33-112">Skapa Application Insights API-beskrivning som "testapiKey" med behörigheter "ReadTelemetry", "WriteAnnotations" för resurs "test" i resurs gruppen "testGroup".</span><span class="sxs-lookup"><span data-stu-id="eef33-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="eef33-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eef33-113">PARAMETERS</span></span>

### <span data-ttu-id="eef33-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="eef33-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="eef33-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="eef33-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="eef33-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef33-116">-DefaultProfile</span></span>
<span data-ttu-id="eef33-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eef33-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eef33-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="eef33-118">-Description</span></span>
<span data-ttu-id="eef33-119">Beskrivning som hjälper dig att identifiera denna API-funktion.</span><span class="sxs-lookup"><span data-stu-id="eef33-119">Description to help identify this API key.</span></span>

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

### <span data-ttu-id="eef33-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="eef33-120">-Name</span></span>
<span data-ttu-id="eef33-121">Komponent namn.</span><span class="sxs-lookup"><span data-stu-id="eef33-121">Component Name.</span></span>

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

### <span data-ttu-id="eef33-122">-Behörigheter</span><span class="sxs-lookup"><span data-stu-id="eef33-122">-Permissions</span></span>
<span data-ttu-id="eef33-123">Behörigheter som API-nycklar tillåter att appar gör.</span><span class="sxs-lookup"><span data-stu-id="eef33-123">Permissions that API key allow apps to do.</span></span>

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

### <span data-ttu-id="eef33-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eef33-124">-ResourceGroupName</span></span>
<span data-ttu-id="eef33-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="eef33-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="eef33-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eef33-126">-ResourceId</span></span>
<span data-ttu-id="eef33-127">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="eef33-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="eef33-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eef33-128">-Confirm</span></span>
<span data-ttu-id="eef33-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eef33-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eef33-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eef33-130">-WhatIf</span></span>
<span data-ttu-id="eef33-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eef33-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eef33-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eef33-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eef33-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef33-133">CommonParameters</span></span>
<span data-ttu-id="eef33-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eef33-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef33-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eef33-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef33-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eef33-136">INPUTS</span></span>

### <span data-ttu-id="eef33-137">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="eef33-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="eef33-138">Parametrar: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eef33-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="eef33-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eef33-139">System.String</span></span>

## <span data-ttu-id="eef33-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eef33-140">OUTPUTS</span></span>

### <span data-ttu-id="eef33-141">Microsoft. Azure. commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="eef33-141">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="eef33-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eef33-142">NOTES</span></span>

## <span data-ttu-id="eef33-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eef33-143">RELATED LINKS</span></span>
