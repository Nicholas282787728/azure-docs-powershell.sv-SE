---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54770fd564addf30e7c4ed058776857b823903e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572263"
---
# <span data-ttu-id="8db8e-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8db8e-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="8db8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8db8e-102">SYNOPSIS</span></span>
<span data-ttu-id="8db8e-103">Tar bort en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="8db8e-103">Removes a storage queue.</span></span>

## <span data-ttu-id="8db8e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8db8e-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8db8e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8db8e-105">DESCRIPTION</span></span>
<span data-ttu-id="8db8e-106">Cmdleten **Remove-AzureStorageQueue** tar bort en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="8db8e-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="8db8e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8db8e-107">EXAMPLES</span></span>

### <span data-ttu-id="8db8e-108">Exempel 1: ta bort en lagrings kö efter namn</span><span class="sxs-lookup"><span data-stu-id="8db8e-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="8db8e-109">Det här kommandot tar bort en kö som heter ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="8db8e-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="8db8e-110">Exempel 2: ta bort flera lagrings köer</span><span class="sxs-lookup"><span data-stu-id="8db8e-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="8db8e-111">Det här kommandot tar bort alla köer med namn som börjar med contoso.</span><span class="sxs-lookup"><span data-stu-id="8db8e-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="8db8e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8db8e-112">PARAMETERS</span></span>

### <span data-ttu-id="8db8e-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="8db8e-113">-Context</span></span>
<span data-ttu-id="8db8e-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="8db8e-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="8db8e-115">New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="8db8e-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8db8e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8db8e-116">-Force</span></span>
<span data-ttu-id="8db8e-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8db8e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8db8e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="8db8e-118">-Name</span></span>
<span data-ttu-id="8db8e-119">Anger namnet på den kö som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8db8e-119">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="8db8e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8db8e-120">-PassThru</span></span>
<span data-ttu-id="8db8e-121">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="8db8e-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="8db8e-122">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="8db8e-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8db8e-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8db8e-123">-Confirm</span></span>
<span data-ttu-id="8db8e-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8db8e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8db8e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8db8e-125">-WhatIf</span></span>
<span data-ttu-id="8db8e-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8db8e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8db8e-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8db8e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8db8e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db8e-128">CommonParameters</span></span>
<span data-ttu-id="8db8e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8db8e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db8e-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8db8e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db8e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8db8e-131">INPUTS</span></span>

## <span data-ttu-id="8db8e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8db8e-132">OUTPUTS</span></span>

## <span data-ttu-id="8db8e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8db8e-133">NOTES</span></span>

## <span data-ttu-id="8db8e-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8db8e-134">RELATED LINKS</span></span>

[<span data-ttu-id="8db8e-135">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8db8e-135">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="8db8e-136">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8db8e-136">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
