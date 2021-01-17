---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 0f8d9860f04112c197b91907a7622683069c3589
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403291"
---
# <span data-ttu-id="4cbbb-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cbbb-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="4cbbb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cbbb-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbbb-103">Ställer in en lagrad åtkomst policy för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="4cbbb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cbbb-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cbbb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cbbb-105">DESCRIPTION</span></span>
<span data-ttu-id="4cbbb-106">Cmdleten **set-AzStorageQueueStoredAccessPolicy** anger en lagrad åtkomst princip för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="4cbbb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cbbb-107">EXAMPLES</span></span>

### <span data-ttu-id="4cbbb-108">Exempel 1: Ange en lagrad åtkomst princip i kön med fullständig behörighet</span><span class="sxs-lookup"><span data-stu-id="4cbbb-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="4cbbb-109">Det här kommandot anger en åtkomst princip med namnet Policy07 för lagringsmappen som heter min kö.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="4cbbb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cbbb-110">PARAMETERS</span></span>

### <span data-ttu-id="4cbbb-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4cbbb-111">-Context</span></span>
<span data-ttu-id="4cbbb-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4cbbb-113">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4cbbb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cbbb-114">-DefaultProfile</span></span>
<span data-ttu-id="4cbbb-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cbbb-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4cbbb-116">-ExpiryTime</span></span>
<span data-ttu-id="4cbbb-117">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="4cbbb-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4cbbb-118">-NoExpiryTime</span></span>
<span data-ttu-id="4cbbb-119">Visar att åtkomst policyn inte har något utgångs datum.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="4cbbb-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="4cbbb-120">-NoStartTime</span></span>
<span data-ttu-id="4cbbb-121">Anger att den här cmdleten ställer in start tiden som ska $Null.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="4cbbb-122">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="4cbbb-122">-Permission</span></span>
<span data-ttu-id="4cbbb-123">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="4cbbb-124">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="4cbbb-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="4cbbb-125">-Princip</span><span class="sxs-lookup"><span data-stu-id="4cbbb-125">-Policy</span></span>
<span data-ttu-id="4cbbb-126">Anger namnet på den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="4cbbb-127">-Kö</span><span class="sxs-lookup"><span data-stu-id="4cbbb-127">-Queue</span></span>
<span data-ttu-id="4cbbb-128">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="4cbbb-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4cbbb-129">-StartTime</span></span>
<span data-ttu-id="4cbbb-130">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="4cbbb-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4cbbb-131">-Confirm</span></span>
<span data-ttu-id="4cbbb-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cbbb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cbbb-133">-WhatIf</span></span>
<span data-ttu-id="4cbbb-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cbbb-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cbbb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbbb-136">CommonParameters</span></span>
<span data-ttu-id="4cbbb-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbbb-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cbbb-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbbb-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cbbb-139">INPUTS</span></span>

### <span data-ttu-id="4cbbb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4cbbb-140">System.String</span></span>

### <span data-ttu-id="4cbbb-141">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4cbbb-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4cbbb-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cbbb-142">OUTPUTS</span></span>

### <span data-ttu-id="4cbbb-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4cbbb-143">System.String</span></span>

## <span data-ttu-id="4cbbb-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cbbb-144">NOTES</span></span>

## <span data-ttu-id="4cbbb-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cbbb-145">RELATED LINKS</span></span>

[<span data-ttu-id="4cbbb-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cbbb-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4cbbb-147">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cbbb-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4cbbb-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cbbb-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
