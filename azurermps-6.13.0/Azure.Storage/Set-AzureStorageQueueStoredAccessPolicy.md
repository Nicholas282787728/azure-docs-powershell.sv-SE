---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: e20caedc23dcd4d06336f3dddf80fdaf4a84cbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579176"
---
# <span data-ttu-id="87610-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="87610-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="87610-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87610-102">SYNOPSIS</span></span>
<span data-ttu-id="87610-103">Ställer in en lagrad åtkomst policy för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="87610-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87610-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87610-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87610-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87610-105">DESCRIPTION</span></span>
<span data-ttu-id="87610-106">Cmdleten **set-AzureStorageQueueStoredAccessPolicy** anger en lagrad åtkomst princip för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="87610-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="87610-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87610-107">EXAMPLES</span></span>

### <span data-ttu-id="87610-108">Exempel 1: Ange en lagrad åtkomst princip i kön med fullständig behörighet</span><span class="sxs-lookup"><span data-stu-id="87610-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="87610-109">Det här kommandot anger en åtkomst princip med namnet Policy07 för lagringsmappen som heter min kö.</span><span class="sxs-lookup"><span data-stu-id="87610-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="87610-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87610-110">PARAMETERS</span></span>

### <span data-ttu-id="87610-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="87610-111">-Context</span></span>
<span data-ttu-id="87610-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="87610-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="87610-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="87610-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87610-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87610-114">-DefaultProfile</span></span>
<span data-ttu-id="87610-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="87610-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87610-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="87610-116">-ExpiryTime</span></span>
<span data-ttu-id="87610-117">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="87610-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87610-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="87610-118">-NoExpiryTime</span></span>
<span data-ttu-id="87610-119">Visar att åtkomst policyn inte har något utgångs datum.</span><span class="sxs-lookup"><span data-stu-id="87610-119">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87610-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="87610-120">-NoStartTime</span></span>
<span data-ttu-id="87610-121">Anger att den här cmdleten ställer in start tiden som ska $Null.</span><span class="sxs-lookup"><span data-stu-id="87610-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87610-122">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="87610-122">-Permission</span></span>
<span data-ttu-id="87610-123">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="87610-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="87610-124">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="87610-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87610-125">-Princip</span><span class="sxs-lookup"><span data-stu-id="87610-125">-Policy</span></span>
<span data-ttu-id="87610-126">Anger namnet på den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="87610-126">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87610-127">-Kö</span><span class="sxs-lookup"><span data-stu-id="87610-127">-Queue</span></span>
<span data-ttu-id="87610-128">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="87610-128">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87610-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="87610-129">-StartTime</span></span>
<span data-ttu-id="87610-130">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="87610-130">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87610-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="87610-131">-Confirm</span></span>
<span data-ttu-id="87610-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="87610-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87610-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87610-133">-WhatIf</span></span>
<span data-ttu-id="87610-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="87610-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87610-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="87610-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87610-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87610-136">CommonParameters</span></span>
<span data-ttu-id="87610-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87610-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87610-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87610-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87610-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87610-139">INPUTS</span></span>

### <span data-ttu-id="87610-140">System. String</span><span class="sxs-lookup"><span data-stu-id="87610-140">System.String</span></span>

### <span data-ttu-id="87610-141">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="87610-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="87610-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87610-142">OUTPUTS</span></span>

### <span data-ttu-id="87610-143">System. String</span><span class="sxs-lookup"><span data-stu-id="87610-143">System.String</span></span>

## <span data-ttu-id="87610-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87610-144">NOTES</span></span>

## <span data-ttu-id="87610-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87610-145">RELATED LINKS</span></span>

[<span data-ttu-id="87610-146">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="87610-146">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="87610-147">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="87610-147">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="87610-148">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="87610-148">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
