---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f4dfc77be9006229e2919dd1a4e0cdb1dd8c548e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579899"
---
# <span data-ttu-id="5ffb5-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5ffb5-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="5ffb5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ffb5-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffb5-103">Anger den lagrade åtkomst principen för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ffb5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ffb5-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ffb5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ffb5-105">DESCRIPTION</span></span>
<span data-ttu-id="5ffb5-106">Cmdleten **set-AzureStorageTableStoredAccessPolicy** anger den lagrade åtkomst principen för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="5ffb5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ffb5-107">EXAMPLES</span></span>

### <span data-ttu-id="5ffb5-108">Exempel 1: Ange en lagrad åtkomst princip i en tabell med fullständig behörighet</span><span class="sxs-lookup"><span data-stu-id="5ffb5-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="5ffb5-109">Det här kommandot ställer in en åtkomst princip med namnet Policy08 för lagrings tabellen tabellen.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="5ffb5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ffb5-110">PARAMETERS</span></span>

### <span data-ttu-id="5ffb5-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="5ffb5-111">-Context</span></span>
<span data-ttu-id="5ffb5-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5ffb5-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb5-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5ffb5-114">-ExpiryTime</span></span>
<span data-ttu-id="5ffb5-115">Anger den tid då den lagrade åtkomst policyn upphör att gälla.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-115">Specifies the time at which the stored access policy expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb5-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5ffb5-116">-NoExpiryTime</span></span>
<span data-ttu-id="5ffb5-117">Visar att åtkomst policyn inte har något utgångs datum.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-117">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb5-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="5ffb5-118">-NoStartTime</span></span>
<span data-ttu-id="5ffb5-119">Anger att start tiden är inställd på $Null.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-119">Indicates that the start time is set to $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb5-120">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="5ffb5-120">-Permission</span></span>
<span data-ttu-id="5ffb5-121">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings tabellen.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-121">Specifies permissions in the stored access policy to access the storage table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb5-122">-Princip</span><span class="sxs-lookup"><span data-stu-id="5ffb5-122">-Policy</span></span>
<span data-ttu-id="5ffb5-123">Anger namnet på den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-123">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb5-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5ffb5-124">-StartTime</span></span>
<span data-ttu-id="5ffb5-125">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-125">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb5-126">-Tabell</span><span class="sxs-lookup"><span data-stu-id="5ffb5-126">-Table</span></span>
<span data-ttu-id="5ffb5-127">Anger namnet på Azure Storage-tabellen.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-127">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb5-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ffb5-128">-Confirm</span></span>
<span data-ttu-id="5ffb5-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ffb5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ffb5-130">-WhatIf</span></span>
<span data-ttu-id="5ffb5-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ffb5-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ffb5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffb5-133">CommonParameters</span></span>
<span data-ttu-id="5ffb5-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffb5-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ffb5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffb5-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ffb5-136">INPUTS</span></span>

### <span data-ttu-id="5ffb5-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5ffb5-137">IStorageContext</span></span>

<span data-ttu-id="5ffb5-138">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5ffb5-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="5ffb5-139">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="5ffb5-139">String</span></span>

<span data-ttu-id="5ffb5-140">Parametern ' tabell ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="5ffb5-140">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5ffb5-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ffb5-141">OUTPUTS</span></span>

### <span data-ttu-id="5ffb5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5ffb5-142">System.String</span></span>

## <span data-ttu-id="5ffb5-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ffb5-143">NOTES</span></span>

## <span data-ttu-id="5ffb5-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ffb5-144">RELATED LINKS</span></span>

[<span data-ttu-id="5ffb5-145">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5ffb5-145">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5ffb5-146">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5ffb5-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="5ffb5-147">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5ffb5-147">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5ffb5-148">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5ffb5-148">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
