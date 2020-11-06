---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3276a23869633238ebc6b84dfa01934e5ad9896
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571572"
---
# <span data-ttu-id="a4414-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a4414-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="a4414-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4414-102">SYNOPSIS</span></span>
<span data-ttu-id="a4414-103">Tar bort en lagrad åtkomst princip från en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="a4414-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="a4414-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4414-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4414-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4414-105">DESCRIPTION</span></span>
<span data-ttu-id="a4414-106">Cmdleten **Remove-AzureStorageTableStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="a4414-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="a4414-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4414-107">EXAMPLES</span></span>

### <span data-ttu-id="a4414-108">Exempel 1: ta bort en lagrad åtkomst princip från en lagrings tabell</span><span class="sxs-lookup"><span data-stu-id="a4414-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="a4414-109">Det här kommandot tar bort principen med namnet Policy05 från lagrings tabellen tabell.</span><span class="sxs-lookup"><span data-stu-id="a4414-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="a4414-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4414-110">PARAMETERS</span></span>

### <span data-ttu-id="a4414-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="a4414-111">-Context</span></span>
<span data-ttu-id="a4414-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="a4414-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a4414-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="a4414-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a4414-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4414-114">-PassThru</span></span>
<span data-ttu-id="a4414-115">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="a4414-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a4414-116">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="a4414-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a4414-117">-Princip</span><span class="sxs-lookup"><span data-stu-id="a4414-117">-Policy</span></span>
<span data-ttu-id="a4414-118">Anger den lagrade åtkomst principen, som innehåller behörigheter för denna SAS-token.</span><span class="sxs-lookup"><span data-stu-id="a4414-118">Specifies the stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4414-119">-Tabell</span><span class="sxs-lookup"><span data-stu-id="a4414-119">-Table</span></span>
<span data-ttu-id="a4414-120">Anger namnet på Azure-tabellen.</span><span class="sxs-lookup"><span data-stu-id="a4414-120">Specifies the Azure table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4414-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4414-121">-Confirm</span></span>
<span data-ttu-id="a4414-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4414-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4414-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4414-123">-WhatIf</span></span>
<span data-ttu-id="a4414-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4414-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4414-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4414-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4414-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4414-126">CommonParameters</span></span>
<span data-ttu-id="a4414-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4414-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4414-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4414-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4414-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4414-129">INPUTS</span></span>

## <span data-ttu-id="a4414-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4414-130">OUTPUTS</span></span>

## <span data-ttu-id="a4414-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4414-131">NOTES</span></span>

## <span data-ttu-id="a4414-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4414-132">RELATED LINKS</span></span>

[<span data-ttu-id="a4414-133">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a4414-133">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a4414-134">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a4414-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a4414-135">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a4414-135">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a4414-136">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a4414-136">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
