---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 69ec2307dfdf8525f892720281079c58c1e1bd55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583920"
---
# <span data-ttu-id="fa3a6-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa3a6-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="fa3a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="fa3a6-103">Ställer in en lagrad åtkomst policy för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa3a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa3a6-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa3a6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa3a6-105">DESCRIPTION</span></span>
<span data-ttu-id="fa3a6-106">Cmdleten **set-AzureStorageQueueStoredAccessPolicy** anger en lagrad åtkomst princip för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="fa3a6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa3a6-107">EXAMPLES</span></span>

### <span data-ttu-id="fa3a6-108">Exempel 1: Ange en lagrad åtkomst princip i kön med fullständig behörighet</span><span class="sxs-lookup"><span data-stu-id="fa3a6-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="fa3a6-109">Det här kommandot anger en åtkomst princip med namnet Policy07 för lagringsmappen som heter min kö.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="fa3a6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa3a6-110">PARAMETERS</span></span>

### <span data-ttu-id="fa3a6-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="fa3a6-111">-Context</span></span>
<span data-ttu-id="fa3a6-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fa3a6-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fa3a6-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fa3a6-114">-ExpiryTime</span></span>
<span data-ttu-id="fa3a6-115">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="fa3a6-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fa3a6-116">-NoExpiryTime</span></span>
<span data-ttu-id="fa3a6-117">Visar att åtkomst policyn inte har något utgångs datum.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="fa3a6-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="fa3a6-118">-NoStartTime</span></span>
<span data-ttu-id="fa3a6-119">Anger att den här cmdleten ställer in start tiden som ska $Null.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="fa3a6-120">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="fa3a6-120">-Permission</span></span>
<span data-ttu-id="fa3a6-121">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-121">Specifies permissions in the stored access policy to access the storage queue.</span></span>

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

### <span data-ttu-id="fa3a6-122">-Princip</span><span class="sxs-lookup"><span data-stu-id="fa3a6-122">-Policy</span></span>
<span data-ttu-id="fa3a6-123">Anger namnet på den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-123">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="fa3a6-124">-Kö</span><span class="sxs-lookup"><span data-stu-id="fa3a6-124">-Queue</span></span>
<span data-ttu-id="fa3a6-125">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="fa3a6-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fa3a6-126">-StartTime</span></span>
<span data-ttu-id="fa3a6-127">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="fa3a6-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fa3a6-128">-Confirm</span></span>
<span data-ttu-id="fa3a6-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa3a6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa3a6-130">-WhatIf</span></span>
<span data-ttu-id="fa3a6-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa3a6-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa3a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa3a6-133">CommonParameters</span></span>
<span data-ttu-id="fa3a6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa3a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa3a6-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa3a6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa3a6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa3a6-136">INPUTS</span></span>

### <span data-ttu-id="fa3a6-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fa3a6-137">IStorageContext</span></span>

<span data-ttu-id="fa3a6-138">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="fa3a6-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="fa3a6-139">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="fa3a6-139">String</span></span>

<span data-ttu-id="fa3a6-140">Parametern ' Queue ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="fa3a6-140">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="fa3a6-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa3a6-141">OUTPUTS</span></span>

### <span data-ttu-id="fa3a6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fa3a6-142">System.String</span></span>

## <span data-ttu-id="fa3a6-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa3a6-143">NOTES</span></span>

## <span data-ttu-id="fa3a6-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa3a6-144">RELATED LINKS</span></span>

[<span data-ttu-id="fa3a6-145">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa3a6-145">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="fa3a6-146">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa3a6-146">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="fa3a6-147">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa3a6-147">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
