---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 2707100452f9b64c093b4ae52c724e09f6cfe6e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576562"
---
# <span data-ttu-id="83680-101">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="83680-101">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="83680-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83680-102">SYNOPSIS</span></span>
<span data-ttu-id="83680-103">Tar bort en data Källa från ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="83680-103">Removes a data source from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83680-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83680-104">SYNTAX</span></span>

### <span data-ttu-id="83680-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="83680-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83680-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="83680-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83680-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83680-107">DESCRIPTION</span></span>
<span data-ttu-id="83680-108">Cmdleten **Remove-AzureRmDataLakeAnalyticsDataSource** tar bort en data Källa från ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="83680-108">The **Remove-AzureRmDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="83680-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83680-109">EXAMPLES</span></span>

### <span data-ttu-id="83680-110">Exempel 1: ta bort en data Källa</span><span class="sxs-lookup"><span data-stu-id="83680-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="83680-111">Det här kommandot tar bort data källan som heter AzureStorage01 från kontot som heter ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="83680-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="83680-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83680-112">PARAMETERS</span></span>

### <span data-ttu-id="83680-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="83680-113">-Account</span></span>
<span data-ttu-id="83680-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="83680-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83680-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="83680-115">-Blob</span></span>
<span data-ttu-id="83680-116">Anger namnet på AzureBlob lagrings konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="83680-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83680-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="83680-117">-DataLakeStore</span></span>
<span data-ttu-id="83680-118">Anger namnet på den AzureData Lake Store-konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="83680-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83680-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83680-119">-DefaultProfile</span></span>
<span data-ttu-id="83680-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="83680-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83680-121">-Force</span><span class="sxs-lookup"><span data-stu-id="83680-121">-Force</span></span>
<span data-ttu-id="83680-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="83680-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83680-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83680-123">-PassThru</span></span>
<span data-ttu-id="83680-124">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="83680-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="83680-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="83680-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83680-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83680-126">-ResourceGroupName</span></span>
<span data-ttu-id="83680-127">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="83680-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83680-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="83680-128">-Confirm</span></span>
<span data-ttu-id="83680-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83680-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83680-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83680-130">-WhatIf</span></span>
<span data-ttu-id="83680-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="83680-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83680-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="83680-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83680-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83680-133">CommonParameters</span></span>
<span data-ttu-id="83680-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83680-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83680-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83680-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83680-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83680-136">INPUTS</span></span>

### <span data-ttu-id="83680-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="83680-137">None</span></span>
<span data-ttu-id="83680-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="83680-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83680-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83680-139">OUTPUTS</span></span>

### <span data-ttu-id="83680-140">bool</span><span class="sxs-lookup"><span data-stu-id="83680-140">bool</span></span>
<span data-ttu-id="83680-141">Om PassThru anges returneras sant när åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="83680-141">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="83680-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83680-142">NOTES</span></span>

## <span data-ttu-id="83680-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83680-143">RELATED LINKS</span></span>

[<span data-ttu-id="83680-144">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="83680-144">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="83680-145">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="83680-145">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


