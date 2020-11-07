---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: 074e6224c7a5b1ea1e8039901b75d223581495d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744529"
---
# <span data-ttu-id="6cebf-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="6cebf-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="6cebf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6cebf-102">SYNOPSIS</span></span>
<span data-ttu-id="6cebf-103">Anger eller tar bort förfallo tiden för en fil i ett Azure Data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="6cebf-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="6cebf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6cebf-104">SYNTAX</span></span>

### <span data-ttu-id="6cebf-105">SetAbsoluteNeverExpireExpiry (standard)</span><span class="sxs-lookup"><span data-stu-id="6cebf-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6cebf-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="6cebf-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cebf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6cebf-107">DESCRIPTION</span></span>
<span data-ttu-id="6cebf-108">Cmdleten **set-AzDataLakeStoreItemExpiry** anger eller tar bort förfallo tiden för en fil i ett Azure Data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="6cebf-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="6cebf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6cebf-109">EXAMPLES</span></span>

### <span data-ttu-id="6cebf-110">Exempel 1: Ange förfallo tid för en fil</span><span class="sxs-lookup"><span data-stu-id="6cebf-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="6cebf-111">Ställer in utgångs datum på filen myfile.txt i konto ContosoADL till två timmar från nu.</span><span class="sxs-lookup"><span data-stu-id="6cebf-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="6cebf-112">Detta gör att filen upphör att gälla (markeras för borttagning) om två timmar.</span><span class="sxs-lookup"><span data-stu-id="6cebf-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="6cebf-113">Exempel 2: ta bort utgångs datum för en fil</span><span class="sxs-lookup"><span data-stu-id="6cebf-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="6cebf-114">Tar bort eventuell utgångs datum som tidigare ställts in på filen myfile.txt i kontot ' ContosoADL '.</span><span class="sxs-lookup"><span data-stu-id="6cebf-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="6cebf-115">Det innebär att filen inte automatiskt upphör att gälla (markeras för borttagning) och måste tas bort manuellt eller ställas in på nytt.</span><span class="sxs-lookup"><span data-stu-id="6cebf-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="6cebf-116">Exempel 3: Ange förfallo tid för en fil relativt nu</span><span class="sxs-lookup"><span data-stu-id="6cebf-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="6cebf-117">Det första kommandot ställer in förfallo tiden för filen per myfile.txt 240 sekunder i förhållande till aktuell tid på servern.</span><span class="sxs-lookup"><span data-stu-id="6cebf-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="6cebf-118">Det andra kommandot ställer in förfallo tiden för filen per myfile.txt 240 sekunder i förhållande till skapande tid på Server.</span><span class="sxs-lookup"><span data-stu-id="6cebf-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="6cebf-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6cebf-119">PARAMETERS</span></span>

### <span data-ttu-id="6cebf-120">-Konto</span><span class="sxs-lookup"><span data-stu-id="6cebf-120">-Account</span></span>
<span data-ttu-id="6cebf-121">Anger namnet på data Lake Store-butiken.</span><span class="sxs-lookup"><span data-stu-id="6cebf-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="6cebf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cebf-122">-DefaultProfile</span></span>
<span data-ttu-id="6cebf-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6cebf-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cebf-124">-Utgång</span><span class="sxs-lookup"><span data-stu-id="6cebf-124">-Expiration</span></span>
<span data-ttu-id="6cebf-125">Den absoluta förfallo tiden för den angivna filen.</span><span class="sxs-lookup"><span data-stu-id="6cebf-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="6cebf-126">Om det inte finns något värde eller angett till MaxValue upphör filen aldrig att gälla.</span><span class="sxs-lookup"><span data-stu-id="6cebf-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cebf-127">-Path</span><span class="sxs-lookup"><span data-stu-id="6cebf-127">-Path</span></span>
<span data-ttu-id="6cebf-128">Anger data Lake Store-sökvägen för det fil objekt för vilket du vill ange eller ta bort förfallo datum.</span><span class="sxs-lookup"><span data-stu-id="6cebf-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cebf-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="6cebf-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="6cebf-130">Relativa utgångs alternativ.</span><span class="sxs-lookup"><span data-stu-id="6cebf-130">Relative expiry options.</span></span> <span data-ttu-id="6cebf-131">RelativeToNow eller RelativeToCreationDate är aktuella alternativ</span><span class="sxs-lookup"><span data-stu-id="6cebf-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cebf-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="6cebf-132">-RelativeTime</span></span>
<span data-ttu-id="6cebf-133">Den relativa tiden i millisekunder för nu eller skapande tid</span><span class="sxs-lookup"><span data-stu-id="6cebf-133">The relative time in milliseconds with respect to now or creation time</span></span>

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cebf-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6cebf-134">-Confirm</span></span>
<span data-ttu-id="6cebf-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6cebf-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cebf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cebf-136">-WhatIf</span></span>
<span data-ttu-id="6cebf-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6cebf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cebf-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6cebf-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cebf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cebf-139">CommonParameters</span></span>
<span data-ttu-id="6cebf-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cebf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cebf-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cebf-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cebf-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6cebf-142">INPUTS</span></span>

### <span data-ttu-id="6cebf-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6cebf-143">System.String</span></span>

### <span data-ttu-id="6cebf-144">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="6cebf-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6cebf-145">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6cebf-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="6cebf-146">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="6cebf-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="6cebf-147">System. Int64</span><span class="sxs-lookup"><span data-stu-id="6cebf-147">System.Int64</span></span>

## <span data-ttu-id="6cebf-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6cebf-148">OUTPUTS</span></span>

### <span data-ttu-id="6cebf-149">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6cebf-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="6cebf-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6cebf-150">NOTES</span></span>
<span data-ttu-id="6cebf-151">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="6cebf-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="6cebf-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6cebf-152">RELATED LINKS</span></span>

[<span data-ttu-id="6cebf-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6cebf-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

