---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258850"
---
# <span data-ttu-id="2acf5-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2acf5-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="2acf5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2acf5-102">SYNOPSIS</span></span>
<span data-ttu-id="2acf5-103">Flyttar eller byter namn på en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2acf5-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2acf5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2acf5-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2acf5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2acf5-105">DESCRIPTION</span></span>
<span data-ttu-id="2acf5-106">Cmdleten **Move-AzDataLakeStoreItem** flyttar eller byter namn på en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2acf5-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2acf5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2acf5-107">EXAMPLES</span></span>

### <span data-ttu-id="2acf5-108">Exempel 1: flytta och byta namn på ett objekt</span><span class="sxs-lookup"><span data-stu-id="2acf5-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="2acf5-109">Det här kommandot byter namn på objektet File.txt till RenamedFile.txt och flyttar det till en annan mapp.</span><span class="sxs-lookup"><span data-stu-id="2acf5-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="2acf5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2acf5-110">PARAMETERS</span></span>

### <span data-ttu-id="2acf5-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="2acf5-111">-Account</span></span>
<span data-ttu-id="2acf5-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="2acf5-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2acf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2acf5-113">-DefaultProfile</span></span>
<span data-ttu-id="2acf5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2acf5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2acf5-115">-Mål</span><span class="sxs-lookup"><span data-stu-id="2acf5-115">-Destination</span></span>
<span data-ttu-id="2acf5-116">Anger sökvägen till data Lake Store dit objektet ska flyttas, med början med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="2acf5-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2acf5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2acf5-117">-Force</span></span>
<span data-ttu-id="2acf5-118">Anger att den här åtgärden kan skriva över målfilen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="2acf5-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="2acf5-119">-Path</span><span class="sxs-lookup"><span data-stu-id="2acf5-119">-Path</span></span>
<span data-ttu-id="2acf5-120">Anger data Lake Store-sökvägen för det objekt som ska flyttas eller byta namn, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="2acf5-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2acf5-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2acf5-121">-Confirm</span></span>
<span data-ttu-id="2acf5-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2acf5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2acf5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2acf5-123">-WhatIf</span></span>
<span data-ttu-id="2acf5-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2acf5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2acf5-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2acf5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2acf5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2acf5-126">CommonParameters</span></span>
<span data-ttu-id="2acf5-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2acf5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2acf5-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2acf5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2acf5-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2acf5-129">INPUTS</span></span>

### <span data-ttu-id="2acf5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2acf5-130">System.String</span></span>

### <span data-ttu-id="2acf5-131">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2acf5-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="2acf5-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2acf5-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2acf5-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2acf5-133">OUTPUTS</span></span>

### <span data-ttu-id="2acf5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2acf5-134">System.String</span></span>

## <span data-ttu-id="2acf5-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2acf5-135">NOTES</span></span>

## <span data-ttu-id="2acf5-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2acf5-136">RELATED LINKS</span></span>

[<span data-ttu-id="2acf5-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2acf5-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="2acf5-138">Exportera-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2acf5-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="2acf5-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2acf5-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="2acf5-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2acf5-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="2acf5-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2acf5-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="2acf5-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2acf5-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


