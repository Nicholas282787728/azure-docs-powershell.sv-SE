---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: d5711e6bca9b0579b456e4d2b0c5f915b4ad6fe0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091874"
---
# <span data-ttu-id="52a7a-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="52a7a-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="52a7a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52a7a-102">SYNOPSIS</span></span>
<span data-ttu-id="52a7a-103">Hämta Application Insights kontinuerligt Exportera konfiguration för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="52a7a-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="52a7a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52a7a-104">SYNTAX</span></span>

### <span data-ttu-id="52a7a-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="52a7a-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52a7a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52a7a-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52a7a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52a7a-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52a7a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52a7a-108">DESCRIPTION</span></span>
<span data-ttu-id="52a7a-109">Hämta Application Insights kontinuerligt Exportera konfiguration för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="52a7a-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="52a7a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52a7a-110">EXAMPLES</span></span>

### <span data-ttu-id="52a7a-111">Exempel 1 få kontinuerlig export för resurser med Application Insights</span><span class="sxs-lookup"><span data-stu-id="52a7a-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="52a7a-112">Hämta Application Insights kontinuerligt exportera konfigurationer för resursen "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="52a7a-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="52a7a-113">Exempel 2 få kontinuerlig export för resurser med Application Insights</span><span class="sxs-lookup"><span data-stu-id="52a7a-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

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

<span data-ttu-id="52a7a-114">Hämta Application Insights kontinuerligt Exportera konfiguration med export-ID "ZJrfffySPdtG3ESn3iRxVIEFuNY =" för resursen med namnet "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="52a7a-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="52a7a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52a7a-115">PARAMETERS</span></span>

### <span data-ttu-id="52a7a-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="52a7a-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="52a7a-117">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="52a7a-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="52a7a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a7a-118">-DefaultProfile</span></span>
<span data-ttu-id="52a7a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52a7a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52a7a-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="52a7a-120">-ExportId</span></span>
<span data-ttu-id="52a7a-121">Application Insights kontinuerligt exportera-ID.</span><span class="sxs-lookup"><span data-stu-id="52a7a-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a7a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="52a7a-122">-Name</span></span>
<span data-ttu-id="52a7a-123">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="52a7a-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="52a7a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a7a-124">-ResourceGroupName</span></span>
<span data-ttu-id="52a7a-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="52a7a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="52a7a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52a7a-126">-ResourceId</span></span>
<span data-ttu-id="52a7a-127">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="52a7a-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="52a7a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a7a-128">CommonParameters</span></span>
<span data-ttu-id="52a7a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52a7a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a7a-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52a7a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a7a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52a7a-131">INPUTS</span></span>

### <span data-ttu-id="52a7a-132">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="52a7a-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="52a7a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="52a7a-133">System.String</span></span>

## <span data-ttu-id="52a7a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52a7a-134">OUTPUTS</span></span>

### <span data-ttu-id="52a7a-135">Microsoft. Azure. commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="52a7a-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="52a7a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52a7a-136">NOTES</span></span>

## <span data-ttu-id="52a7a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52a7a-137">RELATED LINKS</span></span>