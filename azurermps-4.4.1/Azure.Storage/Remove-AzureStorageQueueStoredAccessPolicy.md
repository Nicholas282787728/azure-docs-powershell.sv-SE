---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 94c5bc28ae381227366b5461b51a2da7fd6feccd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578699"
---
# <span data-ttu-id="eb996-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb996-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="eb996-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb996-102">SYNOPSIS</span></span>
<span data-ttu-id="eb996-103">Tar bort en lagrad åtkomst princip från en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="eb996-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb996-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb996-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb996-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb996-105">DESCRIPTION</span></span>
<span data-ttu-id="eb996-106">Cmdleten **Remove-AzureStorageQueueStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="eb996-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="eb996-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb996-107">EXAMPLES</span></span>

### <span data-ttu-id="eb996-108">Exempel 1: ta bort en lagrad åtkomst princip från en lagrings kö</span><span class="sxs-lookup"><span data-stu-id="eb996-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="eb996-109">Det här kommandot tar bort en åtkomst princip med namnet Policy04 från lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="eb996-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="eb996-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb996-110">PARAMETERS</span></span>

### <span data-ttu-id="eb996-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="eb996-111">-Context</span></span>
<span data-ttu-id="eb996-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="eb996-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="eb996-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="eb996-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="eb996-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb996-114">-PassThru</span></span>
<span data-ttu-id="eb996-115">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="eb996-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="eb996-116">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="eb996-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="eb996-117">-Princip</span><span class="sxs-lookup"><span data-stu-id="eb996-117">-Policy</span></span>
<span data-ttu-id="eb996-118">Anger namnet på den lagrade åtkomst principen som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eb996-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eb996-119">-Kö</span><span class="sxs-lookup"><span data-stu-id="eb996-119">-Queue</span></span>
<span data-ttu-id="eb996-120">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="eb996-120">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="eb996-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eb996-121">-Confirm</span></span>
<span data-ttu-id="eb996-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eb996-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb996-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb996-123">-WhatIf</span></span>
<span data-ttu-id="eb996-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eb996-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb996-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eb996-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb996-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb996-126">CommonParameters</span></span>
<span data-ttu-id="eb996-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb996-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb996-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb996-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb996-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb996-129">INPUTS</span></span>

### <span data-ttu-id="eb996-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eb996-130">IStorageContext</span></span>

<span data-ttu-id="eb996-131">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="eb996-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="eb996-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb996-132">OUTPUTS</span></span>

### <span data-ttu-id="eb996-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb996-133">System.Boolean</span></span>

## <span data-ttu-id="eb996-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb996-134">NOTES</span></span>

## <span data-ttu-id="eb996-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb996-135">RELATED LINKS</span></span>

[<span data-ttu-id="eb996-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb996-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="eb996-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="eb996-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="eb996-138">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb996-138">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="eb996-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb996-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
