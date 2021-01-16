---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402792"
---
# <span data-ttu-id="3176a-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3176a-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="3176a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3176a-102">SYNOPSIS</span></span>
<span data-ttu-id="3176a-103">Flyttar eller byter namn på en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3176a-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3176a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3176a-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3176a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3176a-105">DESCRIPTION</span></span>
<span data-ttu-id="3176a-106">Cmdleten **Move-AzDataLakeStoreItem** flyttar eller byter namn på en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3176a-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3176a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3176a-107">EXAMPLES</span></span>

### <span data-ttu-id="3176a-108">Exempel 1: flytta och byta namn på ett objekt</span><span class="sxs-lookup"><span data-stu-id="3176a-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="3176a-109">Det här kommandot byter namn på objektet File.txt till RenamedFile.txt och flyttar det till en annan mapp.</span><span class="sxs-lookup"><span data-stu-id="3176a-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="3176a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3176a-110">PARAMETERS</span></span>

### <span data-ttu-id="3176a-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="3176a-111">-Account</span></span>
<span data-ttu-id="3176a-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="3176a-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3176a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3176a-113">-DefaultProfile</span></span>
<span data-ttu-id="3176a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3176a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3176a-115">-Mål</span><span class="sxs-lookup"><span data-stu-id="3176a-115">-Destination</span></span>
<span data-ttu-id="3176a-116">Anger sökvägen till data Lake Store dit objektet ska flyttas, med början med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="3176a-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="3176a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3176a-117">-Force</span></span>
<span data-ttu-id="3176a-118">Anger att den här åtgärden kan skriva över målfilen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="3176a-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="3176a-119">-Path</span><span class="sxs-lookup"><span data-stu-id="3176a-119">-Path</span></span>
<span data-ttu-id="3176a-120">Anger data Lake Store-sökvägen för det objekt som ska flyttas eller byta namn, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="3176a-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="3176a-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3176a-121">-Confirm</span></span>
<span data-ttu-id="3176a-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3176a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3176a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3176a-123">-WhatIf</span></span>
<span data-ttu-id="3176a-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3176a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3176a-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3176a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3176a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3176a-126">CommonParameters</span></span>
<span data-ttu-id="3176a-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3176a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3176a-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3176a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3176a-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3176a-129">INPUTS</span></span>

### <span data-ttu-id="3176a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3176a-130">System.String</span></span>

### <span data-ttu-id="3176a-131">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="3176a-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="3176a-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3176a-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3176a-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3176a-133">OUTPUTS</span></span>

### <span data-ttu-id="3176a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3176a-134">System.String</span></span>

## <span data-ttu-id="3176a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3176a-135">NOTES</span></span>

## <span data-ttu-id="3176a-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3176a-136">RELATED LINKS</span></span>

[<span data-ttu-id="3176a-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3176a-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="3176a-138">Exportera-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3176a-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="3176a-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3176a-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="3176a-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3176a-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="3176a-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3176a-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="3176a-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3176a-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


