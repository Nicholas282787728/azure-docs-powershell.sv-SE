---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: ab752ec2201c9b64a9656153f29a947b7a722819
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258846"
---
# <span data-ttu-id="1e5ac-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e5ac-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="1e5ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e5ac-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5ac-103">Skapar en ny fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1e5ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e5ac-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e5ac-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e5ac-105">DESCRIPTION</span></span>
<span data-ttu-id="1e5ac-106">Cmdleten **New-AzDataLakeStoreItem** skapar en ny fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1e5ac-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e5ac-107">EXAMPLES</span></span>

### <span data-ttu-id="1e5ac-108">Exempel 1: skapa en ny fil och en ny mapp</span><span class="sxs-lookup"><span data-stu-id="1e5ac-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="1e5ac-109">Det första kommandot skapar filen NewFile.txt för det angivna kontot.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="1e5ac-110">Det andra kommandot skapar mappen NewFolder i rotmappen.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="1e5ac-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e5ac-111">PARAMETERS</span></span>

### <span data-ttu-id="1e5ac-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="1e5ac-112">-Account</span></span>
<span data-ttu-id="1e5ac-113">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1e5ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e5ac-114">-DefaultProfile</span></span>
<span data-ttu-id="1e5ac-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e5ac-116">-Kodning</span><span class="sxs-lookup"><span data-stu-id="1e5ac-116">-Encoding</span></span>
<span data-ttu-id="1e5ac-117">Anger kodningen för det objekt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="1e5ac-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1e5ac-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1e5ac-119">Känd</span><span class="sxs-lookup"><span data-stu-id="1e5ac-119">Unknown</span></span>
- <span data-ttu-id="1e5ac-120">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="1e5ac-120">String</span></span>
- <span data-ttu-id="1e5ac-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="1e5ac-121">Unicode</span></span>
- <span data-ttu-id="1e5ac-122">SBCS</span><span class="sxs-lookup"><span data-stu-id="1e5ac-122">Byte</span></span>
- <span data-ttu-id="1e5ac-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="1e5ac-123">BigEndianUnicode</span></span>
- <span data-ttu-id="1e5ac-124">SKICKADE</span><span class="sxs-lookup"><span data-stu-id="1e5ac-124">UTF8</span></span>
- <span data-ttu-id="1e5ac-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="1e5ac-125">UTF7</span></span>
- <span data-ttu-id="1e5ac-126">Teckenuppsättning</span><span class="sxs-lookup"><span data-stu-id="1e5ac-126">Ascii</span></span>
- <span data-ttu-id="1e5ac-127">Vis</span><span class="sxs-lookup"><span data-stu-id="1e5ac-127">Default</span></span>
- <span data-ttu-id="1e5ac-128">Koms</span><span class="sxs-lookup"><span data-stu-id="1e5ac-128">Oem</span></span>
- <span data-ttu-id="1e5ac-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="1e5ac-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="1e5ac-130">-Mappen</span><span class="sxs-lookup"><span data-stu-id="1e5ac-130">-Folder</span></span>
<span data-ttu-id="1e5ac-131">Anger att den här åtgärden skapar en mapp.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="1e5ac-132">-Force</span><span class="sxs-lookup"><span data-stu-id="1e5ac-132">-Force</span></span>
<span data-ttu-id="1e5ac-133">Anger att den här åtgärden kan skriva över målobjektet om det redan finns.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="1e5ac-134">-Path</span><span class="sxs-lookup"><span data-stu-id="1e5ac-134">-Path</span></span>
<span data-ttu-id="1e5ac-135">Anger data Lake Store-sökvägen för det objekt som ska skapas, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="1e5ac-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1e5ac-136">-Värde</span><span class="sxs-lookup"><span data-stu-id="1e5ac-136">-Value</span></span>
<span data-ttu-id="1e5ac-137">Anger vilket innehåll som ska läggas till i det objekt som du skapar.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="1e5ac-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1e5ac-138">-Confirm</span></span>
<span data-ttu-id="1e5ac-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e5ac-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e5ac-140">-WhatIf</span></span>
<span data-ttu-id="1e5ac-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e5ac-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e5ac-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5ac-143">CommonParameters</span></span>
<span data-ttu-id="1e5ac-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5ac-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e5ac-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5ac-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e5ac-146">INPUTS</span></span>

### <span data-ttu-id="1e5ac-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1e5ac-147">System.String</span></span>

### <span data-ttu-id="1e5ac-148">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1e5ac-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1e5ac-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="1e5ac-149">System.Object</span></span>

### <span data-ttu-id="1e5ac-150">System. text. Encoding</span><span class="sxs-lookup"><span data-stu-id="1e5ac-150">System.Text.Encoding</span></span>

### <span data-ttu-id="1e5ac-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1e5ac-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1e5ac-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e5ac-152">OUTPUTS</span></span>

### <span data-ttu-id="1e5ac-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1e5ac-153">System.String</span></span>

## <span data-ttu-id="1e5ac-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e5ac-154">NOTES</span></span>

## <span data-ttu-id="1e5ac-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e5ac-155">RELATED LINKS</span></span>

[<span data-ttu-id="1e5ac-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e5ac-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="1e5ac-157">Exportera-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e5ac-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="1e5ac-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e5ac-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="1e5ac-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e5ac-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="1e5ac-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e5ac-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="1e5ac-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e5ac-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


