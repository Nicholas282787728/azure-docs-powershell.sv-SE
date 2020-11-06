---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsights.md
ms.openlocfilehash: 917c40d5ec4939e3b6c8b5dc31f68088d4380290
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574057"
---
# <span data-ttu-id="f091d-101">Get-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f091d-101">Get-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="f091d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f091d-102">SYNOPSIS</span></span>
<span data-ttu-id="f091d-103">Få Application Insights-resurser</span><span class="sxs-lookup"><span data-stu-id="f091d-103">Get application insights resources</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f091d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f091d-104">SYNTAX</span></span>

### <span data-ttu-id="f091d-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f091d-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f091d-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f091d-106">ComponentNameParameterSet</span></span>
```
Get-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f091d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f091d-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f091d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f091d-108">DESCRIPTION</span></span>
<span data-ttu-id="f091d-109">Få Application Insights-resurser i en resurs grupp eller specifik resurs</span><span class="sxs-lookup"><span data-stu-id="f091d-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="f091d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f091d-110">EXAMPLES</span></span>

### <span data-ttu-id="f091d-111">Exempel 1 få Application Insights-resursen</span><span class="sxs-lookup"><span data-stu-id="f091d-111">Example 1 Get application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test"

Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
```

<span data-ttu-id="f091d-112">Få Application Insights-resursen "test" i resoruce Group "testgroup"</span><span class="sxs-lookup"><span data-stu-id="f091d-112">Get application insights resource named "test" in resoruce group "testgroup"</span></span>

### <span data-ttu-id="f091d-113">Exempel 2 få Application Insights-resurs med information om pris plan</span><span class="sxs-lookup"><span data-stu-id="f091d-113">Example 2 Get application insights resource with pricing plan information</span></span>
```
PS C:\> Get-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -IncludePricingPlan

Cap                            : 330
ResetTime                      : 0
StopSendNotificationWhenHitCap : True
CapExpirationTime              :
IsCapped                       : False
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
PricingPlan        : Basic
```

<span data-ttu-id="f091d-114">Resursen för Application Insights och innehåller information om pris plan för resursen "test" i resoruce Group "testgroup"</span><span class="sxs-lookup"><span data-stu-id="f091d-114">Get application insights resource and include pricing plan information for resource named "test" in resoruce group "testgroup"</span></span>

## <span data-ttu-id="f091d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f091d-115">PARAMETERS</span></span>

### <span data-ttu-id="f091d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f091d-116">-DefaultProfile</span></span>
<span data-ttu-id="f091d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f091d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f091d-118">-Fullständig</span><span class="sxs-lookup"><span data-stu-id="f091d-118">-Full</span></span>
<span data-ttu-id="f091d-119">Om det här alternativet anges får du tillbaka prissättnings plan/daglig Kap och status för komponenten Application Insights.</span><span class="sxs-lookup"><span data-stu-id="f091d-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ComponentNameParameterSet, ResourceIdParameterSet
Aliases: IncludeDailyCap, IncludeDailyCapStatus, IncludePricingPlan

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f091d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f091d-120">-Name</span></span>
<span data-ttu-id="f091d-121">Resurs namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="f091d-121">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="f091d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f091d-122">-ResourceGroupName</span></span>
<span data-ttu-id="f091d-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f091d-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="f091d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f091d-124">-ResourceId</span></span>
<span data-ttu-id="f091d-125">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="f091d-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="f091d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f091d-126">CommonParameters</span></span>
<span data-ttu-id="f091d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f091d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f091d-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f091d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f091d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f091d-129">INPUTS</span></span>

### <span data-ttu-id="f091d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f091d-130">System.String</span></span>

## <span data-ttu-id="f091d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f091d-131">OUTPUTS</span></span>

### <span data-ttu-id="f091d-132">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f091d-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="f091d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f091d-133">NOTES</span></span>

## <span data-ttu-id="f091d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f091d-134">RELATED LINKS</span></span>
