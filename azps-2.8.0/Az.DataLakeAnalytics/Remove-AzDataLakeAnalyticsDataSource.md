---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 43f1ac12e6f88faa43dcc4f96157425f2e180680
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744627"
---
# <span data-ttu-id="4ef14-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="4ef14-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="4ef14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ef14-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef14-103">Tar bort en data Källa från ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="4ef14-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="4ef14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ef14-104">SYNTAX</span></span>

### <span data-ttu-id="4ef14-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ef14-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ef14-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ef14-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ef14-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ef14-107">DESCRIPTION</span></span>
<span data-ttu-id="4ef14-108">Cmdleten **Remove-AzDataLakeAnalyticsDataSource** tar bort en data Källa från ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="4ef14-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4ef14-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ef14-109">EXAMPLES</span></span>

### <span data-ttu-id="4ef14-110">Exempel 1: ta bort en data Källa</span><span class="sxs-lookup"><span data-stu-id="4ef14-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="4ef14-111">Det här kommandot tar bort data källan som heter AzureStorage01 från kontot som heter ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="4ef14-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="4ef14-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ef14-112">PARAMETERS</span></span>

### <span data-ttu-id="4ef14-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="4ef14-113">-Account</span></span>
<span data-ttu-id="4ef14-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="4ef14-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef14-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="4ef14-115">-Blob</span></span>
<span data-ttu-id="4ef14-116">Anger namnet på AzureBlob lagrings konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4ef14-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef14-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ef14-117">-DataLakeStore</span></span>
<span data-ttu-id="4ef14-118">Anger namnet på den AzureData Lake Store-konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4ef14-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef14-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef14-119">-DefaultProfile</span></span>
<span data-ttu-id="4ef14-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4ef14-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ef14-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4ef14-121">-Force</span></span>
<span data-ttu-id="4ef14-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4ef14-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef14-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ef14-123">-PassThru</span></span>
<span data-ttu-id="4ef14-124">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="4ef14-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4ef14-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="4ef14-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef14-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ef14-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ef14-127">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="4ef14-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef14-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ef14-128">-Confirm</span></span>
<span data-ttu-id="4ef14-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ef14-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef14-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ef14-130">-WhatIf</span></span>
<span data-ttu-id="4ef14-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ef14-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ef14-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ef14-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef14-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef14-133">CommonParameters</span></span>
<span data-ttu-id="4ef14-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ef14-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef14-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ef14-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef14-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ef14-136">INPUTS</span></span>

### <span data-ttu-id="4ef14-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4ef14-137">System.String</span></span>

## <span data-ttu-id="4ef14-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ef14-138">OUTPUTS</span></span>

### <span data-ttu-id="4ef14-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ef14-139">System.Boolean</span></span>

## <span data-ttu-id="4ef14-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ef14-140">NOTES</span></span>

## <span data-ttu-id="4ef14-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ef14-141">RELATED LINKS</span></span>

[<span data-ttu-id="4ef14-142">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="4ef14-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="4ef14-143">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="4ef14-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


