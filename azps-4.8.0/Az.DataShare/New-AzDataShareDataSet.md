---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 5dbf797ffabdf42b1d30d9d709ba6bb3153d8696
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102907"
---
# <span data-ttu-id="74640-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="74640-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="74640-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74640-102">SYNOPSIS</span></span>
<span data-ttu-id="74640-103">Lägger till data uppsättningar i Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="74640-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="74640-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74640-104">SYNTAX</span></span>

### <span data-ttu-id="74640-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="74640-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74640-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="74640-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74640-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="74640-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74640-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="74640-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74640-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74640-109">DESCRIPTION</span></span>
<span data-ttu-id="74640-110">**New-AzDataShareDataSet-** cmdleten lägga till data uppsättningar i Azure Data Share för data delnings konto.</span><span class="sxs-lookup"><span data-stu-id="74640-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="74640-111">Du kan lägga till data uppsättningar av typen BLOB, ADLS Gen2 och ADLS gen1.</span><span class="sxs-lookup"><span data-stu-id="74640-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="74640-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74640-112">EXAMPLES</span></span>

### <span data-ttu-id="74640-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="74640-113">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="74640-114">Det här kommandot lägger till en data mängd som heter AdsDataSet av typen BLOB-behållare i Azure Data Share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="74640-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="74640-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74640-115">PARAMETERS</span></span>

### <span data-ttu-id="74640-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="74640-116">-AccountName</span></span>
<span data-ttu-id="74640-117">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="74640-117">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74640-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="74640-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="74640-119">Azure Storage ADLS gen1-mappsökväg</span><span class="sxs-lookup"><span data-stu-id="74640-119">Azure storage ADLS gen1 folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74640-120">-Container</span><span class="sxs-lookup"><span data-stu-id="74640-120">-Container</span></span>
<span data-ttu-id="74640-121">Namn på behållare för Azure Storage-konto</span><span class="sxs-lookup"><span data-stu-id="74640-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="74640-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74640-122">-DefaultProfile</span></span>
<span data-ttu-id="74640-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74640-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74640-124">-FileName</span><span class="sxs-lookup"><span data-stu-id="74640-124">-FileName</span></span>
<span data-ttu-id="74640-125">Azure Storage ADLS gen1 fil namn</span><span class="sxs-lookup"><span data-stu-id="74640-125">Azure storage ADLS gen1 file name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74640-126">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="74640-126">-FilePath</span></span>
<span data-ttu-id="74640-127">Sökväg till Azure-lagringsplats</span><span class="sxs-lookup"><span data-stu-id="74640-127">Azure storage file path</span></span>

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

### <span data-ttu-id="74640-128">-Fil system</span><span class="sxs-lookup"><span data-stu-id="74640-128">-FileSystem</span></span>
<span data-ttu-id="74640-129">Namn på fil systemet Azure ADLS Gen2</span><span class="sxs-lookup"><span data-stu-id="74640-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="74640-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="74640-130">-FolderPath</span></span>
<span data-ttu-id="74640-131">Sökväg till Azure-lagringsplats</span><span class="sxs-lookup"><span data-stu-id="74640-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="74640-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="74640-132">-Name</span></span>
<span data-ttu-id="74640-133">Namn på Azure Data uppsättning</span><span class="sxs-lookup"><span data-stu-id="74640-133">Azure data set name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74640-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74640-134">-ResourceGroupName</span></span>
<span data-ttu-id="74640-135">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="74640-135">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74640-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="74640-136">-ShareName</span></span>
<span data-ttu-id="74640-137">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="74640-137">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74640-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="74640-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="74640-139">Konto-resourceId för Azure Storage</span><span class="sxs-lookup"><span data-stu-id="74640-139">Azure storage account resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74640-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74640-140">-Confirm</span></span>
<span data-ttu-id="74640-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74640-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74640-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74640-142">-WhatIf</span></span>
<span data-ttu-id="74640-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74640-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74640-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74640-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74640-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74640-145">CommonParameters</span></span>
<span data-ttu-id="74640-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74640-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74640-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74640-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74640-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74640-148">INPUTS</span></span>

### <span data-ttu-id="74640-149">System. String</span><span class="sxs-lookup"><span data-stu-id="74640-149">System.String</span></span>

## <span data-ttu-id="74640-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74640-150">OUTPUTS</span></span>

### <span data-ttu-id="74640-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="74640-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="74640-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74640-152">NOTES</span></span>

## <span data-ttu-id="74640-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74640-153">RELATED LINKS</span></span>