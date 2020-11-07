---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 996dc0ee168b11ecf3610b0d977854e32dd769bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755557"
---
# <span data-ttu-id="bfd4f-101">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="bfd4f-101">Set-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="bfd4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bfd4f-102">SYNOPSIS</span></span>
<span data-ttu-id="bfd4f-103">Uppdatera en kontinuerlig export konfiguration i en applciation-Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="bfd4f-103">Update a continuous export configuration in an applciation insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfd4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bfd4f-104">SYNTAX</span></span>

### <span data-ttu-id="bfd4f-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bfd4f-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfd4f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfd4f-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfd4f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfd4f-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfd4f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bfd4f-108">DESCRIPTION</span></span>
<span data-ttu-id="bfd4f-109">Uppdatera en kontinuerlig export konfiguration i en applciation-Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="bfd4f-109">Update a continuous export configuration in an applciation insights resource</span></span>

## <span data-ttu-id="bfd4f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bfd4f-110">EXAMPLES</span></span>

### <span data-ttu-id="bfd4f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bfd4f-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -DestinationStorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -DestinationStorageLocationId sourcecentralus
 -DestinationStorageSASUri $sasuri

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

<span data-ttu-id="bfd4f-112">Uppdatera kontinuerlig export konfiguration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" för resurs "test" i resurs gruppen "testgroup" för att exportera "begäran" och "spåra" dokument till lagrings behållaren "testcontainer" i "teststorageaccount". SAS-token måste vara giltiga och ha Skriv behörighet till behållaren, annars fungerar inte ständig.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.</span></span> <span data-ttu-id="bfd4f-113">Om SAS-token upphörde att gälla kommer funktionen fort löp ande inte längre att fungera.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="bfd4f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bfd4f-114">PARAMETERS</span></span>

### <span data-ttu-id="bfd4f-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="bfd4f-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="bfd4f-116">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="bfd4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfd4f-117">-DefaultProfile</span></span>
<span data-ttu-id="bfd4f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfd4f-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfd4f-119">-DisableConfiguration</span></span>
<span data-ttu-id="bfd4f-120">Inaktivera löpande export eller inte.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="bfd4f-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="bfd4f-121">-DocumentType</span></span>
<span data-ttu-id="bfd4f-122">Dokument typer som måste exporteras.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="bfd4f-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="bfd4f-123">-ExportId</span></span>
<span data-ttu-id="bfd4f-124">Application Insights kontinuerligt exportera-ID.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="bfd4f-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="bfd4f-125">-Name</span></span>
<span data-ttu-id="bfd4f-126">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="bfd4f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfd4f-127">-ResourceGroupName</span></span>
<span data-ttu-id="bfd4f-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="bfd4f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfd4f-129">-ResourceId</span></span>
<span data-ttu-id="bfd4f-130">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="bfd4f-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bfd4f-131">-StorageAccountId</span></span>
<span data-ttu-id="bfd4f-132">Mål lagrings konto-ID.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="bfd4f-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="bfd4f-133">-StorageLocation</span></span>
<span data-ttu-id="bfd4f-134">Plats-ID för mål lagring.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="bfd4f-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="bfd4f-135">-StorageSASUri</span></span>
<span data-ttu-id="bfd4f-136">Mål-URI för lagrings utrymme.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="bfd4f-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bfd4f-137">-Confirm</span></span>
<span data-ttu-id="bfd4f-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfd4f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfd4f-139">-WhatIf</span></span>
<span data-ttu-id="bfd4f-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfd4f-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfd4f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfd4f-142">CommonParameters</span></span>
<span data-ttu-id="bfd4f-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfd4f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfd4f-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfd4f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfd4f-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bfd4f-145">INPUTS</span></span>

### <span data-ttu-id="bfd4f-146">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="bfd4f-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="bfd4f-147">Parametrar: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bfd4f-147">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="bfd4f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="bfd4f-148">System.String</span></span>

## <span data-ttu-id="bfd4f-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bfd4f-149">OUTPUTS</span></span>

### <span data-ttu-id="bfd4f-150">Microsoft. Azure. commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfd4f-150">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="bfd4f-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bfd4f-151">NOTES</span></span>

## <span data-ttu-id="bfd4f-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bfd4f-152">RELATED LINKS</span></span>
