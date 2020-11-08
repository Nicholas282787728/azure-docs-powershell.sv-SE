---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: 5f927bd9ef64cc22eda7669e9b0d60127cf503ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262303"
---
# <span data-ttu-id="005ce-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="005ce-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="005ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="005ce-102">SYNOPSIS</span></span>
<span data-ttu-id="005ce-103">Tar bort en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="005ce-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="005ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="005ce-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="005ce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="005ce-105">DESCRIPTION</span></span>
<span data-ttu-id="005ce-106">Cmdleten **Remove-AzDataLakeStoreItem** tar bort en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="005ce-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="005ce-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="005ce-107">EXAMPLES</span></span>

### <span data-ttu-id="005ce-108">Exempel 1: ta bort flera objekt</span><span class="sxs-lookup"><span data-stu-id="005ce-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="005ce-109">Det här kommandot tar bort filerna File01.txt och File.csv från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="005ce-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="005ce-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="005ce-110">PARAMETERS</span></span>

### <span data-ttu-id="005ce-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="005ce-111">-Account</span></span>
<span data-ttu-id="005ce-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="005ce-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="005ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="005ce-113">-DefaultProfile</span></span>
<span data-ttu-id="005ce-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="005ce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="005ce-115">-Force</span><span class="sxs-lookup"><span data-stu-id="005ce-115">-Force</span></span>
<span data-ttu-id="005ce-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="005ce-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="005ce-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="005ce-117">-PassThru</span></span>
<span data-ttu-id="005ce-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="005ce-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="005ce-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="005ce-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="005ce-120">-Banor</span><span class="sxs-lookup"><span data-stu-id="005ce-120">-Paths</span></span>
<span data-ttu-id="005ce-121">Anger en matris med data Lake Store-sökvägar för de filer som ska tas bort, från och med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="005ce-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="005ce-122">-Recurse</span><span class="sxs-lookup"><span data-stu-id="005ce-122">-Recurse</span></span>
<span data-ttu-id="005ce-123">Indikerar att den här åtgärden tar bort alla objekt i målmappen, inklusive undermappar.</span><span class="sxs-lookup"><span data-stu-id="005ce-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="005ce-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="005ce-124">-Confirm</span></span>
<span data-ttu-id="005ce-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="005ce-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="005ce-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="005ce-126">-WhatIf</span></span>
<span data-ttu-id="005ce-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="005ce-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="005ce-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="005ce-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="005ce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="005ce-129">CommonParameters</span></span>
<span data-ttu-id="005ce-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="005ce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="005ce-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="005ce-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="005ce-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="005ce-132">INPUTS</span></span>

### <span data-ttu-id="005ce-133">System. String</span><span class="sxs-lookup"><span data-stu-id="005ce-133">System.String</span></span>

### <span data-ttu-id="005ce-134">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="005ce-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="005ce-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="005ce-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="005ce-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="005ce-136">OUTPUTS</span></span>

### <span data-ttu-id="005ce-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="005ce-137">System.Boolean</span></span>

## <span data-ttu-id="005ce-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="005ce-138">NOTES</span></span>

## <span data-ttu-id="005ce-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="005ce-139">RELATED LINKS</span></span>

[<span data-ttu-id="005ce-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="005ce-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="005ce-141">Exportera-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="005ce-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="005ce-142">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="005ce-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="005ce-143">Anslut-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="005ce-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="005ce-144">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="005ce-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="005ce-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="005ce-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


