---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 41ae0d3c985bbb5e1d58f92287fa4a0050dfa738
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746251"
---
# <span data-ttu-id="adb0e-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="adb0e-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="adb0e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="adb0e-102">SYNOPSIS</span></span>
<span data-ttu-id="adb0e-103">Anger den lagrade åtkomst principen för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="adb0e-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="adb0e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="adb0e-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adb0e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="adb0e-105">DESCRIPTION</span></span>
<span data-ttu-id="adb0e-106">Cmdleten **set-AzStorageTableStoredAccessPolicy** anger den lagrade åtkomst principen för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="adb0e-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="adb0e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="adb0e-107">EXAMPLES</span></span>

### <span data-ttu-id="adb0e-108">Exempel 1: Ange en lagrad åtkomst princip i en tabell med fullständig behörighet</span><span class="sxs-lookup"><span data-stu-id="adb0e-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="adb0e-109">Det här kommandot ställer in en åtkomst princip med namnet Policy08 för lagrings tabellen tabellen.</span><span class="sxs-lookup"><span data-stu-id="adb0e-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="adb0e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="adb0e-110">PARAMETERS</span></span>

### <span data-ttu-id="adb0e-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="adb0e-111">-Context</span></span>
<span data-ttu-id="adb0e-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="adb0e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="adb0e-113">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="adb0e-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="adb0e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb0e-114">-DefaultProfile</span></span>
<span data-ttu-id="adb0e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="adb0e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adb0e-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="adb0e-116">-ExpiryTime</span></span>
<span data-ttu-id="adb0e-117">Anger den tid då den lagrade åtkomst policyn upphör att gälla.</span><span class="sxs-lookup"><span data-stu-id="adb0e-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="adb0e-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="adb0e-118">-NoExpiryTime</span></span>
<span data-ttu-id="adb0e-119">Visar att åtkomst policyn inte har något utgångs datum.</span><span class="sxs-lookup"><span data-stu-id="adb0e-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="adb0e-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="adb0e-120">-NoStartTime</span></span>
<span data-ttu-id="adb0e-121">Anger att start tiden är inställd på $Null.</span><span class="sxs-lookup"><span data-stu-id="adb0e-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="adb0e-122">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="adb0e-122">-Permission</span></span>
<span data-ttu-id="adb0e-123">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings tabellen.</span><span class="sxs-lookup"><span data-stu-id="adb0e-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="adb0e-124">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="adb0e-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="adb0e-125">-Princip</span><span class="sxs-lookup"><span data-stu-id="adb0e-125">-Policy</span></span>
<span data-ttu-id="adb0e-126">Anger namnet på den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="adb0e-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="adb0e-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="adb0e-127">-StartTime</span></span>
<span data-ttu-id="adb0e-128">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="adb0e-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="adb0e-129">-Tabell</span><span class="sxs-lookup"><span data-stu-id="adb0e-129">-Table</span></span>
<span data-ttu-id="adb0e-130">Anger namnet på Azure Storage-tabellen.</span><span class="sxs-lookup"><span data-stu-id="adb0e-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="adb0e-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="adb0e-131">-Confirm</span></span>
<span data-ttu-id="adb0e-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="adb0e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adb0e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adb0e-133">-WhatIf</span></span>
<span data-ttu-id="adb0e-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="adb0e-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="adb0e-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="adb0e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adb0e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb0e-136">CommonParameters</span></span>
<span data-ttu-id="adb0e-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adb0e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb0e-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adb0e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb0e-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="adb0e-139">INPUTS</span></span>

### <span data-ttu-id="adb0e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="adb0e-140">System.String</span></span>

### <span data-ttu-id="adb0e-141">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="adb0e-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="adb0e-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="adb0e-142">OUTPUTS</span></span>

### <span data-ttu-id="adb0e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="adb0e-143">System.String</span></span>

## <span data-ttu-id="adb0e-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="adb0e-144">NOTES</span></span>

## <span data-ttu-id="adb0e-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="adb0e-145">RELATED LINKS</span></span>

[<span data-ttu-id="adb0e-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="adb0e-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="adb0e-147">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="adb0e-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="adb0e-148">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="adb0e-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="adb0e-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="adb0e-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
