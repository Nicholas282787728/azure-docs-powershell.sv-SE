---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: 6908bc4d474d0dbe9df045332f3820b5f7536dac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581203"
---
# <span data-ttu-id="5bc96-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="5bc96-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="5bc96-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5bc96-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc96-103">Anger eller tar bort förfallo tiden för en fil i ett Azure Data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="5bc96-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bc96-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5bc96-104">SYNTAX</span></span>

### <span data-ttu-id="5bc96-105">SetAbsoluteNeverExpireExpiry (standard)</span><span class="sxs-lookup"><span data-stu-id="5bc96-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bc96-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="5bc96-106">SetRelativeExpiry</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-RelativeFileExpiryOption] <PathRelativeExpiryOptions>] [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bc96-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5bc96-107">DESCRIPTION</span></span>
<span data-ttu-id="5bc96-108">Cmdleten **set-AzureRmDataLakeStoreItemExpiry** anger eller tar bort förfallo tiden för en fil i ett Azure Data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="5bc96-108">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="5bc96-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5bc96-109">EXAMPLES</span></span>

### <span data-ttu-id="5bc96-110">Exempel 1: Ange förfallo tid för en fil</span><span class="sxs-lookup"><span data-stu-id="5bc96-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="5bc96-111">Ställer in utgångs datum på filen myfile.txt i konto ContosoADL till två timmar från nu.</span><span class="sxs-lookup"><span data-stu-id="5bc96-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="5bc96-112">Detta gör att filen upphör att gälla (markeras för borttagning) om två timmar.</span><span class="sxs-lookup"><span data-stu-id="5bc96-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="5bc96-113">Exempel 2: ta bort utgångs datum för en fil</span><span class="sxs-lookup"><span data-stu-id="5bc96-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="5bc96-114">Tar bort eventuell utgångs datum som tidigare ställts in på filen myfile.txt i kontot ' ContosoADL '.</span><span class="sxs-lookup"><span data-stu-id="5bc96-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="5bc96-115">Det innebär att filen inte automatiskt upphör att gälla (markeras för borttagning) och måste tas bort manuellt eller ställas in på nytt.</span><span class="sxs-lookup"><span data-stu-id="5bc96-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>


### <span data-ttu-id="5bc96-116">Exempel 3: Ange förfallo tid för en fil relativt nu</span><span class="sxs-lookup"><span data-stu-id="5bc96-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="5bc96-117">Det första kommandot ställer in förfallo tiden för filen per myfile.txt 240 sekunder i förhållande till aktuell tid på servern.</span><span class="sxs-lookup"><span data-stu-id="5bc96-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>

<span data-ttu-id="5bc96-118">Det andra kommandot ställer in förfallo tiden för filen per myfile.txt 240 sekunder i förhållande till skapande tid på Server.</span><span class="sxs-lookup"><span data-stu-id="5bc96-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="5bc96-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5bc96-119">PARAMETERS</span></span>

### <span data-ttu-id="5bc96-120">-Konto</span><span class="sxs-lookup"><span data-stu-id="5bc96-120">-Account</span></span>
<span data-ttu-id="5bc96-121">Anger namnet på data Lake Store-butiken.</span><span class="sxs-lookup"><span data-stu-id="5bc96-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="5bc96-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc96-122">-DefaultProfile</span></span>
<span data-ttu-id="5bc96-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5bc96-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bc96-124">-Utgång</span><span class="sxs-lookup"><span data-stu-id="5bc96-124">-Expiration</span></span>
<span data-ttu-id="5bc96-125">Den absoluta förfallo tiden för den angivna filen.</span><span class="sxs-lookup"><span data-stu-id="5bc96-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="5bc96-126">Om det inte finns något värde eller angett till MaxValue upphör filen aldrig att gälla.</span><span class="sxs-lookup"><span data-stu-id="5bc96-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: Set expiry as Absolute or NeverExpire
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc96-127">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="5bc96-127">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="5bc96-128">Relativa utgångs alternativ.</span><span class="sxs-lookup"><span data-stu-id="5bc96-128">Relative expiry options.</span></span> <span data-ttu-id="5bc96-129">RelativeToNow eller RelativeToCreationDate är aktuella alternativ</span><span class="sxs-lookup"><span data-stu-id="5bc96-129">RelativeToNow or RelativeToCreationDate are current options</span></span>
```yaml
Type: PathRelativeExpiryOptions
Parameter Sets: Set expiry as relative to creation or now
Aliases: 
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc96-130">-Path</span><span class="sxs-lookup"><span data-stu-id="5bc96-130">-Path</span></span>
<span data-ttu-id="5bc96-131">Anger data Lake Store-sökvägen för det fil objekt för vilket du vill ange eller ta bort förfallo datum.</span><span class="sxs-lookup"><span data-stu-id="5bc96-131">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc96-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="5bc96-132">-RelativeTime</span></span>
<span data-ttu-id="5bc96-133">Den relativa tiden i millisekunder för nu eller skapande tid</span><span class="sxs-lookup"><span data-stu-id="5bc96-133">The relative time in milliseconds with respect to now or creation time</span></span>
```yaml
Type: Int64
Parameter Sets: Set expiry as relative to creation or now
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc96-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5bc96-134">-Confirm</span></span>
<span data-ttu-id="5bc96-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5bc96-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc96-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bc96-136">-WhatIf</span></span>
<span data-ttu-id="5bc96-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5bc96-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bc96-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5bc96-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc96-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc96-139">CommonParameters</span></span>
<span data-ttu-id="5bc96-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bc96-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc96-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bc96-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc96-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5bc96-142">INPUTS</span></span>

### <span data-ttu-id="5bc96-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="5bc96-143">None</span></span>
<span data-ttu-id="5bc96-144">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5bc96-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5bc96-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5bc96-145">OUTPUTS</span></span>

### <span data-ttu-id="5bc96-146">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5bc96-146">DataLakeStoreItem</span></span>
<span data-ttu-id="5bc96-147">Den uppdaterade filen med en ny förfallo tid.</span><span class="sxs-lookup"><span data-stu-id="5bc96-147">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="5bc96-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5bc96-148">NOTES</span></span>
<span data-ttu-id="5bc96-149">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="5bc96-149">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="5bc96-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5bc96-150">RELATED LINKS</span></span>

[<span data-ttu-id="5bc96-151">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5bc96-151">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

