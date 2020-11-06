---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 705ebfc151ef4f6bcd5029026ce08ee1da5bd676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579679"
---
# <span data-ttu-id="8c409-101">Get-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="8c409-101">Get-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="8c409-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c409-102">SYNOPSIS</span></span>
<span data-ttu-id="8c409-103">Få Application Insights-API-nycklar för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="8c409-103">Get application insights api keys for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c409-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c409-104">SYNTAX</span></span>

### <span data-ttu-id="8c409-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8c409-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c409-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c409-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c409-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c409-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c409-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c409-108">DESCRIPTION</span></span>
<span data-ttu-id="8c409-109">Få Application Insights-API-nycklar för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="8c409-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="8c409-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c409-110">EXAMPLES</span></span>

### <span data-ttu-id="8c409-111">Exempel 1 Hämta API-nycklar för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="8c409-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="8c409-112">Hämta Application Insights API-nycklar för resurs "test" i resurs gruppen "testGroup".</span><span class="sxs-lookup"><span data-stu-id="8c409-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="8c409-113">Exempel 2 Hämta specifik API-Server för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="8c409-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="8c409-114">Få speciella program insikter API-tangenten det ID är "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" för Resource "test" i resurs gruppen "testGroup".</span><span class="sxs-lookup"><span data-stu-id="8c409-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="8c409-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c409-115">PARAMETERS</span></span>

### <span data-ttu-id="8c409-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="8c409-116">-ApiKeyId</span></span>
<span data-ttu-id="8c409-117">Application Insights API-ID.</span><span class="sxs-lookup"><span data-stu-id="8c409-117">Application Insights Api Key Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c409-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8c409-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8c409-119">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8c409-119">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="8c409-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c409-120">-DefaultProfile</span></span>
<span data-ttu-id="8c409-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c409-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c409-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="8c409-122">-Name</span></span>
<span data-ttu-id="8c409-123">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8c409-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="8c409-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c409-124">-ResourceGroupName</span></span>
<span data-ttu-id="8c409-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="8c409-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8c409-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c409-126">-ResourceId</span></span>
<span data-ttu-id="8c409-127">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8c409-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8c409-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c409-128">CommonParameters</span></span>
<span data-ttu-id="8c409-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c409-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c409-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c409-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c409-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c409-131">INPUTS</span></span>

### <span data-ttu-id="8c409-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8c409-132">System.String</span></span>

## <span data-ttu-id="8c409-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c409-133">OUTPUTS</span></span>

### <span data-ttu-id="8c409-134">Microsoft. Azure. commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="8c409-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="8c409-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c409-135">NOTES</span></span>

## <span data-ttu-id="8c409-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c409-136">RELATED LINKS</span></span>

