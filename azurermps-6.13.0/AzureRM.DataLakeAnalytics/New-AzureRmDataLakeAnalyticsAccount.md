---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 2fec19864e9d13e4b0e4ede1d351a08427e95357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582712"
---
# <span data-ttu-id="3c65a-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="3c65a-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="3c65a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c65a-102">SYNOPSIS</span></span>
<span data-ttu-id="3c65a-103">Skapar ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="3c65a-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c65a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c65a-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c65a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c65a-105">DESCRIPTION</span></span>
<span data-ttu-id="3c65a-106">Cmdleten **New-AzureRmDataLakeAnalyticsAccount** skapar ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="3c65a-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="3c65a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c65a-107">EXAMPLES</span></span>

### <span data-ttu-id="3c65a-108">Exempel 1: skapa ett data Lake Analytics-konto</span><span class="sxs-lookup"><span data-stu-id="3c65a-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="3c65a-109">Det här kommandot skapar ett data Lake Analytics-konto med namnet ContosoAdlAccount som använder data lagret ContosoAdlStore i resurs gruppen med namnet ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="3c65a-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="3c65a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c65a-110">PARAMETERS</span></span>

### <span data-ttu-id="3c65a-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3c65a-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="3c65a-112">Anger namnet på data Lake Store-kontot som ska anges som standard data källa.</span><span class="sxs-lookup"><span data-stu-id="3c65a-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c65a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c65a-113">-DefaultProfile</span></span>
<span data-ttu-id="3c65a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3c65a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c65a-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="3c65a-115">-Location</span></span>
<span data-ttu-id="3c65a-116">Anger den plats där du vill skapa data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="3c65a-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="3c65a-117">Endast östra amerikanska 2 stöds för närvarande.</span><span class="sxs-lookup"><span data-stu-id="3c65a-117">Only East US 2 is supported at this time.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c65a-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="3c65a-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="3c65a-119">Det valfria Max antalet analys enheter för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="3c65a-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c65a-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="3c65a-120">-MaxJobCount</span></span>
<span data-ttu-id="3c65a-121">Det valfria maximalt tillåtna jobbet som körs under kontot samtidigt.</span><span class="sxs-lookup"><span data-stu-id="3c65a-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="3c65a-122">Om inget anges visas standardvärdet 3</span><span class="sxs-lookup"><span data-stu-id="3c65a-122">If none is specified, defaults to 3</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c65a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="3c65a-123">-Name</span></span>
<span data-ttu-id="3c65a-124">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="3c65a-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c65a-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="3c65a-125">-QueryStoreRetention</span></span>
<span data-ttu-id="3c65a-126">Det valfria antalet dagar som jobbets metadata bevaras.</span><span class="sxs-lookup"><span data-stu-id="3c65a-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="3c65a-127">Om inget anges är standardvärdet 30 dagar.</span><span class="sxs-lookup"><span data-stu-id="3c65a-127">If none specified, the default is 30 days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c65a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c65a-128">-ResourceGroupName</span></span>
<span data-ttu-id="3c65a-129">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="3c65a-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="3c65a-130">Använd New-AzureRmResourceGroup cmdlet för att skapa en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3c65a-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c65a-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3c65a-131">-Tag</span></span>
<span data-ttu-id="3c65a-132">En sträng, en sträng ord lista med flaggor associerade till det här kontot</span><span class="sxs-lookup"><span data-stu-id="3c65a-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c65a-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="3c65a-133">-Tier</span></span>
<span data-ttu-id="3c65a-134">Önskad åtagande nivå för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="3c65a-134">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c65a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c65a-135">CommonParameters</span></span>
<span data-ttu-id="3c65a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c65a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c65a-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c65a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c65a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c65a-138">INPUTS</span></span>

### <span data-ttu-id="3c65a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3c65a-139">System.String</span></span>

### <span data-ttu-id="3c65a-140">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="3c65a-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3c65a-141">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3c65a-141">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="3c65a-142">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. Models. TierType, Microsoft. Azure. Management. DataLake. Analytics, version = 3.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3c65a-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="3c65a-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c65a-143">OUTPUTS</span></span>

### <span data-ttu-id="3c65a-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="3c65a-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="3c65a-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c65a-145">NOTES</span></span>

## <span data-ttu-id="3c65a-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c65a-146">RELATED LINKS</span></span>

[<span data-ttu-id="3c65a-147">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="3c65a-147">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="3c65a-148">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="3c65a-148">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="3c65a-149">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="3c65a-149">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="3c65a-150">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="3c65a-150">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


