---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 7c35821cbaf75a616ab1b9b8bbc2db9fc2a96794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584763"
---
# <span data-ttu-id="ce99a-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ce99a-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="ce99a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce99a-102">SYNOPSIS</span></span>
<span data-ttu-id="ce99a-103">Skapar ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="ce99a-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce99a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce99a-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tags] <Hashtable>] [-MaxDegreeOfParallelism <Int32>]
 [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce99a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce99a-105">DESCRIPTION</span></span>
<span data-ttu-id="ce99a-106">Cmdleten **New-AzureRmDataLakeAnalyticsAccount** skapar ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="ce99a-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ce99a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce99a-107">EXAMPLES</span></span>

### <span data-ttu-id="ce99a-108">Exempel 1: skapa ett data Lake Analytics-konto</span><span class="sxs-lookup"><span data-stu-id="ce99a-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="ce99a-109">Det här kommandot skapar ett data Lake Analytics-konto med namnet ContosoAdlAccount som använder data lagret ContosoAdlStore i resurs gruppen med namnet ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="ce99a-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="ce99a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce99a-110">PARAMETERS</span></span>

### <span data-ttu-id="ce99a-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ce99a-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="ce99a-112">Anger namnet på data Lake Store-kontot som ska anges som standard data källa.</span><span class="sxs-lookup"><span data-stu-id="ce99a-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="ce99a-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="ce99a-113">-Location</span></span>
<span data-ttu-id="ce99a-114">Anger den plats där du vill skapa data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="ce99a-114">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="ce99a-115">Endast östra amerikanska 2 stöds för närvarande.</span><span class="sxs-lookup"><span data-stu-id="ce99a-115">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="ce99a-116">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="ce99a-116">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="ce99a-117">Den valfria högsta möjliga graden av parallellitet för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="ce99a-117">The optional maximum supported degree of parallelism for this account.</span></span> <span data-ttu-id="ce99a-118">Om inget anges, förvalda 30</span><span class="sxs-lookup"><span data-stu-id="ce99a-118">If none is specified, defaults to 30</span></span>

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

### <span data-ttu-id="ce99a-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="ce99a-119">-MaxJobCount</span></span>
<span data-ttu-id="ce99a-120">Det valfria maximalt tillåtna jobbet som körs under kontot samtidigt.</span><span class="sxs-lookup"><span data-stu-id="ce99a-120">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="ce99a-121">Om inget anges visas standardvärdet 3</span><span class="sxs-lookup"><span data-stu-id="ce99a-121">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="ce99a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ce99a-122">-Name</span></span>
<span data-ttu-id="ce99a-123">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="ce99a-123">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="ce99a-124">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="ce99a-124">-QueryStoreRetention</span></span>
<span data-ttu-id="ce99a-125">Det valfria antalet dagar som jobbets metadata bevaras.</span><span class="sxs-lookup"><span data-stu-id="ce99a-125">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="ce99a-126">Om inget anges är standardvärdet 30 dagar.</span><span class="sxs-lookup"><span data-stu-id="ce99a-126">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="ce99a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce99a-127">-ResourceGroupName</span></span>
<span data-ttu-id="ce99a-128">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="ce99a-128">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="ce99a-129">Använd New-AzureRmResourceGroup cmdlet för att skapa en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ce99a-129">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="ce99a-130">-Taggar</span><span class="sxs-lookup"><span data-stu-id="ce99a-130">-Tags</span></span>
<span data-ttu-id="ce99a-131">Anger par med nyckelord som kan användas för att identifiera data Lake Analytics-kontot bland andra Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="ce99a-131">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

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

### <span data-ttu-id="ce99a-132">-Tier</span><span class="sxs-lookup"><span data-stu-id="ce99a-132">-Tier</span></span>
<span data-ttu-id="ce99a-133">Önskad åtagande nivå för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="ce99a-133">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="ce99a-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce99a-134">-DefaultProfile</span></span>
<span data-ttu-id="ce99a-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce99a-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce99a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce99a-136">CommonParameters</span></span>
<span data-ttu-id="ce99a-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce99a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce99a-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce99a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce99a-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce99a-139">INPUTS</span></span>

## <span data-ttu-id="ce99a-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce99a-140">OUTPUTS</span></span>

### <span data-ttu-id="ce99a-141">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ce99a-141">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="ce99a-142">Information om det nya kontot.</span><span class="sxs-lookup"><span data-stu-id="ce99a-142">The details of the newly created account.</span></span>

## <span data-ttu-id="ce99a-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce99a-143">NOTES</span></span>

## <span data-ttu-id="ce99a-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce99a-144">RELATED LINKS</span></span>

[<span data-ttu-id="ce99a-145">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ce99a-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ce99a-146">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ce99a-146">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ce99a-147">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ce99a-147">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ce99a-148">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ce99a-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


