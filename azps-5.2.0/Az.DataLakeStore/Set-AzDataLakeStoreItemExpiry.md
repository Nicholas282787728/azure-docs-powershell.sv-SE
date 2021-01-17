---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: ff769801c7a3496ab094e5c9877e0b53fb64fbfd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408616"
---
# <span data-ttu-id="a452c-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="a452c-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="a452c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a452c-102">SYNOPSIS</span></span>
<span data-ttu-id="a452c-103">Anger eller tar bort förfallo tiden för en fil i ett Azure Data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="a452c-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="a452c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a452c-104">SYNTAX</span></span>

### <span data-ttu-id="a452c-105">SetAbsoluteNeverExpireExpiry (standard)</span><span class="sxs-lookup"><span data-stu-id="a452c-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a452c-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="a452c-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a452c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a452c-107">DESCRIPTION</span></span>
<span data-ttu-id="a452c-108">Cmdleten **set-AzDataLakeStoreItemExpiry** anger eller tar bort förfallo tiden för en fil i ett Azure Data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="a452c-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="a452c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a452c-109">EXAMPLES</span></span>

### <span data-ttu-id="a452c-110">Exempel 1: Ange förfallo tid för en fil</span><span class="sxs-lookup"><span data-stu-id="a452c-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="a452c-111">Ställer in utgångs datum på filen myfile.txt i konto ContosoADL till två timmar från nu.</span><span class="sxs-lookup"><span data-stu-id="a452c-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="a452c-112">Detta gör att filen upphör att gälla (markeras för borttagning) om två timmar.</span><span class="sxs-lookup"><span data-stu-id="a452c-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="a452c-113">Exempel 2: ta bort utgångs datum för en fil</span><span class="sxs-lookup"><span data-stu-id="a452c-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="a452c-114">Tar bort eventuell utgångs datum som tidigare ställts in på filen myfile.txt i kontot ' ContosoADL '.</span><span class="sxs-lookup"><span data-stu-id="a452c-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="a452c-115">Det innebär att filen inte automatiskt upphör att gälla (markeras för borttagning) och måste tas bort manuellt eller ställas in på nytt.</span><span class="sxs-lookup"><span data-stu-id="a452c-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="a452c-116">Exempel 3: Ange förfallo tid för en fil relativt nu</span><span class="sxs-lookup"><span data-stu-id="a452c-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="a452c-117">Det första kommandot ställer in förfallo tiden för filen per myfile.txt 240 sekunder i förhållande till aktuell tid på servern.</span><span class="sxs-lookup"><span data-stu-id="a452c-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="a452c-118">Det andra kommandot ställer in förfallo tiden för filen per myfile.txt 240 sekunder i förhållande till skapande tid på Server.</span><span class="sxs-lookup"><span data-stu-id="a452c-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="a452c-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a452c-119">PARAMETERS</span></span>

### <span data-ttu-id="a452c-120">-Konto</span><span class="sxs-lookup"><span data-stu-id="a452c-120">-Account</span></span>
<span data-ttu-id="a452c-121">Anger namnet på data Lake Store-butiken.</span><span class="sxs-lookup"><span data-stu-id="a452c-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="a452c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a452c-122">-DefaultProfile</span></span>
<span data-ttu-id="a452c-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a452c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a452c-124">-Utgång</span><span class="sxs-lookup"><span data-stu-id="a452c-124">-Expiration</span></span>
<span data-ttu-id="a452c-125">Den absoluta förfallo tiden för den angivna filen.</span><span class="sxs-lookup"><span data-stu-id="a452c-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="a452c-126">Om det inte finns något värde eller angett till MaxValue upphör filen aldrig att gälla.</span><span class="sxs-lookup"><span data-stu-id="a452c-126">If no value or set to MaxValue, the file will never expire.</span></span>

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

### <span data-ttu-id="a452c-127">-Path</span><span class="sxs-lookup"><span data-stu-id="a452c-127">-Path</span></span>
<span data-ttu-id="a452c-128">Anger data Lake Store-sökvägen för det fil objekt för vilket du vill ange eller ta bort förfallo datum.</span><span class="sxs-lookup"><span data-stu-id="a452c-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="a452c-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="a452c-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="a452c-130">Relativa utgångs alternativ.</span><span class="sxs-lookup"><span data-stu-id="a452c-130">Relative expiry options.</span></span> <span data-ttu-id="a452c-131">RelativeToNow eller RelativeToCreationDate är aktuella alternativ</span><span class="sxs-lookup"><span data-stu-id="a452c-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

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

### <span data-ttu-id="a452c-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="a452c-132">-RelativeTime</span></span>
<span data-ttu-id="a452c-133">Den relativa tiden i millisekunder för nu eller skapande tid</span><span class="sxs-lookup"><span data-stu-id="a452c-133">The relative time in milliseconds with respect to now or creation time</span></span>

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

### <span data-ttu-id="a452c-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a452c-134">-Confirm</span></span>
<span data-ttu-id="a452c-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a452c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a452c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a452c-136">-WhatIf</span></span>
<span data-ttu-id="a452c-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a452c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a452c-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a452c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a452c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a452c-139">CommonParameters</span></span>
<span data-ttu-id="a452c-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a452c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a452c-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a452c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a452c-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a452c-142">INPUTS</span></span>

### <span data-ttu-id="a452c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a452c-143">System.String</span></span>

### <span data-ttu-id="a452c-144">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a452c-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a452c-145">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a452c-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="a452c-146">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="a452c-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="a452c-147">System. Int64</span><span class="sxs-lookup"><span data-stu-id="a452c-147">System.Int64</span></span>

## <span data-ttu-id="a452c-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a452c-148">OUTPUTS</span></span>

### <span data-ttu-id="a452c-149">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a452c-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="a452c-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a452c-150">NOTES</span></span>
<span data-ttu-id="a452c-151">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="a452c-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="a452c-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a452c-152">RELATED LINKS</span></span>

[<span data-ttu-id="a452c-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a452c-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

