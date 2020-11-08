---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 2a762bb115132f97dd31cf14f9f13d7c6cf5ef70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088264"
---
# <span data-ttu-id="8b274-101">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8b274-101">Set-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="8b274-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b274-102">SYNOPSIS</span></span>
<span data-ttu-id="8b274-103">Ändrar ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="8b274-103">Modifies a Data Lake Analytics account.</span></span>

## <span data-ttu-id="8b274-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b274-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b274-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b274-105">DESCRIPTION</span></span>
<span data-ttu-id="8b274-106">Cmdleten **set-AzDataLakeAnalyticsAccount** ändrar ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="8b274-106">The **Set-AzDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="8b274-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b274-107">EXAMPLES</span></span>

### <span data-ttu-id="8b274-108">Exempel 1: ändra data källan för ett konto</span><span class="sxs-lookup"><span data-stu-id="8b274-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="8b274-109">Det här kommandot ändrar standard data källan och egenskapen Tags för kontot.</span><span class="sxs-lookup"><span data-stu-id="8b274-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="8b274-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b274-110">PARAMETERS</span></span>

### <span data-ttu-id="8b274-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="8b274-111">-AllowAzureIpState</span></span>
<span data-ttu-id="8b274-112">Tillåt/blockera Azure med IP-adresser via brand väggen.</span><span class="sxs-lookup"><span data-stu-id="8b274-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="8b274-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b274-113">-DefaultProfile</span></span>
<span data-ttu-id="8b274-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8b274-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b274-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="8b274-115">-FirewallState</span></span>
<span data-ttu-id="8b274-116">Aktivera/inaktivera befintliga brand Väggs regler.</span><span class="sxs-lookup"><span data-stu-id="8b274-116">Optionally enable/disable existing firewall rules.</span></span>

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

### <span data-ttu-id="8b274-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="8b274-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="8b274-118">Det valfria Max antalet analys enheter som du kan använda för att uppdatera kontot.</span><span class="sxs-lookup"><span data-stu-id="8b274-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="8b274-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="8b274-119">-MaxJobCount</span></span>
<span data-ttu-id="8b274-120">Det valfria högsta tillåtna antalet jobb som körs under kontot samtidigt som du anger.</span><span class="sxs-lookup"><span data-stu-id="8b274-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="8b274-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b274-121">-Name</span></span>
<span data-ttu-id="8b274-122">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="8b274-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="8b274-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="8b274-123">-QueryStoreRetention</span></span>
<span data-ttu-id="8b274-124">Det valfria antalet dagar som jobbets metadata bevaras i kontot.</span><span class="sxs-lookup"><span data-stu-id="8b274-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="8b274-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b274-125">-ResourceGroupName</span></span>
<span data-ttu-id="8b274-126">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="8b274-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="8b274-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8b274-127">-Tag</span></span>
<span data-ttu-id="8b274-128">En sträng, en sträng ord lista med taggar som är associerade till det här kontot och som ska ersätta den aktuella uppsättningen Taggar</span><span class="sxs-lookup"><span data-stu-id="8b274-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

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

### <span data-ttu-id="8b274-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="8b274-129">-Tier</span></span>
<span data-ttu-id="8b274-130">Önskad åtagande nivå för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="8b274-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="8b274-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b274-131">CommonParameters</span></span>
<span data-ttu-id="8b274-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b274-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b274-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b274-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b274-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b274-134">INPUTS</span></span>

### <span data-ttu-id="8b274-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8b274-135">System.String</span></span>

### <span data-ttu-id="8b274-136">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="8b274-136">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8b274-137">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8b274-137">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8b274-138">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. Models. TierType, Microsoft. Azure. Management. DataLake. Analytics, version = 3.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8b274-138">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8b274-139">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. Models. FirewallState, Microsoft. Azure. Management. DataLake. Analytics, version = 3.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8b274-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8b274-140">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. DataLake. Analytics, version = 3.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8b274-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="8b274-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b274-141">OUTPUTS</span></span>

### <span data-ttu-id="8b274-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8b274-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="8b274-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b274-143">NOTES</span></span>

## <span data-ttu-id="8b274-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b274-144">RELATED LINKS</span></span>

[<span data-ttu-id="8b274-145">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8b274-145">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8b274-146">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8b274-146">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8b274-147">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8b274-147">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8b274-148">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8b274-148">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


