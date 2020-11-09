---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 9dcc45f8f082ce59a6082ad71c2084c5df10064c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320511"
---
# <span data-ttu-id="a5a3c-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="a5a3c-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="a5a3c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a3c-103">Återställa en borttagen fil eller mapp i Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="a5a3c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5a3c-104">SYNTAX</span></span>

### <span data-ttu-id="a5a3c-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="a5a3c-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5a3c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a5a3c-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5a3c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5a3c-107">DESCRIPTION</span></span>
<span data-ttu-id="a5a3c-108">Cmdleten **restore-AzDataLakeStoreDeletedItem** återställer en borttagen fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="a5a3c-109">Kräver att sökvägen till borttaget objekt i pappers korgen returneras av Get-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="a5a3c-110">Varning! det är en bra åtgärd att ta bort filer.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="a5a3c-111">Det finns inga garantier för att en fil kan återställas när den har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="a5a3c-112">Användningen av detta API aktive ras via väggar.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="a5a3c-113">Om ditt ADL-konto inte är whitelisted, följer detta API inte implementerat undantag.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="a5a3c-114">Om du vill ha mer information kontaktar du Microsoft support.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="a5a3c-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5a3c-115">EXAMPLES</span></span>

### <span data-ttu-id="a5a3c-116">Exempel 1: återställa en fil från alternativet Använd-Force för data Lake Store</span><span class="sxs-lookup"><span data-stu-id="a5a3c-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
```
PS > Restore-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -Destination adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 -Type "file" -Force
PS >

### Example 2: Restore a file from Data Lake Store using user confirmation

PS > restore-azdatalakestoredeleteditem -account ml1ptrashtest -path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -destination adl://ml1ptrashtest.azuredatalake.com/test4/file_1115 -type file

Restore user data ?
From - 927e8fb1-a287-4353-b50e-3b4a39ae4088
To   - adl://ml1ptrashtest.azuredatalake.com/test4/file_1115
Type - file
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
PS >
```

## <span data-ttu-id="a5a3c-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5a3c-117">PARAMETERS</span></span>

### <span data-ttu-id="a5a3c-118">-Konto</span><span class="sxs-lookup"><span data-stu-id="a5a3c-118">-Account</span></span>
<span data-ttu-id="a5a3c-119">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a5a3c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a3c-120">-DefaultProfile</span></span>
<span data-ttu-id="a5a3c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a3c-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="a5a3c-122">-DeletedItem</span></span>
<span data-ttu-id="a5a3c-123">Objektet borttaget.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-123">The deleted item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a3c-124">-Mål</span><span class="sxs-lookup"><span data-stu-id="a5a3c-124">-Destination</span></span>
<span data-ttu-id="a5a3c-125">Mål Sök vägen dit den borttagna filen eller mappen ska återställas.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-125">The destination path to where the deleted file or folder should be restored.</span></span> 

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a3c-126">-Force</span><span class="sxs-lookup"><span data-stu-id="a5a3c-126">-Force</span></span>
<span data-ttu-id="a5a3c-127">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-127">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a3c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5a3c-128">-PassThru</span></span>
<span data-ttu-id="a5a3c-129">Returnerar boolesk sant vid framgång.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-129">Return boolean true on success.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a3c-130">-Path</span><span class="sxs-lookup"><span data-stu-id="a5a3c-130">-Path</span></span>
<span data-ttu-id="a5a3c-131">Sökvägen till den borttagna filen eller mappen i pappers korgen.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-131">The path of the deleted file or folder in trash.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a3c-132">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="a5a3c-132">-RestoreAction</span></span>
<span data-ttu-id="a5a3c-133">Åtgärd att vidta för mål namn konflikter – "Kopiera" eller "överskrivning"</span><span class="sxs-lookup"><span data-stu-id="a5a3c-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a3c-134">– Skriv</span><span class="sxs-lookup"><span data-stu-id="a5a3c-134">-Type</span></span>
<span data-ttu-id="a5a3c-135">Den typ av post som återställs – "fil" eller "mapp"</span><span class="sxs-lookup"><span data-stu-id="a5a3c-135">The type of entry being restored - "file" or "folder"</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a3c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a3c-136">CommonParameters</span></span>
<span data-ttu-id="a5a3c-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a3c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a3c-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a3c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a3c-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5a3c-139">INPUTS</span></span>

### <span data-ttu-id="a5a3c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a5a3c-140">System.String</span></span>

## <span data-ttu-id="a5a3c-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5a3c-141">OUTPUTS</span></span>

### <span data-ttu-id="a5a3c-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="a5a3c-142">None</span></span>

## <span data-ttu-id="a5a3c-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5a3c-143">NOTES</span></span>

## <span data-ttu-id="a5a3c-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5a3c-144">RELATED LINKS</span></span>

[<span data-ttu-id="a5a3c-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="a5a3c-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)