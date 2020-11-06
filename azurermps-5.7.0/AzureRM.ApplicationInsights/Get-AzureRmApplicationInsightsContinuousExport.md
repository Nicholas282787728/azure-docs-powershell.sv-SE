---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 5e3b2feff3b59df30960856718911a3aeb699c37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579675"
---
# <span data-ttu-id="27634-101">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="27634-101">Get-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="27634-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27634-102">SYNOPSIS</span></span>
<span data-ttu-id="27634-103">Hämta Application Insights kontinuerligt Exportera konfiguration för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="27634-103">Get application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27634-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27634-104">SYNTAX</span></span>

### <span data-ttu-id="27634-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="27634-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27634-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27634-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27634-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27634-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27634-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27634-108">DESCRIPTION</span></span>
<span data-ttu-id="27634-109">Hämta Application Insights kontinuerligt Exportera konfiguration för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="27634-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="27634-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27634-110">EXAMPLES</span></span>

### <span data-ttu-id="27634-111">Exempel 1 få kontinuerlig export för resurser med Application Insights</span><span class="sxs-lookup"><span data-stu-id="27634-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="27634-112">Hämta Application Insights kontinuerligt exportera konfigurationer för resursen "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="27634-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="27634-113">Exempel 2 få kontinuerlig export för resurser med Application Insights</span><span class="sxs-lookup"><span data-stu-id="27634-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

ExportId                         : ZJrfffySPdtG3ESn3iRxVIEFuNY=
StorageName                      : targetaccount
ContainerName                    : continuousexport
DocumentTypes                    : Request, Performance Counter
DestinationStorageSubscriptionId : {subid}
DestinationStorageLocationId     : eastus
DestinationStorageAccountId      : /subscriptions/{subid}/resourceGroups/targetstorage/providers/Microsoft.Storage/storageAccounts/targetaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="27634-114">Hämta Application Insights kontinuerligt Exportera konfiguration med export-ID "ZJrfffySPdtG3ESn3iRxVIEFuNY =" för resursen med namnet "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="27634-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="27634-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27634-115">PARAMETERS</span></span>

### <span data-ttu-id="27634-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="27634-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="27634-117">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="27634-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="27634-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27634-118">-DefaultProfile</span></span>
<span data-ttu-id="27634-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27634-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27634-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="27634-120">-ExportId</span></span>
<span data-ttu-id="27634-121">Application Insights kontinuerligt exportera-ID.</span><span class="sxs-lookup"><span data-stu-id="27634-121">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="27634-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="27634-122">-Name</span></span>
<span data-ttu-id="27634-123">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="27634-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="27634-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27634-124">-ResourceGroupName</span></span>
<span data-ttu-id="27634-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="27634-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="27634-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27634-126">-ResourceId</span></span>
<span data-ttu-id="27634-127">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="27634-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="27634-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27634-128">CommonParameters</span></span>
<span data-ttu-id="27634-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27634-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27634-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27634-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27634-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27634-131">INPUTS</span></span>

### <span data-ttu-id="27634-132">System. String</span><span class="sxs-lookup"><span data-stu-id="27634-132">System.String</span></span>

## <span data-ttu-id="27634-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27634-133">OUTPUTS</span></span>

### <span data-ttu-id="27634-134">Microsoft. Azure. commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="27634-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="27634-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27634-135">NOTES</span></span>

## <span data-ttu-id="27634-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27634-136">RELATED LINKS</span></span>

