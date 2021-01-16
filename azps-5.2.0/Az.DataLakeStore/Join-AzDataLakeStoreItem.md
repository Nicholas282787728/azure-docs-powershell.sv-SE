---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411443"
---
# <span data-ttu-id="d961b-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d961b-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="d961b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d961b-102">SYNOPSIS</span></span>
<span data-ttu-id="d961b-103">Ansluter en eller flera filer för att skapa en fil i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d961b-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="d961b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d961b-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d961b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d961b-105">DESCRIPTION</span></span>
<span data-ttu-id="d961b-106">Cmdleten **Join-AzDataLakeStoreItem** ansluter till en eller flera filer för att skapa en fil i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d961b-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="d961b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d961b-107">EXAMPLES</span></span>

### <span data-ttu-id="d961b-108">Exempel 1: koppla ihop två objekt</span><span class="sxs-lookup"><span data-stu-id="d961b-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="d961b-109">Det här kommandot ansluter File01.txt och File02.txt för att skapa filen CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="d961b-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="d961b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d961b-110">PARAMETERS</span></span>

### <span data-ttu-id="d961b-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="d961b-111">-Account</span></span>
<span data-ttu-id="d961b-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="d961b-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d961b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d961b-113">-DefaultProfile</span></span>
<span data-ttu-id="d961b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d961b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d961b-115">-Mål</span><span class="sxs-lookup"><span data-stu-id="d961b-115">-Destination</span></span>
<span data-ttu-id="d961b-116">Anger sökvägen till data Lake Store för det kopplade objektet, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="d961b-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d961b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d961b-117">-Force</span></span>
<span data-ttu-id="d961b-118">Anger att den här åtgärden kan skriva över målfilen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="d961b-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="d961b-119">-Banor</span><span class="sxs-lookup"><span data-stu-id="d961b-119">-Paths</span></span>
<span data-ttu-id="d961b-120">Anger en matris med data Lake Store-sökvägar för de filer som ska kombineras, från och med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="d961b-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d961b-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d961b-121">-Confirm</span></span>
<span data-ttu-id="d961b-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d961b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d961b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d961b-123">-WhatIf</span></span>
<span data-ttu-id="d961b-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d961b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d961b-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d961b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d961b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d961b-126">CommonParameters</span></span>
<span data-ttu-id="d961b-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d961b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d961b-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d961b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d961b-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d961b-129">INPUTS</span></span>

### <span data-ttu-id="d961b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d961b-130">System.String</span></span>

### <span data-ttu-id="d961b-131">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="d961b-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="d961b-132">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d961b-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d961b-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d961b-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d961b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d961b-134">OUTPUTS</span></span>

### <span data-ttu-id="d961b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d961b-135">System.String</span></span>

## <span data-ttu-id="d961b-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d961b-136">NOTES</span></span>

## <span data-ttu-id="d961b-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d961b-137">RELATED LINKS</span></span>

[<span data-ttu-id="d961b-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d961b-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="d961b-139">Exportera-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d961b-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="d961b-140">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d961b-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="d961b-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d961b-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="d961b-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d961b-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="d961b-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d961b-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


