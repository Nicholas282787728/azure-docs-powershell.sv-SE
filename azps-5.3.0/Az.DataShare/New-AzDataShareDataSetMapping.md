---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 5792aeb937f82d3d80c0a6a7aea11e1ad0497970
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420632"
---
# <span data-ttu-id="8351e-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="8351e-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="8351e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8351e-102">SYNOPSIS</span></span>
<span data-ttu-id="8351e-103">Skapar data uppsättnings mappning för Share-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="8351e-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="8351e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8351e-104">SYNTAX</span></span>

### <span data-ttu-id="8351e-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8351e-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8351e-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="8351e-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8351e-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="8351e-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8351e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8351e-108">DESCRIPTION</span></span>
<span data-ttu-id="8351e-109">Cmdleten **New-AzDataShareDataSetMapping** skapar en data uppsättnings mappning mellan käll data uppsättningarna och Sink-kontot i dela prenumeration.</span><span class="sxs-lookup"><span data-stu-id="8351e-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="8351e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8351e-110">EXAMPLES</span></span>

### <span data-ttu-id="8351e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8351e-111">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccoutName "WikiAdsAccount" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsDataSetMapping" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName        : AdsContainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : AdsStorage
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/AdsShareSubscription/dataSetMappings/AdsDataSetMapping
Name                 : AdsDataSetMapping
Type                 : Microsoft.DataShare/DataSetMappings
```

<span data-ttu-id="8351e-112">Det här kommandot skapar en data uppsättnings mappning AdsDataSetMapping till Storage Account AdsStorage för Share abonnemang AdsShareSubscription i data Share Account WikiAdsAccount.</span><span class="sxs-lookup"><span data-stu-id="8351e-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="8351e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8351e-113">PARAMETERS</span></span>

### <span data-ttu-id="8351e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8351e-114">-AccountName</span></span>
<span data-ttu-id="8351e-115">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="8351e-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8351e-116">-Container</span><span class="sxs-lookup"><span data-stu-id="8351e-116">-Container</span></span>
<span data-ttu-id="8351e-117">Namn på behållare för Azure Storage-konto</span><span class="sxs-lookup"><span data-stu-id="8351e-117">Azure storage account container name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8351e-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="8351e-118">-DataSetId</span></span>
<span data-ttu-id="8351e-119">ID för konsument data uppsättning</span><span class="sxs-lookup"><span data-stu-id="8351e-119">Consumer data set id</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8351e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8351e-120">-DefaultProfile</span></span>
<span data-ttu-id="8351e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8351e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8351e-122">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="8351e-122">-FilePath</span></span>
<span data-ttu-id="8351e-123">Sökväg till Azure-lagringsplats</span><span class="sxs-lookup"><span data-stu-id="8351e-123">Azure storage file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8351e-124">-Fil system</span><span class="sxs-lookup"><span data-stu-id="8351e-124">-FileSystem</span></span>
<span data-ttu-id="8351e-125">Namn på fil systemet Azure ADLS Gen2</span><span class="sxs-lookup"><span data-stu-id="8351e-125">Azure ADLS gen2 file system name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8351e-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="8351e-126">-FolderPath</span></span>
<span data-ttu-id="8351e-127">Sökväg till Azure-lagringsplats</span><span class="sxs-lookup"><span data-stu-id="8351e-127">Azure storage folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8351e-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="8351e-128">-Name</span></span>
<span data-ttu-id="8351e-129">Mappnings namn för Azure Data uppsättning</span><span class="sxs-lookup"><span data-stu-id="8351e-129">Azure data set mapping name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8351e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8351e-130">-ResourceGroupName</span></span>
<span data-ttu-id="8351e-131">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="8351e-131">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8351e-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8351e-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="8351e-133">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="8351e-133">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8351e-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8351e-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="8351e-135">Konto-ResourceId för Azure Storage</span><span class="sxs-lookup"><span data-stu-id="8351e-135">Azure Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8351e-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8351e-136">-Confirm</span></span>
<span data-ttu-id="8351e-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8351e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8351e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8351e-138">-WhatIf</span></span>
<span data-ttu-id="8351e-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8351e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8351e-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8351e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8351e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8351e-141">CommonParameters</span></span>
<span data-ttu-id="8351e-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8351e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8351e-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8351e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8351e-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8351e-144">INPUTS</span></span>

### <span data-ttu-id="8351e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="8351e-145">System.String</span></span>

## <span data-ttu-id="8351e-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8351e-146">OUTPUTS</span></span>

### <span data-ttu-id="8351e-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="8351e-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="8351e-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8351e-148">NOTES</span></span>

## <span data-ttu-id="8351e-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8351e-149">RELATED LINKS</span></span>
