---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 3cf556bce81a2e77250e597b428aa23c6eabe496
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089562"
---
# <span data-ttu-id="c117d-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="c117d-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="c117d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c117d-102">SYNOPSIS</span></span>
<span data-ttu-id="c117d-103">Skapar data uppsättnings mappning för Share-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c117d-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="c117d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c117d-104">SYNTAX</span></span>

### <span data-ttu-id="c117d-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c117d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c117d-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="c117d-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c117d-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="c117d-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c117d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c117d-108">DESCRIPTION</span></span>
<span data-ttu-id="c117d-109">Cmdleten **New-AzDataShareDataSetMapping** skapar en data uppsättnings mappning mellan käll data uppsättningarna och Sink-kontot i dela prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c117d-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="c117d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c117d-110">EXAMPLES</span></span>

### <span data-ttu-id="c117d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c117d-111">Example 1</span></span>
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

<span data-ttu-id="c117d-112">Det här kommandot skapar en data uppsättnings mappning AdsDataSetMapping till Storage Account AdsStorage för Share abonnemang AdsShareSubscription i data Share Account WikiAdsAccount.</span><span class="sxs-lookup"><span data-stu-id="c117d-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="c117d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c117d-113">PARAMETERS</span></span>

### <span data-ttu-id="c117d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c117d-114">-AccountName</span></span>
<span data-ttu-id="c117d-115">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="c117d-115">Azure data share account name</span></span>

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

### <span data-ttu-id="c117d-116">-Container</span><span class="sxs-lookup"><span data-stu-id="c117d-116">-Container</span></span>
<span data-ttu-id="c117d-117">Namn på behållare för Azure Storage-konto</span><span class="sxs-lookup"><span data-stu-id="c117d-117">Azure storage account container name</span></span>

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

### <span data-ttu-id="c117d-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="c117d-118">-DataSetId</span></span>
<span data-ttu-id="c117d-119">ID för konsument data uppsättning</span><span class="sxs-lookup"><span data-stu-id="c117d-119">Consumer data set id</span></span>

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

### <span data-ttu-id="c117d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c117d-120">-DefaultProfile</span></span>
<span data-ttu-id="c117d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c117d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c117d-122">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="c117d-122">-FilePath</span></span>
<span data-ttu-id="c117d-123">Sökväg till Azure-lagringsplats</span><span class="sxs-lookup"><span data-stu-id="c117d-123">Azure storage file path</span></span>

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

### <span data-ttu-id="c117d-124">-Fil system</span><span class="sxs-lookup"><span data-stu-id="c117d-124">-FileSystem</span></span>
<span data-ttu-id="c117d-125">Namn på fil systemet Azure ADLS Gen2</span><span class="sxs-lookup"><span data-stu-id="c117d-125">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="c117d-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="c117d-126">-FolderPath</span></span>
<span data-ttu-id="c117d-127">Sökväg till Azure-lagringsplats</span><span class="sxs-lookup"><span data-stu-id="c117d-127">Azure storage folder path</span></span>

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

### <span data-ttu-id="c117d-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="c117d-128">-Name</span></span>
<span data-ttu-id="c117d-129">Mappnings namn för Azure Data uppsättning</span><span class="sxs-lookup"><span data-stu-id="c117d-129">Azure data set mapping name</span></span>

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

### <span data-ttu-id="c117d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c117d-130">-ResourceGroupName</span></span>
<span data-ttu-id="c117d-131">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="c117d-131">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c117d-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c117d-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="c117d-133">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="c117d-133">Azure data share subscription name</span></span>

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

### <span data-ttu-id="c117d-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c117d-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="c117d-135">Konto-ResourceId för Azure Storage</span><span class="sxs-lookup"><span data-stu-id="c117d-135">Azure Storage Account ResourceId</span></span>

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

### <span data-ttu-id="c117d-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c117d-136">-Confirm</span></span>
<span data-ttu-id="c117d-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c117d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c117d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c117d-138">-WhatIf</span></span>
<span data-ttu-id="c117d-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c117d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c117d-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c117d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c117d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c117d-141">CommonParameters</span></span>
<span data-ttu-id="c117d-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c117d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c117d-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c117d-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c117d-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c117d-144">INPUTS</span></span>

### <span data-ttu-id="c117d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c117d-145">System.String</span></span>

## <span data-ttu-id="c117d-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c117d-146">OUTPUTS</span></span>

### <span data-ttu-id="c117d-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="c117d-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="c117d-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c117d-148">NOTES</span></span>

## <span data-ttu-id="c117d-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c117d-149">RELATED LINKS</span></span>
