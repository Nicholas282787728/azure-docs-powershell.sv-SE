---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
ms.openlocfilehash: d517ca49f0be3b6add58d151b3b2f79dad17611c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572468"
---
# <span data-ttu-id="655dd-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="655dd-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="655dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="655dd-102">SYNOPSIS</span></span>
<span data-ttu-id="655dd-103">Anger den lagrade åtkomst principen för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="655dd-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="655dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="655dd-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="655dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="655dd-105">DESCRIPTION</span></span>
<span data-ttu-id="655dd-106">Cmdleten **set-AzureStorageTableStoredAccessPolicy** anger den lagrade åtkomst principen för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="655dd-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="655dd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="655dd-107">EXAMPLES</span></span>

### <span data-ttu-id="655dd-108">Exempel 1: Ange en lagrad åtkomst princip i en tabell med fullständig behörighet</span><span class="sxs-lookup"><span data-stu-id="655dd-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08"
```

<span data-ttu-id="655dd-109">Det här kommandot ställer in en åtkomst princip med namnet Policy08 för lagrings tabellen tabellen.</span><span class="sxs-lookup"><span data-stu-id="655dd-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="655dd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="655dd-110">PARAMETERS</span></span>

### <span data-ttu-id="655dd-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="655dd-111">-Context</span></span>
<span data-ttu-id="655dd-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="655dd-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="655dd-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="655dd-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="655dd-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="655dd-114">-ExpiryTime</span></span>
<span data-ttu-id="655dd-115">Anger den tid då den lagrade åtkomst policyn upphör att gälla.</span><span class="sxs-lookup"><span data-stu-id="655dd-115">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="655dd-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="655dd-116">-NoExpiryTime</span></span>
<span data-ttu-id="655dd-117">Visar att åtkomst policyn inte har något utgångs datum.</span><span class="sxs-lookup"><span data-stu-id="655dd-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="655dd-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="655dd-118">-NoStartTime</span></span>
<span data-ttu-id="655dd-119">Anger att start tiden är inställd på $Null.</span><span class="sxs-lookup"><span data-stu-id="655dd-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="655dd-120">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="655dd-120">-Permission</span></span>
<span data-ttu-id="655dd-121">Anger nivån för offentlig åtkomst till den här lagrings tabellen.</span><span class="sxs-lookup"><span data-stu-id="655dd-121">Specifies the level of public access to this storage table.</span></span>

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

### <span data-ttu-id="655dd-122">-Princip</span><span class="sxs-lookup"><span data-stu-id="655dd-122">-Policy</span></span>
<span data-ttu-id="655dd-123">Anger en lagrad åtkomst princip som innehåller behörigheter för denna SAS-token.</span><span class="sxs-lookup"><span data-stu-id="655dd-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="655dd-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="655dd-124">-StartTime</span></span>
<span data-ttu-id="655dd-125">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="655dd-125">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="655dd-126">-Tabell</span><span class="sxs-lookup"><span data-stu-id="655dd-126">-Table</span></span>
<span data-ttu-id="655dd-127">Anger namnet på Azure Storage-tabellen.</span><span class="sxs-lookup"><span data-stu-id="655dd-127">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="655dd-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="655dd-128">-Confirm</span></span>
<span data-ttu-id="655dd-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="655dd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="655dd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="655dd-130">-WhatIf</span></span>
<span data-ttu-id="655dd-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="655dd-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="655dd-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="655dd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="655dd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="655dd-133">CommonParameters</span></span>
<span data-ttu-id="655dd-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="655dd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="655dd-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="655dd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="655dd-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="655dd-136">INPUTS</span></span>

## <span data-ttu-id="655dd-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="655dd-137">OUTPUTS</span></span>

## <span data-ttu-id="655dd-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="655dd-138">NOTES</span></span>

## <span data-ttu-id="655dd-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="655dd-139">RELATED LINKS</span></span>

[<span data-ttu-id="655dd-140">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="655dd-140">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="655dd-141">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="655dd-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="655dd-142">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="655dd-142">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="655dd-143">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="655dd-143">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
