---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 4c7f488e7a9ffca823128cccff18ba33b88dabfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579668"
---
# <span data-ttu-id="04add-101">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="04add-101">New-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="04add-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04add-102">SYNOPSIS</span></span>
<span data-ttu-id="04add-103">Skapa en Application Insights-API-Server för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="04add-103">Create an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04add-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04add-104">SYNTAX</span></span>

### <span data-ttu-id="04add-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="04add-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04add-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04add-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04add-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04add-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04add-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04add-108">DESCRIPTION</span></span>
<span data-ttu-id="04add-109">Skapa en Application Insights-API-nycklar för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="04add-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="04add-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04add-110">EXAMPLES</span></span>

### <span data-ttu-id="04add-111">Exempel 1 Skapa en ny API-Server för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="04add-111">Example 1 Create a new Api Key for an application insights resource</span></span>
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

<span data-ttu-id="04add-112">Skapa Application Insights API-beskrivning som "testapiKey" med behörigheter "ReadTelemetry", "WriteAnnotations" för resurs "test" i resurs gruppen "testGroup".</span><span class="sxs-lookup"><span data-stu-id="04add-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="04add-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04add-113">PARAMETERS</span></span>

### <span data-ttu-id="04add-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="04add-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="04add-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="04add-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="04add-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="04add-116">-Confirm</span></span>
<span data-ttu-id="04add-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04add-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04add-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04add-118">-DefaultProfile</span></span>
<span data-ttu-id="04add-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04add-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04add-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="04add-120">-Description</span></span>
<span data-ttu-id="04add-121">Beskrivning som hjälper dig att identifiera denna API-funktion.</span><span class="sxs-lookup"><span data-stu-id="04add-121">Description to help identify this API key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04add-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="04add-122">-Name</span></span>
<span data-ttu-id="04add-123">Komponent namn.</span><span class="sxs-lookup"><span data-stu-id="04add-123">Component Name.</span></span>

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

### <span data-ttu-id="04add-124">-Behörigheter</span><span class="sxs-lookup"><span data-stu-id="04add-124">-Permissions</span></span>
<span data-ttu-id="04add-125">Behörigheter som API-nycklar tillåter att appar gör.</span><span class="sxs-lookup"><span data-stu-id="04add-125">Permissions that API key allow apps to do.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04add-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04add-126">-ResourceGroupName</span></span>
<span data-ttu-id="04add-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="04add-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="04add-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04add-128">-ResourceId</span></span>
<span data-ttu-id="04add-129">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="04add-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="04add-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04add-130">-WhatIf</span></span>
<span data-ttu-id="04add-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="04add-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04add-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="04add-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04add-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04add-133">CommonParameters</span></span>
<span data-ttu-id="04add-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04add-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04add-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04add-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04add-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04add-136">INPUTS</span></span>

### <span data-ttu-id="04add-137">System. String</span><span class="sxs-lookup"><span data-stu-id="04add-137">System.String</span></span>
<span data-ttu-id="04add-138">System. string []</span><span class="sxs-lookup"><span data-stu-id="04add-138">System.String[]</span></span>

## <span data-ttu-id="04add-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04add-139">OUTPUTS</span></span>

### <span data-ttu-id="04add-140">Microsoft. Azure. commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="04add-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="04add-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04add-141">NOTES</span></span>

## <span data-ttu-id="04add-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04add-142">RELATED LINKS</span></span>

