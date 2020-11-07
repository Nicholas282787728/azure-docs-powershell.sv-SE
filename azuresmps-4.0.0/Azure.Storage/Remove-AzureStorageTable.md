---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcb08eb9e63917d072630f81a2026d961a70dd27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754942"
---
# <span data-ttu-id="bda64-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="bda64-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="bda64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bda64-102">SYNOPSIS</span></span>
<span data-ttu-id="bda64-103">Tar bort en lagrings tabell.</span><span class="sxs-lookup"><span data-stu-id="bda64-103">Removes a storage table.</span></span>

## <span data-ttu-id="bda64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bda64-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bda64-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bda64-105">DESCRIPTION</span></span>
<span data-ttu-id="bda64-106">Cmdleten **Remove-AzureStorageTable** tar bort en eller flera lagrings tabeller från ett lagrings konto i Azure.</span><span class="sxs-lookup"><span data-stu-id="bda64-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="bda64-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bda64-107">EXAMPLES</span></span>

### <span data-ttu-id="bda64-108">Exempel 1: ta bort en tabell</span><span class="sxs-lookup"><span data-stu-id="bda64-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="bda64-109">Det här kommandot tar bort en tabell.</span><span class="sxs-lookup"><span data-stu-id="bda64-109">This command removes a table.</span></span>

### <span data-ttu-id="bda64-110">Exempel 2: ta bort flera tabeller</span><span class="sxs-lookup"><span data-stu-id="bda64-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="bda64-111">I det här exemplet används ett jokertecken med parametern *Name* för att hämta alla tabeller som matchar tabellen mönster och sedan skickas resultatet i pipeline för att ta bort tabellerna.</span><span class="sxs-lookup"><span data-stu-id="bda64-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="bda64-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bda64-112">PARAMETERS</span></span>

### <span data-ttu-id="bda64-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="bda64-113">-Context</span></span>
<span data-ttu-id="bda64-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="bda64-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="bda64-115">Du kan skapa det med hjälp av New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bda64-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bda64-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bda64-116">-Force</span></span>
<span data-ttu-id="bda64-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="bda64-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bda64-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="bda64-118">-Name</span></span>
<span data-ttu-id="bda64-119">Anger namnet på tabellen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="bda64-119">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="bda64-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bda64-120">-PassThru</span></span>
<span data-ttu-id="bda64-121">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="bda64-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="bda64-122">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="bda64-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="bda64-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bda64-123">-Confirm</span></span>
<span data-ttu-id="bda64-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bda64-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bda64-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bda64-125">-WhatIf</span></span>
<span data-ttu-id="bda64-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bda64-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bda64-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bda64-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bda64-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda64-128">CommonParameters</span></span>
<span data-ttu-id="bda64-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bda64-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda64-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bda64-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda64-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bda64-131">INPUTS</span></span>

## <span data-ttu-id="bda64-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bda64-132">OUTPUTS</span></span>

## <span data-ttu-id="bda64-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bda64-133">NOTES</span></span>

## <span data-ttu-id="bda64-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bda64-134">RELATED LINKS</span></span>

[<span data-ttu-id="bda64-135">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="bda64-135">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
