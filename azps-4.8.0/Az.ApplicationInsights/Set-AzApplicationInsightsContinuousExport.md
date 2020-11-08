---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: fef34358855666d0f407c72831b2973ce95cc7e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102453"
---
# <span data-ttu-id="a8f3a-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="a8f3a-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="a8f3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f3a-103">Uppdatera en kontinuerlig export konfiguration i resursen Application Insights</span><span class="sxs-lookup"><span data-stu-id="a8f3a-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="a8f3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8f3a-104">SYNTAX</span></span>

### <span data-ttu-id="a8f3a-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a8f3a-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8f3a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8f3a-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8f3a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8f3a-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8f3a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8f3a-108">DESCRIPTION</span></span>
<span data-ttu-id="a8f3a-109">Uppdatera en kontinuerlig export konfiguration i resursen Application Insights</span><span class="sxs-lookup"><span data-stu-id="a8f3a-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="a8f3a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8f3a-110">EXAMPLES</span></span>

### <span data-ttu-id="a8f3a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a8f3a-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
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

<span data-ttu-id="a8f3a-112">Uppdatera kontinuerlig export konfiguration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" för resurs "test" i resurs gruppen "testgroup" för att exportera "begäran" och "spåra" dokument till lagrings behållaren "testcontainer" i "teststorageaccount". SAS-token måste vara giltiga och ha Skriv behörighet till behållaren, annars fungerar inte löpande exportera.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="a8f3a-113">Om SAS-token upphörde att gälla kommer funktionen fort löp ande inte längre att fungera.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="a8f3a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8f3a-114">PARAMETERS</span></span>

### <span data-ttu-id="a8f3a-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a8f3a-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="a8f3a-116">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="a8f3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f3a-117">-DefaultProfile</span></span>
<span data-ttu-id="a8f3a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8f3a-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8f3a-119">-DisableConfiguration</span></span>
<span data-ttu-id="a8f3a-120">Inaktivera löpande export eller inte.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-120">Disable continuous export or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f3a-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="a8f3a-121">-DocumentType</span></span>
<span data-ttu-id="a8f3a-122">Dokument typer som måste exporteras.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="a8f3a-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="a8f3a-123">-ExportId</span></span>
<span data-ttu-id="a8f3a-124">Application Insights kontinuerligt exportera-ID.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="a8f3a-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8f3a-125">-Name</span></span>
<span data-ttu-id="a8f3a-126">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="a8f3a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8f3a-127">-ResourceGroupName</span></span>
<span data-ttu-id="a8f3a-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="a8f3a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8f3a-129">-ResourceId</span></span>
<span data-ttu-id="a8f3a-130">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="a8f3a-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a8f3a-131">-StorageAccountId</span></span>
<span data-ttu-id="a8f3a-132">Mål lagrings konto-ID.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="a8f3a-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="a8f3a-133">-StorageLocation</span></span>
<span data-ttu-id="a8f3a-134">Plats-ID för mål lagring.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="a8f3a-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="a8f3a-135">-StorageSASUri</span></span>
<span data-ttu-id="a8f3a-136">Mål-URI för lagrings utrymme.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="a8f3a-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8f3a-137">-Confirm</span></span>
<span data-ttu-id="a8f3a-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8f3a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8f3a-139">-WhatIf</span></span>
<span data-ttu-id="a8f3a-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8f3a-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8f3a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f3a-142">CommonParameters</span></span>
<span data-ttu-id="a8f3a-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8f3a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f3a-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8f3a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f3a-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8f3a-145">INPUTS</span></span>

### <span data-ttu-id="a8f3a-146">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a8f3a-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="a8f3a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a8f3a-147">System.String</span></span>

## <span data-ttu-id="a8f3a-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8f3a-148">OUTPUTS</span></span>

### <span data-ttu-id="a8f3a-149">Microsoft. Azure. commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8f3a-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="a8f3a-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8f3a-150">NOTES</span></span>

## <span data-ttu-id="a8f3a-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8f3a-151">RELATED LINKS</span></span>
