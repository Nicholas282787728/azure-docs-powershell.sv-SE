---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8ca5efc7e5cee80fdf7ce34a13ce23ac733c0154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576560"
---
# <span data-ttu-id="7040c-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7040c-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="7040c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7040c-102">SYNOPSIS</span></span>
<span data-ttu-id="7040c-103">Ändrar ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="7040c-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7040c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7040c-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7040c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7040c-105">DESCRIPTION</span></span>
<span data-ttu-id="7040c-106">Cmdleten **set-AzureRmDataLakeAnalyticsAccount** ändrar ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="7040c-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7040c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7040c-107">EXAMPLES</span></span>

### <span data-ttu-id="7040c-108">Exempel 1: ändra data källan för ett konto</span><span class="sxs-lookup"><span data-stu-id="7040c-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="7040c-109">Det här kommandot ändrar standard data källan och egenskapen Tags för kontot.</span><span class="sxs-lookup"><span data-stu-id="7040c-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="7040c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7040c-110">PARAMETERS</span></span>

### <span data-ttu-id="7040c-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="7040c-111">-AllowAzureIpState</span></span>
<span data-ttu-id="7040c-112">Tillåt/blockera Azure med IP-adresser via brand väggen.</span><span class="sxs-lookup"><span data-stu-id="7040c-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: FirewallAllowAzureIpsState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7040c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7040c-113">-DefaultProfile</span></span>
<span data-ttu-id="7040c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7040c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7040c-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="7040c-115">-FirewallState</span></span>
<span data-ttu-id="7040c-116">Aktivera/inaktivera befintliga brand Väggs regler.</span><span class="sxs-lookup"><span data-stu-id="7040c-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: FirewallState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7040c-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="7040c-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="7040c-118">Det valfria Max antalet analys enheter som du kan använda för att uppdatera kontot.</span><span class="sxs-lookup"><span data-stu-id="7040c-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="7040c-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="7040c-119">-MaxJobCount</span></span>
<span data-ttu-id="7040c-120">Det valfria högsta tillåtna antalet jobb som körs under kontot samtidigt som du anger.</span><span class="sxs-lookup"><span data-stu-id="7040c-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="7040c-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="7040c-121">-Name</span></span>
<span data-ttu-id="7040c-122">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="7040c-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="7040c-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="7040c-123">-QueryStoreRetention</span></span>
<span data-ttu-id="7040c-124">Det valfria antalet dagar som jobbets metadata bevaras i kontot.</span><span class="sxs-lookup"><span data-stu-id="7040c-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="7040c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7040c-125">-ResourceGroupName</span></span>
<span data-ttu-id="7040c-126">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="7040c-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7040c-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7040c-127">-Tag</span></span>
<span data-ttu-id="7040c-128">En sträng, en sträng ord lista med taggar som är associerade till det här kontot och som ska ersätta den aktuella uppsättningen Taggar</span><span class="sxs-lookup"><span data-stu-id="7040c-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7040c-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="7040c-129">-Tier</span></span>
<span data-ttu-id="7040c-130">Önskad åtagande nivå för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="7040c-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="7040c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7040c-131">CommonParameters</span></span>
<span data-ttu-id="7040c-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7040c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7040c-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7040c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7040c-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7040c-134">INPUTS</span></span>

### <span data-ttu-id="7040c-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="7040c-135">None</span></span>
<span data-ttu-id="7040c-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7040c-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7040c-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7040c-137">OUTPUTS</span></span>

### <span data-ttu-id="7040c-138">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7040c-138">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="7040c-139">Uppdaterade konto uppgifter.</span><span class="sxs-lookup"><span data-stu-id="7040c-139">The updated account details.</span></span>

## <span data-ttu-id="7040c-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7040c-140">NOTES</span></span>

## <span data-ttu-id="7040c-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7040c-141">RELATED LINKS</span></span>

[<span data-ttu-id="7040c-142">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7040c-142">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7040c-143">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7040c-143">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7040c-144">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7040c-144">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7040c-145">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7040c-145">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


