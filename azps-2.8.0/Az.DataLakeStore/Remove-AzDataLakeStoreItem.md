---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: 1ad6fbd77bc827b1cccd3074198182489186d06b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744549"
---
# <span data-ttu-id="cdb31-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cdb31-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="cdb31-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cdb31-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb31-103">Tar bort en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cdb31-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="cdb31-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cdb31-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdb31-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cdb31-105">DESCRIPTION</span></span>
<span data-ttu-id="cdb31-106">Cmdleten **Remove-AzDataLakeStoreItem** tar bort en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cdb31-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="cdb31-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cdb31-107">EXAMPLES</span></span>

### <span data-ttu-id="cdb31-108">Exempel 1: ta bort flera objekt</span><span class="sxs-lookup"><span data-stu-id="cdb31-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="cdb31-109">Det här kommandot tar bort filerna File01.txt och File.csv från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cdb31-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="cdb31-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cdb31-110">PARAMETERS</span></span>

### <span data-ttu-id="cdb31-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="cdb31-111">-Account</span></span>
<span data-ttu-id="cdb31-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="cdb31-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="cdb31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb31-113">-DefaultProfile</span></span>
<span data-ttu-id="cdb31-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb31-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdb31-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cdb31-115">-Force</span></span>
<span data-ttu-id="cdb31-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cdb31-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cdb31-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdb31-117">-PassThru</span></span>
<span data-ttu-id="cdb31-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="cdb31-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cdb31-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="cdb31-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cdb31-120">-Banor</span><span class="sxs-lookup"><span data-stu-id="cdb31-120">-Paths</span></span>
<span data-ttu-id="cdb31-121">Anger en matris med data Lake Store-sökvägar för de filer som ska tas bort, från och med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="cdb31-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="cdb31-122">-Recurse</span><span class="sxs-lookup"><span data-stu-id="cdb31-122">-Recurse</span></span>
<span data-ttu-id="cdb31-123">Indikerar att den här åtgärden tar bort alla objekt i målmappen, inklusive undermappar.</span><span class="sxs-lookup"><span data-stu-id="cdb31-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

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

### <span data-ttu-id="cdb31-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cdb31-124">-Confirm</span></span>
<span data-ttu-id="cdb31-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cdb31-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdb31-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdb31-126">-WhatIf</span></span>
<span data-ttu-id="cdb31-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cdb31-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdb31-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cdb31-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdb31-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb31-129">CommonParameters</span></span>
<span data-ttu-id="cdb31-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdb31-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb31-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb31-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb31-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cdb31-132">INPUTS</span></span>

### <span data-ttu-id="cdb31-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cdb31-133">System.String</span></span>

### <span data-ttu-id="cdb31-134">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="cdb31-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="cdb31-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cdb31-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cdb31-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cdb31-136">OUTPUTS</span></span>

### <span data-ttu-id="cdb31-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdb31-137">System.Boolean</span></span>

## <span data-ttu-id="cdb31-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cdb31-138">NOTES</span></span>

## <span data-ttu-id="cdb31-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cdb31-139">RELATED LINKS</span></span>

[<span data-ttu-id="cdb31-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cdb31-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="cdb31-141">Exportera-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cdb31-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="cdb31-142">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cdb31-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="cdb31-143">Anslut-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cdb31-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="cdb31-144">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cdb31-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="cdb31-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cdb31-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


