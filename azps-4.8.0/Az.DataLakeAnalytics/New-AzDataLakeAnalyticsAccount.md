---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: c79665a6ed21309a7a702d9fd5bc5e876aa2ff21
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260239"
---
# <span data-ttu-id="93d76-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="93d76-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="93d76-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93d76-102">SYNOPSIS</span></span>
<span data-ttu-id="93d76-103">Skapar ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="93d76-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="93d76-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93d76-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93d76-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93d76-105">DESCRIPTION</span></span>
<span data-ttu-id="93d76-106">Cmdleten **New-AzDataLakeAnalyticsAccount** skapar ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="93d76-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="93d76-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93d76-107">EXAMPLES</span></span>

### <span data-ttu-id="93d76-108">Exempel 1: skapa ett data Lake Analytics-konto</span><span class="sxs-lookup"><span data-stu-id="93d76-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="93d76-109">Det här kommandot skapar ett data Lake Analytics-konto med namnet ContosoAdlAccount som använder data lagret ContosoAdlStore i resurs gruppen med namnet ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="93d76-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="93d76-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93d76-110">PARAMETERS</span></span>

### <span data-ttu-id="93d76-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="93d76-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="93d76-112">Anger namnet på data Lake Store-kontot som ska anges som standard data källa.</span><span class="sxs-lookup"><span data-stu-id="93d76-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="93d76-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d76-113">-DefaultProfile</span></span>
<span data-ttu-id="93d76-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="93d76-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93d76-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="93d76-115">-Location</span></span>
<span data-ttu-id="93d76-116">Anger den plats där du vill skapa data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="93d76-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="93d76-117">Endast östra amerikanska 2 stöds för närvarande.</span><span class="sxs-lookup"><span data-stu-id="93d76-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="93d76-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="93d76-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="93d76-119">Det valfria Max antalet analys enheter för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="93d76-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="93d76-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="93d76-120">-MaxJobCount</span></span>
<span data-ttu-id="93d76-121">Det valfria maximalt tillåtna jobbet som körs under kontot samtidigt.</span><span class="sxs-lookup"><span data-stu-id="93d76-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="93d76-122">Om inget anges visas standardvärdet 3</span><span class="sxs-lookup"><span data-stu-id="93d76-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="93d76-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="93d76-123">-Name</span></span>
<span data-ttu-id="93d76-124">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="93d76-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="93d76-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="93d76-125">-QueryStoreRetention</span></span>
<span data-ttu-id="93d76-126">Det valfria antalet dagar som jobbets metadata bevaras.</span><span class="sxs-lookup"><span data-stu-id="93d76-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="93d76-127">Om inget anges är standardvärdet 30 dagar.</span><span class="sxs-lookup"><span data-stu-id="93d76-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="93d76-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93d76-128">-ResourceGroupName</span></span>
<span data-ttu-id="93d76-129">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="93d76-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="93d76-130">Använd New-AzResourceGroup cmdlet för att skapa en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="93d76-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="93d76-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="93d76-131">-Tag</span></span>
<span data-ttu-id="93d76-132">En sträng, en sträng ord lista med flaggor associerade till det här kontot</span><span class="sxs-lookup"><span data-stu-id="93d76-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="93d76-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="93d76-133">-Tier</span></span>
<span data-ttu-id="93d76-134">Önskad åtagande nivå för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="93d76-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="93d76-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d76-135">CommonParameters</span></span>
<span data-ttu-id="93d76-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93d76-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d76-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93d76-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d76-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93d76-138">INPUTS</span></span>

### <span data-ttu-id="93d76-139">System. String</span><span class="sxs-lookup"><span data-stu-id="93d76-139">System.String</span></span>

### <span data-ttu-id="93d76-140">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="93d76-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="93d76-141">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="93d76-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="93d76-142">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. Models. TierType, Microsoft. Azure. Management. DataLake. Analytics, version = 3.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="93d76-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="93d76-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93d76-143">OUTPUTS</span></span>

### <span data-ttu-id="93d76-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="93d76-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="93d76-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93d76-145">NOTES</span></span>

## <span data-ttu-id="93d76-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93d76-146">RELATED LINKS</span></span>

[<span data-ttu-id="93d76-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="93d76-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="93d76-148">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="93d76-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="93d76-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="93d76-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="93d76-150">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="93d76-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


