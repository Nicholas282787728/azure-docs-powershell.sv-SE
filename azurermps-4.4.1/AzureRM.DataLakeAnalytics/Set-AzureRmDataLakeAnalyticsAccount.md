---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8de6b2a0d86c9eb83a067f4982a5ef62d3a9adbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574699"
---
# <span data-ttu-id="866ce-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="866ce-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="866ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="866ce-102">SYNOPSIS</span></span>
<span data-ttu-id="866ce-103">Ändrar ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="866ce-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="866ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="866ce-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tags] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxDegreeOfParallelism <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="866ce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="866ce-105">DESCRIPTION</span></span>
<span data-ttu-id="866ce-106">Cmdleten **set-AzureRmDataLakeAnalyticsAccount** ändrar ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="866ce-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="866ce-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="866ce-107">EXAMPLES</span></span>

### <span data-ttu-id="866ce-108">Exempel 1: ändra data källan för ett konto</span><span class="sxs-lookup"><span data-stu-id="866ce-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="866ce-109">Det här kommandot ändrar standard data källan och egenskapen Tags för kontot.</span><span class="sxs-lookup"><span data-stu-id="866ce-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="866ce-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="866ce-110">PARAMETERS</span></span>

### <span data-ttu-id="866ce-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="866ce-111">-AllowAzureIpState</span></span>
<span data-ttu-id="866ce-112">Tillåt/blockera Azure med IP-adresser via brand väggen.</span><span class="sxs-lookup"><span data-stu-id="866ce-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866ce-113">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="866ce-113">-FirewallState</span></span>
<span data-ttu-id="866ce-114">Aktivera/inaktivera befintliga brand Väggs regler.</span><span class="sxs-lookup"><span data-stu-id="866ce-114">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState]
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866ce-115">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="866ce-115">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="866ce-116">Den valfria högsta graden av parallellitet som kan användas för att uppdatera kontot med.</span><span class="sxs-lookup"><span data-stu-id="866ce-116">The optional maximum supported degree of parallelism to update the account with.</span></span>

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

### <span data-ttu-id="866ce-117">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="866ce-117">-MaxJobCount</span></span>
<span data-ttu-id="866ce-118">Det valfria högsta tillåtna antalet jobb som körs under kontot samtidigt som du anger.</span><span class="sxs-lookup"><span data-stu-id="866ce-118">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="866ce-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="866ce-119">-Name</span></span>
<span data-ttu-id="866ce-120">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="866ce-120">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="866ce-121">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="866ce-121">-QueryStoreRetention</span></span>
<span data-ttu-id="866ce-122">Det valfria antalet dagar som jobbets metadata bevaras i kontot.</span><span class="sxs-lookup"><span data-stu-id="866ce-122">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="866ce-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="866ce-123">-ResourceGroupName</span></span>
<span data-ttu-id="866ce-124">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="866ce-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866ce-125">-Taggar</span><span class="sxs-lookup"><span data-stu-id="866ce-125">-Tags</span></span>
<span data-ttu-id="866ce-126">Anger par med nyckelord som kan användas för att identifiera data Lake Analytics-kontot bland andra Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="866ce-126">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866ce-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="866ce-127">-Tier</span></span>
<span data-ttu-id="866ce-128">Önskad åtagande nivå för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="866ce-128">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="866ce-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866ce-129">-DefaultProfile</span></span>
<span data-ttu-id="866ce-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="866ce-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="866ce-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866ce-131">CommonParameters</span></span>
<span data-ttu-id="866ce-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="866ce-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866ce-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="866ce-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866ce-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="866ce-134">INPUTS</span></span>

## <span data-ttu-id="866ce-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="866ce-135">OUTPUTS</span></span>

### <span data-ttu-id="866ce-136">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="866ce-136">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="866ce-137">Uppdaterade konto uppgifter.</span><span class="sxs-lookup"><span data-stu-id="866ce-137">The updated account details.</span></span>

## <span data-ttu-id="866ce-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="866ce-138">NOTES</span></span>

## <span data-ttu-id="866ce-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="866ce-139">RELATED LINKS</span></span>

[<span data-ttu-id="866ce-140">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="866ce-140">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="866ce-141">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="866ce-141">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="866ce-142">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="866ce-142">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="866ce-143">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="866ce-143">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


