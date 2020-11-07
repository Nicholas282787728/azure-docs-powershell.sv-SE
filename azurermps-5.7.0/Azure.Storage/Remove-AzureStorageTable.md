---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
ms.openlocfilehash: 7423cbb6995430523beb137ef10eb6f1a53c959c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756299"
---
# <span data-ttu-id="d16a9-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d16a9-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="d16a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d16a9-102">SYNOPSIS</span></span>
<span data-ttu-id="d16a9-103">Tar bort en lagrings tabell.</span><span class="sxs-lookup"><span data-stu-id="d16a9-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d16a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d16a9-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d16a9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d16a9-105">DESCRIPTION</span></span>
<span data-ttu-id="d16a9-106">Cmdleten **Remove-AzureStorageTable** tar bort en eller flera lagrings tabeller från ett lagrings konto i Azure.</span><span class="sxs-lookup"><span data-stu-id="d16a9-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="d16a9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d16a9-107">EXAMPLES</span></span>

### <span data-ttu-id="d16a9-108">Exempel 1: ta bort en tabell</span><span class="sxs-lookup"><span data-stu-id="d16a9-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="d16a9-109">Det här kommandot tar bort en tabell.</span><span class="sxs-lookup"><span data-stu-id="d16a9-109">This command removes a table.</span></span>

### <span data-ttu-id="d16a9-110">Exempel 2: ta bort flera tabeller</span><span class="sxs-lookup"><span data-stu-id="d16a9-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="d16a9-111">I det här exemplet används ett jokertecken med parametern *Name* för att hämta alla tabeller som matchar tabellen mönster och sedan skickas resultatet i pipeline för att ta bort tabellerna.</span><span class="sxs-lookup"><span data-stu-id="d16a9-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="d16a9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d16a9-112">PARAMETERS</span></span>

### <span data-ttu-id="d16a9-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d16a9-113">-Context</span></span>
<span data-ttu-id="d16a9-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="d16a9-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d16a9-115">Du kan skapa det med hjälp av New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d16a9-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d16a9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d16a9-116">-Force</span></span>
<span data-ttu-id="d16a9-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d16a9-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d16a9-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d16a9-118">-Name</span></span>
<span data-ttu-id="d16a9-119">Anger namnet på tabellen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d16a9-119">Specifies the name of the table to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d16a9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d16a9-120">-PassThru</span></span>
<span data-ttu-id="d16a9-121">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="d16a9-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="d16a9-122">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="d16a9-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d16a9-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d16a9-123">-Confirm</span></span>
<span data-ttu-id="d16a9-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d16a9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d16a9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d16a9-125">-WhatIf</span></span>
<span data-ttu-id="d16a9-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d16a9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d16a9-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d16a9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d16a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d16a9-128">CommonParameters</span></span>
<span data-ttu-id="d16a9-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d16a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d16a9-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d16a9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d16a9-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d16a9-131">INPUTS</span></span>

### <span data-ttu-id="d16a9-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d16a9-132">IStorageContext</span></span>

<span data-ttu-id="d16a9-133">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d16a9-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="d16a9-134">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="d16a9-134">String</span></span>

<span data-ttu-id="d16a9-135">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="d16a9-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d16a9-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d16a9-136">OUTPUTS</span></span>

### <span data-ttu-id="d16a9-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d16a9-137">System.Boolean</span></span>

## <span data-ttu-id="d16a9-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d16a9-138">NOTES</span></span>

## <span data-ttu-id="d16a9-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d16a9-139">RELATED LINKS</span></span>

[<span data-ttu-id="d16a9-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d16a9-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
