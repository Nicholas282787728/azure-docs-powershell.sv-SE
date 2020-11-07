---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 1c0306355dd9d95c4e0d6c07f7510d00c3238019
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745626"
---
# <span data-ttu-id="73bf6-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="73bf6-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="73bf6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="73bf6-103">Skapa en ny Application Insights-kontinuerlig export konfiguration för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="73bf6-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="73bf6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73bf6-104">SYNTAX</span></span>

### <span data-ttu-id="73bf6-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="73bf6-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73bf6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73bf6-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73bf6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73bf6-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73bf6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73bf6-108">DESCRIPTION</span></span>
<span data-ttu-id="73bf6-109">Skapa en ny Application Insights-kontinuerlig export konfiguration för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="73bf6-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="73bf6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73bf6-110">EXAMPLES</span></span>

### <span data-ttu-id="73bf6-111">Exempel 1 Skapa en ny kontinuerlig export konfiguration för resursen Application Insights</span><span class="sxs-lookup"><span data-stu-id="73bf6-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
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

<span data-ttu-id="73bf6-112">Skapa en ny Application Insights-kontinuerlig export konfiguration för att exportera "begäran" och "spåra" dokument typer till lagrings utrymme innehåller "testcontainer" i lagrings kontot "teststorageaccount" i resurs gruppen "testgroup".</span><span class="sxs-lookup"><span data-stu-id="73bf6-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="73bf6-113">SAS-token måste vara giltiga och ha Skriv behörighet till behållaren, annars fungerar inte löpande exportera. Om SAS-token upphörde att gälla kommer funktionen fort löp ande inte längre att fungera.</span><span class="sxs-lookup"><span data-stu-id="73bf6-113">The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="73bf6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73bf6-114">PARAMETERS</span></span>

### <span data-ttu-id="73bf6-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="73bf6-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="73bf6-116">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="73bf6-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="73bf6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73bf6-117">-DefaultProfile</span></span>
<span data-ttu-id="73bf6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73bf6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73bf6-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="73bf6-119">-DocumentType</span></span>
<span data-ttu-id="73bf6-120">Dokument typer som måste exporteras.</span><span class="sxs-lookup"><span data-stu-id="73bf6-120">Document types that need exported.</span></span>

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

### <span data-ttu-id="73bf6-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="73bf6-121">-Name</span></span>
<span data-ttu-id="73bf6-122">Komponent namn.</span><span class="sxs-lookup"><span data-stu-id="73bf6-122">Component Name.</span></span>

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

### <span data-ttu-id="73bf6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73bf6-123">-ResourceGroupName</span></span>
<span data-ttu-id="73bf6-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="73bf6-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="73bf6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73bf6-125">-ResourceId</span></span>
<span data-ttu-id="73bf6-126">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="73bf6-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="73bf6-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="73bf6-127">-StorageAccountId</span></span>
<span data-ttu-id="73bf6-128">Mål lagrings konto-ID.</span><span class="sxs-lookup"><span data-stu-id="73bf6-128">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="73bf6-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="73bf6-129">-StorageLocation</span></span>
<span data-ttu-id="73bf6-130">Plats-ID för mål lagring.</span><span class="sxs-lookup"><span data-stu-id="73bf6-130">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="73bf6-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="73bf6-131">-StorageSASUri</span></span>
<span data-ttu-id="73bf6-132">Mål-URI för lagrings utrymme.</span><span class="sxs-lookup"><span data-stu-id="73bf6-132">Destination Storage SAS Uri.</span></span>

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

### <span data-ttu-id="73bf6-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="73bf6-133">-Confirm</span></span>
<span data-ttu-id="73bf6-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73bf6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73bf6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73bf6-135">-WhatIf</span></span>
<span data-ttu-id="73bf6-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="73bf6-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73bf6-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="73bf6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73bf6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73bf6-138">CommonParameters</span></span>
<span data-ttu-id="73bf6-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73bf6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73bf6-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73bf6-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73bf6-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73bf6-141">INPUTS</span></span>

### <span data-ttu-id="73bf6-142">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="73bf6-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="73bf6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="73bf6-143">System.String</span></span>

## <span data-ttu-id="73bf6-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73bf6-144">OUTPUTS</span></span>

### <span data-ttu-id="73bf6-145">Microsoft. Azure. commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="73bf6-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="73bf6-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73bf6-146">NOTES</span></span>

## <span data-ttu-id="73bf6-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73bf6-147">RELATED LINKS</span></span>