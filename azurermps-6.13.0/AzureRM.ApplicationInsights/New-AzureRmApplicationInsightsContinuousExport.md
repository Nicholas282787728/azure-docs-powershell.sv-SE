---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 73aa26491a86b0eba01adb3898dba803f1ecf0eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575367"
---
# <span data-ttu-id="f2071-101">New-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="f2071-101">New-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="f2071-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2071-102">SYNOPSIS</span></span>
<span data-ttu-id="f2071-103">Skapa en ny Application Insights-kontinuerlig export konfiguration för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="f2071-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2071-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2071-104">SYNTAX</span></span>

### <span data-ttu-id="f2071-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f2071-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2071-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2071-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2071-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2071-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2071-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2071-108">DESCRIPTION</span></span>
<span data-ttu-id="f2071-109">Skapa en ny Application Insights-kontinuerlig export konfiguration för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="f2071-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="f2071-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2071-110">EXAMPLES</span></span>

### <span data-ttu-id="f2071-111">Exempel 1 Skapa en ny kontinuerlig export konfiguration för resursen Application Insights</span><span class="sxs-lookup"><span data-stu-id="f2071-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentType "Request","Trace", "Custom Event" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
 -StorageSASUri $sasuri

ExportId                         : jlTFEiBg1rkDXOCIeJQ2mB2TxZg=
StorageName                      : teststorageaccount
ContainerName                    : testcontainer
DocumentTypes                    : Request, Custom Event, Trace
DestinationStorageSubscriptionId : 50359d91-7b9d-4823-85af-eb298a61ba96
DestinationStorageLocationId     : sourcecentralus
DestinationStorageAccountId      : /subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="f2071-112">Skapa en ny Application Insights-kontinuerlig export konfiguration för att exportera "begäran" och "spåra" dokument typer till lagrings utrymme innehåller "testcontainer" i lagrings kontot "teststorageaccount" i resurs gruppen "testgroup".</span><span class="sxs-lookup"><span data-stu-id="f2071-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="f2071-113">SAS-token måste vara giltiga och ha Skriv behörighet till behållaren, annars fungerar inte ständig. Om SAS-token upphörde att gälla kommer funktionen fort löp ande inte längre att fungera.</span><span class="sxs-lookup"><span data-stu-id="f2071-113">The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="f2071-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2071-114">PARAMETERS</span></span>

### <span data-ttu-id="f2071-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f2071-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="f2071-116">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="f2071-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="f2071-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2071-117">-DefaultProfile</span></span>
<span data-ttu-id="f2071-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2071-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2071-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="f2071-119">-DocumentType</span></span>
<span data-ttu-id="f2071-120">Dokument typer som måste exporteras.</span><span class="sxs-lookup"><span data-stu-id="f2071-120">Document types that need exported.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2071-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2071-121">-Name</span></span>
<span data-ttu-id="f2071-122">Komponent namn.</span><span class="sxs-lookup"><span data-stu-id="f2071-122">Component Name.</span></span>

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

### <span data-ttu-id="f2071-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2071-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2071-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f2071-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="f2071-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2071-125">-ResourceId</span></span>
<span data-ttu-id="f2071-126">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="f2071-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="f2071-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f2071-127">-StorageAccountId</span></span>
<span data-ttu-id="f2071-128">Mål lagrings konto-ID.</span><span class="sxs-lookup"><span data-stu-id="f2071-128">Destination Storage Account Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2071-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="f2071-129">-StorageLocation</span></span>
<span data-ttu-id="f2071-130">Plats-ID för mål lagring.</span><span class="sxs-lookup"><span data-stu-id="f2071-130">Destination Storage Location Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2071-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="f2071-131">-StorageSASUri</span></span>
<span data-ttu-id="f2071-132">Mål-URI för lagrings utrymme.</span><span class="sxs-lookup"><span data-stu-id="f2071-132">Destination Storage SAS Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2071-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f2071-133">-Confirm</span></span>
<span data-ttu-id="f2071-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f2071-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2071-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2071-135">-WhatIf</span></span>
<span data-ttu-id="f2071-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f2071-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2071-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f2071-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2071-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2071-138">CommonParameters</span></span>
<span data-ttu-id="f2071-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2071-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2071-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2071-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2071-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2071-141">INPUTS</span></span>

### <span data-ttu-id="f2071-142">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f2071-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="f2071-143">Parametrar: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f2071-143">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="f2071-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f2071-144">System.String</span></span>

## <span data-ttu-id="f2071-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2071-145">OUTPUTS</span></span>

### <span data-ttu-id="f2071-146">Microsoft. Azure. commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2071-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="f2071-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2071-147">NOTES</span></span>

## <span data-ttu-id="f2071-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2071-148">RELATED LINKS</span></span>
