---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 51ea3111b5010b0e29f7bfd69ed5a8e66e596113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575065"
---
# <span data-ttu-id="490bf-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="490bf-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="490bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="490bf-102">SYNOPSIS</span></span>
<span data-ttu-id="490bf-103">Tar bort en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="490bf-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="490bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="490bf-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="490bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="490bf-105">DESCRIPTION</span></span>
<span data-ttu-id="490bf-106">Cmdleten **Remove-AzureStorageQueue** tar bort en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="490bf-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="490bf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="490bf-107">EXAMPLES</span></span>

### <span data-ttu-id="490bf-108">Exempel 1: ta bort en lagrings kö efter namn</span><span class="sxs-lookup"><span data-stu-id="490bf-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="490bf-109">Det här kommandot tar bort en kö som heter ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="490bf-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="490bf-110">Exempel 2: ta bort flera lagrings köer</span><span class="sxs-lookup"><span data-stu-id="490bf-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="490bf-111">Det här kommandot tar bort alla köer med namn som börjar med contoso.</span><span class="sxs-lookup"><span data-stu-id="490bf-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="490bf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="490bf-112">PARAMETERS</span></span>

### <span data-ttu-id="490bf-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="490bf-113">-Context</span></span>
<span data-ttu-id="490bf-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="490bf-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="490bf-115">New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="490bf-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="490bf-116">-Force</span><span class="sxs-lookup"><span data-stu-id="490bf-116">-Force</span></span>
<span data-ttu-id="490bf-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="490bf-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="490bf-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="490bf-118">-Name</span></span>
<span data-ttu-id="490bf-119">Anger namnet på den kö som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="490bf-119">Specifies the name of the queue to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="490bf-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="490bf-120">-PassThru</span></span>
<span data-ttu-id="490bf-121">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="490bf-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="490bf-122">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="490bf-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="490bf-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="490bf-123">-Confirm</span></span>
<span data-ttu-id="490bf-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="490bf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="490bf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="490bf-125">-WhatIf</span></span>
<span data-ttu-id="490bf-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="490bf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="490bf-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="490bf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="490bf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="490bf-128">CommonParameters</span></span>
<span data-ttu-id="490bf-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="490bf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="490bf-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="490bf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="490bf-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="490bf-131">INPUTS</span></span>

### <span data-ttu-id="490bf-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="490bf-132">IStorageContext</span></span>

<span data-ttu-id="490bf-133">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="490bf-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="490bf-134">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="490bf-134">String</span></span>

<span data-ttu-id="490bf-135">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="490bf-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="490bf-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="490bf-136">OUTPUTS</span></span>

### <span data-ttu-id="490bf-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="490bf-137">System.Boolean</span></span>

## <span data-ttu-id="490bf-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="490bf-138">NOTES</span></span>

## <span data-ttu-id="490bf-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="490bf-139">RELATED LINKS</span></span>

[<span data-ttu-id="490bf-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="490bf-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="490bf-141">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="490bf-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
