---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
ms.openlocfilehash: b273dbec3fda421574c8866a10eda0a8098513ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572479"
---
# <span data-ttu-id="55717-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="55717-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="55717-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55717-102">SYNOPSIS</span></span>
<span data-ttu-id="55717-103">Ställer in en lagrad åtkomst policy för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="55717-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="55717-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55717-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55717-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55717-105">DESCRIPTION</span></span>
<span data-ttu-id="55717-106">Cmdleten **set-AzureStorageQueueStoredAccessPolicy** anger en lagrad åtkomst princip för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="55717-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="55717-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55717-107">EXAMPLES</span></span>

### <span data-ttu-id="55717-108">Exempel 1: Ange en lagrad åtkomst princip i kön</span><span class="sxs-lookup"><span data-stu-id="55717-108">Example 1: Set a stored access policy in the queue</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07"
```

<span data-ttu-id="55717-109">Det här kommandot anger en åtkomst princip med namnet Policy07 för lagringsmappen som heter min kö.</span><span class="sxs-lookup"><span data-stu-id="55717-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="55717-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55717-110">PARAMETERS</span></span>

### <span data-ttu-id="55717-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="55717-111">-Context</span></span>
<span data-ttu-id="55717-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="55717-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="55717-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="55717-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="55717-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="55717-114">-ExpiryTime</span></span>
<span data-ttu-id="55717-115">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="55717-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="55717-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="55717-116">-NoExpiryTime</span></span>
<span data-ttu-id="55717-117">Visar att åtkomst policyn inte har något utgångs datum.</span><span class="sxs-lookup"><span data-stu-id="55717-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="55717-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="55717-118">-NoStartTime</span></span>
<span data-ttu-id="55717-119">Anger att den här cmdleten ställer in start tiden som ska $Null.</span><span class="sxs-lookup"><span data-stu-id="55717-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="55717-120">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="55717-120">-Permission</span></span>
<span data-ttu-id="55717-121">Anger nivån för offentlig åtkomst till den här lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="55717-121">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="55717-122">-Princip</span><span class="sxs-lookup"><span data-stu-id="55717-122">-Policy</span></span>
<span data-ttu-id="55717-123">Anger en lagrad åtkomst princip som innehåller behörigheter för denna SAS-token.</span><span class="sxs-lookup"><span data-stu-id="55717-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="55717-124">-Kö</span><span class="sxs-lookup"><span data-stu-id="55717-124">-Queue</span></span>
<span data-ttu-id="55717-125">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="55717-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="55717-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="55717-126">-StartTime</span></span>
<span data-ttu-id="55717-127">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="55717-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="55717-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="55717-128">-Confirm</span></span>
<span data-ttu-id="55717-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="55717-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55717-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55717-130">-WhatIf</span></span>
<span data-ttu-id="55717-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="55717-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55717-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="55717-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55717-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55717-133">CommonParameters</span></span>
<span data-ttu-id="55717-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55717-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55717-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55717-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55717-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55717-136">INPUTS</span></span>

## <span data-ttu-id="55717-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55717-137">OUTPUTS</span></span>

## <span data-ttu-id="55717-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55717-138">NOTES</span></span>

## <span data-ttu-id="55717-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55717-139">RELATED LINKS</span></span>

[<span data-ttu-id="55717-140">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="55717-140">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="55717-141">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="55717-141">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="55717-142">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="55717-142">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
