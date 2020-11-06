---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
ms.openlocfilehash: 116dcc8967ab18d0b67cd3e4eeea91190c38930f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572256"
---
# <span data-ttu-id="544d2-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="544d2-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="544d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="544d2-102">SYNOPSIS</span></span>
<span data-ttu-id="544d2-103">Tar bort en lagrad åtkomst princip från en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="544d2-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="544d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="544d2-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="544d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="544d2-105">DESCRIPTION</span></span>
<span data-ttu-id="544d2-106">Cmdleten **Remove-AzureStorageQueueStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="544d2-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="544d2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="544d2-107">EXAMPLES</span></span>

### <span data-ttu-id="544d2-108">Exempel 1: ta bort en lagrad åtkomst princip från en lagrings kö</span><span class="sxs-lookup"><span data-stu-id="544d2-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="544d2-109">Det här kommandot tar bort en åtkomst princip med namnet Policy04 från lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="544d2-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="544d2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="544d2-110">PARAMETERS</span></span>

### <span data-ttu-id="544d2-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="544d2-111">-Context</span></span>
<span data-ttu-id="544d2-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="544d2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="544d2-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="544d2-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="544d2-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="544d2-114">-PassThru</span></span>
<span data-ttu-id="544d2-115">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="544d2-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="544d2-116">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="544d2-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="544d2-117">-Princip</span><span class="sxs-lookup"><span data-stu-id="544d2-117">-Policy</span></span>
<span data-ttu-id="544d2-118">Anger den lagrade åtkomst principen, som innehåller behörigheter för denna delade Access-signatur (SAS).</span><span class="sxs-lookup"><span data-stu-id="544d2-118">Specifies the stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="544d2-119">-Kö</span><span class="sxs-lookup"><span data-stu-id="544d2-119">-Queue</span></span>
<span data-ttu-id="544d2-120">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="544d2-120">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="544d2-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="544d2-121">-Confirm</span></span>
<span data-ttu-id="544d2-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="544d2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="544d2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="544d2-123">-WhatIf</span></span>
<span data-ttu-id="544d2-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="544d2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="544d2-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="544d2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="544d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="544d2-126">CommonParameters</span></span>
<span data-ttu-id="544d2-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="544d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="544d2-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="544d2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="544d2-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="544d2-129">INPUTS</span></span>

## <span data-ttu-id="544d2-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="544d2-130">OUTPUTS</span></span>

## <span data-ttu-id="544d2-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="544d2-131">NOTES</span></span>

## <span data-ttu-id="544d2-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="544d2-132">RELATED LINKS</span></span>

[<span data-ttu-id="544d2-133">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="544d2-133">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="544d2-134">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="544d2-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="544d2-135">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="544d2-135">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="544d2-136">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="544d2-136">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
