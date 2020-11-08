---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2cc10a1b72dc369aef08b84e7b8fe2128ff0ac33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259783"
---
# <span data-ttu-id="527fe-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="527fe-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="527fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="527fe-102">SYNOPSIS</span></span>
<span data-ttu-id="527fe-103">Tar bort en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="527fe-103">Removes a storage queue.</span></span>

## <span data-ttu-id="527fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="527fe-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="527fe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="527fe-105">DESCRIPTION</span></span>
<span data-ttu-id="527fe-106">Cmdleten **Remove-AzStorageQueue** tar bort en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="527fe-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="527fe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="527fe-107">EXAMPLES</span></span>

### <span data-ttu-id="527fe-108">Exempel 1: ta bort en lagrings kö efter namn</span><span class="sxs-lookup"><span data-stu-id="527fe-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="527fe-109">Det här kommandot tar bort en kö som heter ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="527fe-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="527fe-110">Exempel 2: ta bort flera lagrings köer</span><span class="sxs-lookup"><span data-stu-id="527fe-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="527fe-111">Det här kommandot tar bort alla köer med namn som börjar med contoso.</span><span class="sxs-lookup"><span data-stu-id="527fe-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="527fe-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="527fe-112">PARAMETERS</span></span>

### <span data-ttu-id="527fe-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="527fe-113">-Context</span></span>
<span data-ttu-id="527fe-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="527fe-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="527fe-115">New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="527fe-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="527fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="527fe-116">-DefaultProfile</span></span>
<span data-ttu-id="527fe-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="527fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="527fe-118">-Force</span><span class="sxs-lookup"><span data-stu-id="527fe-118">-Force</span></span>
<span data-ttu-id="527fe-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="527fe-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="527fe-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="527fe-120">-Name</span></span>
<span data-ttu-id="527fe-121">Anger namnet på den kö som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="527fe-121">Specifies the name of the queue to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="527fe-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="527fe-122">-PassThru</span></span>
<span data-ttu-id="527fe-123">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="527fe-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="527fe-124">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="527fe-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="527fe-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="527fe-125">-Confirm</span></span>
<span data-ttu-id="527fe-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="527fe-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527fe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="527fe-127">-WhatIf</span></span>
<span data-ttu-id="527fe-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="527fe-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="527fe-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="527fe-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527fe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="527fe-130">CommonParameters</span></span>
<span data-ttu-id="527fe-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="527fe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="527fe-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="527fe-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="527fe-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="527fe-133">INPUTS</span></span>

### <span data-ttu-id="527fe-134">System. String</span><span class="sxs-lookup"><span data-stu-id="527fe-134">System.String</span></span>

### <span data-ttu-id="527fe-135">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="527fe-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="527fe-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="527fe-136">OUTPUTS</span></span>

### <span data-ttu-id="527fe-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="527fe-137">System.Boolean</span></span>

## <span data-ttu-id="527fe-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="527fe-138">NOTES</span></span>

## <span data-ttu-id="527fe-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="527fe-139">RELATED LINKS</span></span>

[<span data-ttu-id="527fe-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="527fe-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="527fe-141">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="527fe-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
