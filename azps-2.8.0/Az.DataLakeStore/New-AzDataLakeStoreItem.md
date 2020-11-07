---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: 222df24f2d3db296ce116e49da8baeb3e22ec699
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744552"
---
# <span data-ttu-id="3c292-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3c292-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="3c292-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c292-102">SYNOPSIS</span></span>
<span data-ttu-id="3c292-103">Skapar en ny fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3c292-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3c292-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c292-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c292-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c292-105">DESCRIPTION</span></span>
<span data-ttu-id="3c292-106">Cmdleten **New-AzDataLakeStoreItem** skapar en ny fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3c292-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3c292-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c292-107">EXAMPLES</span></span>

### <span data-ttu-id="3c292-108">Exempel 1: skapa en ny fil och en ny mapp</span><span class="sxs-lookup"><span data-stu-id="3c292-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="3c292-109">Det första kommandot skapar filen NewFile.txt för det angivna kontot.</span><span class="sxs-lookup"><span data-stu-id="3c292-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="3c292-110">Det andra kommandot skapar mappen NewFolder i rotmappen.</span><span class="sxs-lookup"><span data-stu-id="3c292-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="3c292-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c292-111">PARAMETERS</span></span>

### <span data-ttu-id="3c292-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="3c292-112">-Account</span></span>
<span data-ttu-id="3c292-113">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="3c292-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3c292-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c292-114">-DefaultProfile</span></span>
<span data-ttu-id="3c292-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c292-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c292-116">-Kodning</span><span class="sxs-lookup"><span data-stu-id="3c292-116">-Encoding</span></span>
<span data-ttu-id="3c292-117">Anger kodningen för det objekt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3c292-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="3c292-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3c292-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3c292-119">Känd</span><span class="sxs-lookup"><span data-stu-id="3c292-119">Unknown</span></span>
- <span data-ttu-id="3c292-120">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="3c292-120">String</span></span>
- <span data-ttu-id="3c292-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="3c292-121">Unicode</span></span>
- <span data-ttu-id="3c292-122">SBCS</span><span class="sxs-lookup"><span data-stu-id="3c292-122">Byte</span></span>
- <span data-ttu-id="3c292-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="3c292-123">BigEndianUnicode</span></span>
- <span data-ttu-id="3c292-124">SKICKADE</span><span class="sxs-lookup"><span data-stu-id="3c292-124">UTF8</span></span>
- <span data-ttu-id="3c292-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="3c292-125">UTF7</span></span>
- <span data-ttu-id="3c292-126">Teckenuppsättning</span><span class="sxs-lookup"><span data-stu-id="3c292-126">Ascii</span></span>
- <span data-ttu-id="3c292-127">Vis</span><span class="sxs-lookup"><span data-stu-id="3c292-127">Default</span></span>
- <span data-ttu-id="3c292-128">Koms</span><span class="sxs-lookup"><span data-stu-id="3c292-128">Oem</span></span>
- <span data-ttu-id="3c292-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="3c292-129">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c292-130">-Mappen</span><span class="sxs-lookup"><span data-stu-id="3c292-130">-Folder</span></span>
<span data-ttu-id="3c292-131">Anger att den här åtgärden skapar en mapp.</span><span class="sxs-lookup"><span data-stu-id="3c292-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="3c292-132">-Force</span><span class="sxs-lookup"><span data-stu-id="3c292-132">-Force</span></span>
<span data-ttu-id="3c292-133">Anger att den här åtgärden kan skriva över målobjektet om det redan finns.</span><span class="sxs-lookup"><span data-stu-id="3c292-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="3c292-134">-Path</span><span class="sxs-lookup"><span data-stu-id="3c292-134">-Path</span></span>
<span data-ttu-id="3c292-135">Anger data Lake Store-sökvägen för det objekt som ska skapas, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="3c292-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="3c292-136">-Värde</span><span class="sxs-lookup"><span data-stu-id="3c292-136">-Value</span></span>
<span data-ttu-id="3c292-137">Anger vilket innehåll som ska läggas till i det objekt som du skapar.</span><span class="sxs-lookup"><span data-stu-id="3c292-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c292-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3c292-138">-Confirm</span></span>
<span data-ttu-id="3c292-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3c292-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c292-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c292-140">-WhatIf</span></span>
<span data-ttu-id="3c292-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3c292-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c292-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3c292-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c292-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c292-143">CommonParameters</span></span>
<span data-ttu-id="3c292-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c292-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c292-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c292-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c292-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c292-146">INPUTS</span></span>

### <span data-ttu-id="3c292-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3c292-147">System.String</span></span>

### <span data-ttu-id="3c292-148">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="3c292-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="3c292-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="3c292-149">System.Object</span></span>

### <span data-ttu-id="3c292-150">System. text. Encoding</span><span class="sxs-lookup"><span data-stu-id="3c292-150">System.Text.Encoding</span></span>

### <span data-ttu-id="3c292-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3c292-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3c292-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c292-152">OUTPUTS</span></span>

### <span data-ttu-id="3c292-153">System. String</span><span class="sxs-lookup"><span data-stu-id="3c292-153">System.String</span></span>

## <span data-ttu-id="3c292-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c292-154">NOTES</span></span>

## <span data-ttu-id="3c292-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c292-155">RELATED LINKS</span></span>

[<span data-ttu-id="3c292-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3c292-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="3c292-157">Exportera-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3c292-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="3c292-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3c292-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="3c292-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3c292-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="3c292-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3c292-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="3c292-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3c292-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)

