---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: 8a8cc4d60bfba73b9cbcc9d323b063bff87f8a2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744554"
---
# <span data-ttu-id="74d15-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="74d15-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="74d15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74d15-102">SYNOPSIS</span></span>
<span data-ttu-id="74d15-103">Flyttar eller byter namn på en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="74d15-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="74d15-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74d15-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74d15-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74d15-105">DESCRIPTION</span></span>
<span data-ttu-id="74d15-106">Cmdleten **Move-AzDataLakeStoreItem** flyttar eller byter namn på en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="74d15-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="74d15-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74d15-107">EXAMPLES</span></span>

### <span data-ttu-id="74d15-108">Exempel 1: flytta och byta namn på ett objekt</span><span class="sxs-lookup"><span data-stu-id="74d15-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="74d15-109">Det här kommandot byter namn på objektet File.txt till RenamedFile.txt och flyttar det till en annan mapp.</span><span class="sxs-lookup"><span data-stu-id="74d15-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="74d15-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74d15-110">PARAMETERS</span></span>

### <span data-ttu-id="74d15-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="74d15-111">-Account</span></span>
<span data-ttu-id="74d15-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="74d15-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74d15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d15-113">-DefaultProfile</span></span>
<span data-ttu-id="74d15-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74d15-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d15-115">-Mål</span><span class="sxs-lookup"><span data-stu-id="74d15-115">-Destination</span></span>
<span data-ttu-id="74d15-116">Anger sökvägen till data Lake Store dit objektet ska flyttas, med början med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="74d15-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74d15-117">-Force</span><span class="sxs-lookup"><span data-stu-id="74d15-117">-Force</span></span>
<span data-ttu-id="74d15-118">Anger att den här åtgärden kan skriva över målfilen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="74d15-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74d15-119">-Path</span><span class="sxs-lookup"><span data-stu-id="74d15-119">-Path</span></span>
<span data-ttu-id="74d15-120">Anger data Lake Store-sökvägen för det objekt som ska flyttas eller byta namn, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="74d15-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74d15-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74d15-121">-Confirm</span></span>
<span data-ttu-id="74d15-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74d15-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74d15-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74d15-123">-WhatIf</span></span>
<span data-ttu-id="74d15-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74d15-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74d15-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74d15-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74d15-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d15-126">CommonParameters</span></span>
<span data-ttu-id="74d15-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d15-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d15-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74d15-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d15-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74d15-129">INPUTS</span></span>

### <span data-ttu-id="74d15-130">System. String</span><span class="sxs-lookup"><span data-stu-id="74d15-130">System.String</span></span>

### <span data-ttu-id="74d15-131">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="74d15-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="74d15-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="74d15-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="74d15-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74d15-133">OUTPUTS</span></span>

### <span data-ttu-id="74d15-134">System. String</span><span class="sxs-lookup"><span data-stu-id="74d15-134">System.String</span></span>

## <span data-ttu-id="74d15-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74d15-135">NOTES</span></span>

## <span data-ttu-id="74d15-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74d15-136">RELATED LINKS</span></span>

[<span data-ttu-id="74d15-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="74d15-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="74d15-138">Exportera-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="74d15-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="74d15-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="74d15-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="74d15-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="74d15-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="74d15-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="74d15-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="74d15-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="74d15-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


