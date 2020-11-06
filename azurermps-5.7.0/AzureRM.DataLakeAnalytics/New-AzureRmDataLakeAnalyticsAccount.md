---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 36bf1bbfeb0c44189f5eeeaa0988d0314980e48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575689"
---
# <span data-ttu-id="a80cd-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a80cd-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="a80cd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a80cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a80cd-103">Skapar ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="a80cd-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a80cd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a80cd-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a80cd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a80cd-105">DESCRIPTION</span></span>
<span data-ttu-id="a80cd-106">Cmdleten **New-AzureRmDataLakeAnalyticsAccount** skapar ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="a80cd-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="a80cd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a80cd-107">EXAMPLES</span></span>

### <span data-ttu-id="a80cd-108">Exempel 1: skapa ett data Lake Analytics-konto</span><span class="sxs-lookup"><span data-stu-id="a80cd-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="a80cd-109">Det här kommandot skapar ett data Lake Analytics-konto med namnet ContosoAdlAccount som använder data lagret ContosoAdlStore i resurs gruppen med namnet ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="a80cd-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="a80cd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a80cd-110">PARAMETERS</span></span>

### <span data-ttu-id="a80cd-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a80cd-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="a80cd-112">Anger namnet på data Lake Store-kontot som ska anges som standard data källa.</span><span class="sxs-lookup"><span data-stu-id="a80cd-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a80cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a80cd-113">-DefaultProfile</span></span>
<span data-ttu-id="a80cd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a80cd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a80cd-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="a80cd-115">-Location</span></span>
<span data-ttu-id="a80cd-116">Anger den plats där du vill skapa data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="a80cd-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="a80cd-117">Endast östra amerikanska 2 stöds för närvarande.</span><span class="sxs-lookup"><span data-stu-id="a80cd-117">Only East US 2 is supported at this time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a80cd-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="a80cd-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="a80cd-119">Det valfria Max antalet analys enheter för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="a80cd-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a80cd-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="a80cd-120">-MaxJobCount</span></span>
<span data-ttu-id="a80cd-121">Det valfria maximalt tillåtna jobbet som körs under kontot samtidigt.</span><span class="sxs-lookup"><span data-stu-id="a80cd-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="a80cd-122">Om inget anges visas standardvärdet 3</span><span class="sxs-lookup"><span data-stu-id="a80cd-122">If none is specified, defaults to 3</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a80cd-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="a80cd-123">-Name</span></span>
<span data-ttu-id="a80cd-124">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="a80cd-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a80cd-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="a80cd-125">-QueryStoreRetention</span></span>
<span data-ttu-id="a80cd-126">Det valfria antalet dagar som jobbets metadata bevaras.</span><span class="sxs-lookup"><span data-stu-id="a80cd-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="a80cd-127">Om inget anges är standardvärdet 30 dagar.</span><span class="sxs-lookup"><span data-stu-id="a80cd-127">If none specified, the default is 30 days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a80cd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a80cd-128">-ResourceGroupName</span></span>
<span data-ttu-id="a80cd-129">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="a80cd-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="a80cd-130">Använd New-AzureRmResourceGroup cmdlet för att skapa en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a80cd-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a80cd-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a80cd-131">-Tag</span></span>
<span data-ttu-id="a80cd-132">En sträng, en sträng ord lista med flaggor associerade till det här kontot</span><span class="sxs-lookup"><span data-stu-id="a80cd-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a80cd-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="a80cd-133">-Tier</span></span>
<span data-ttu-id="a80cd-134">Önskad åtagande nivå för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="a80cd-134">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a80cd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a80cd-135">CommonParameters</span></span>
<span data-ttu-id="a80cd-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a80cd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a80cd-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a80cd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a80cd-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a80cd-138">INPUTS</span></span>

### <span data-ttu-id="a80cd-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="a80cd-139">None</span></span>
<span data-ttu-id="a80cd-140">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a80cd-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a80cd-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a80cd-141">OUTPUTS</span></span>

### <span data-ttu-id="a80cd-142">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a80cd-142">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="a80cd-143">Information om det nya kontot.</span><span class="sxs-lookup"><span data-stu-id="a80cd-143">The details of the newly created account.</span></span>

## <span data-ttu-id="a80cd-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a80cd-144">NOTES</span></span>

## <span data-ttu-id="a80cd-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a80cd-145">RELATED LINKS</span></span>

[<span data-ttu-id="a80cd-146">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a80cd-146">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a80cd-147">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a80cd-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a80cd-148">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a80cd-148">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a80cd-149">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a80cd-149">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


