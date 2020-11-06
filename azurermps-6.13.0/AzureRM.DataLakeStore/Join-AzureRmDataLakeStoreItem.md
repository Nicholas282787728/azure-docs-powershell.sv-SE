---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/join-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 6e2a0e21f071f9496cce03f07a9b5c68da405e85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575221"
---
# <span data-ttu-id="2d46f-101">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2d46f-101">Join-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="2d46f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d46f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d46f-103">Ansluter en eller flera filer för att skapa en fil i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d46f-103">Joins one or more files to create one file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d46f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d46f-104">SYNTAX</span></span>

```
Join-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d46f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d46f-105">DESCRIPTION</span></span>
<span data-ttu-id="2d46f-106">Cmdleten **Join-AzureRmDataLakeStoreItem** ansluter till en eller flera filer för att skapa en fil i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d46f-106">The **Join-AzureRmDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="2d46f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d46f-107">EXAMPLES</span></span>

### <span data-ttu-id="2d46f-108">Exempel 1: koppla ihop två objekt</span><span class="sxs-lookup"><span data-stu-id="2d46f-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="2d46f-109">Det här kommandot ansluter File01.txt och File02.txt för att skapa filen CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="2d46f-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="2d46f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d46f-110">PARAMETERS</span></span>

### <span data-ttu-id="2d46f-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="2d46f-111">-Account</span></span>
<span data-ttu-id="2d46f-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="2d46f-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2d46f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d46f-113">-DefaultProfile</span></span>
<span data-ttu-id="2d46f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2d46f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d46f-115">-Mål</span><span class="sxs-lookup"><span data-stu-id="2d46f-115">-Destination</span></span>
<span data-ttu-id="2d46f-116">Anger sökvägen till data Lake Store för det kopplade objektet, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="2d46f-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2d46f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2d46f-117">-Force</span></span>
<span data-ttu-id="2d46f-118">Anger att den här åtgärden kan skriva över målfilen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="2d46f-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="2d46f-119">-Banor</span><span class="sxs-lookup"><span data-stu-id="2d46f-119">-Paths</span></span>
<span data-ttu-id="2d46f-120">Anger en matris med data Lake Store-sökvägar för de filer som ska kombineras, från och med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="2d46f-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2d46f-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2d46f-121">-Confirm</span></span>
<span data-ttu-id="2d46f-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2d46f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d46f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d46f-123">-WhatIf</span></span>
<span data-ttu-id="2d46f-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2d46f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d46f-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2d46f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d46f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d46f-126">CommonParameters</span></span>
<span data-ttu-id="2d46f-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d46f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d46f-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d46f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d46f-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d46f-129">INPUTS</span></span>

### <span data-ttu-id="2d46f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2d46f-130">System.String</span></span>

### <span data-ttu-id="2d46f-131">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="2d46f-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="2d46f-132">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2d46f-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="2d46f-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2d46f-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2d46f-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d46f-134">OUTPUTS</span></span>

### <span data-ttu-id="2d46f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2d46f-135">System.String</span></span>
<span data-ttu-id="2d46f-136">Den fullständiga sökvägen till den resulterande filen från kopplade filer.</span><span class="sxs-lookup"><span data-stu-id="2d46f-136">The full path to the resulting file from the joined files.</span></span>

## <span data-ttu-id="2d46f-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d46f-137">NOTES</span></span>

## <span data-ttu-id="2d46f-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d46f-138">RELATED LINKS</span></span>

[<span data-ttu-id="2d46f-139">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2d46f-139">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2d46f-140">Exportera-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2d46f-140">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2d46f-141">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2d46f-141">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2d46f-142">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2d46f-142">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2d46f-143">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2d46f-143">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2d46f-144">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2d46f-144">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


