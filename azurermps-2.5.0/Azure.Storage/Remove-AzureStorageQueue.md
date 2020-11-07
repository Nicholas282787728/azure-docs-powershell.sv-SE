---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: e2fcfa1d100f460bcf352cc26fd0e094d52cad21
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929990"
---
# <span data-ttu-id="41db2-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="41db2-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="41db2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41db2-102">SYNOPSIS</span></span>
<span data-ttu-id="41db2-103">Tar bort en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="41db2-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41db2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41db2-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41db2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41db2-105">DESCRIPTION</span></span>
<span data-ttu-id="41db2-106">Cmdleten **Remove-AzureStorageQueue** tar bort en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="41db2-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="41db2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41db2-107">EXAMPLES</span></span>

### <span data-ttu-id="41db2-108">Exempel 1: ta bort en lagrings kö efter namn</span><span class="sxs-lookup"><span data-stu-id="41db2-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="41db2-109">Det här kommandot tar bort en kö som heter ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="41db2-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="41db2-110">Exempel 2: ta bort flera lagrings köer</span><span class="sxs-lookup"><span data-stu-id="41db2-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="41db2-111">Det här kommandot tar bort alla köer med namn som börjar med contoso.</span><span class="sxs-lookup"><span data-stu-id="41db2-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="41db2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41db2-112">PARAMETERS</span></span>

### <span data-ttu-id="41db2-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="41db2-113">-Context</span></span>
<span data-ttu-id="41db2-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="41db2-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="41db2-115">New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="41db2-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="41db2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41db2-116">-DefaultProfile</span></span>
<span data-ttu-id="41db2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="41db2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41db2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="41db2-118">-Force</span></span>
<span data-ttu-id="41db2-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="41db2-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="41db2-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="41db2-120">-Name</span></span>
<span data-ttu-id="41db2-121">Anger namnet på den kö som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="41db2-121">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="41db2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41db2-122">-PassThru</span></span>
<span data-ttu-id="41db2-123">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="41db2-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="41db2-124">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="41db2-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="41db2-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="41db2-125">-Confirm</span></span>
<span data-ttu-id="41db2-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="41db2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41db2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41db2-127">-WhatIf</span></span>
<span data-ttu-id="41db2-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="41db2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41db2-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="41db2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41db2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41db2-130">CommonParameters</span></span>
<span data-ttu-id="41db2-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41db2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41db2-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41db2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41db2-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41db2-133">INPUTS</span></span>

### <span data-ttu-id="41db2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="41db2-134">System.String</span></span>

### <span data-ttu-id="41db2-135">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="41db2-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="41db2-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41db2-136">OUTPUTS</span></span>

### <span data-ttu-id="41db2-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41db2-137">System.Boolean</span></span>

## <span data-ttu-id="41db2-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41db2-138">NOTES</span></span>

## <span data-ttu-id="41db2-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41db2-139">RELATED LINKS</span></span>

[<span data-ttu-id="41db2-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="41db2-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="41db2-141">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="41db2-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
