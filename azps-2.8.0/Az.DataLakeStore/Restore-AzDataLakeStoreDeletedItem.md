---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 7df59f75200bbc0d52c595c263228d7bf9801486
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744535"
---
# <span data-ttu-id="462a8-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="462a8-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="462a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="462a8-102">SYNOPSIS</span></span>
<span data-ttu-id="462a8-103">Återställa en borttagen fil eller mapp i Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="462a8-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="462a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="462a8-104">SYNTAX</span></span>

### <span data-ttu-id="462a8-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="462a8-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="462a8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="462a8-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="462a8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="462a8-107">DESCRIPTION</span></span>
<span data-ttu-id="462a8-108">Cmdleten **restore-AzDataLakeStoreDeletedItem** återställer en borttagen fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="462a8-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="462a8-109">Kräver att sökvägen till borttaget objekt i pappers korgen returneras av Get-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="462a8-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>

## <span data-ttu-id="462a8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="462a8-110">EXAMPLES</span></span>

### <span data-ttu-id="462a8-111">Exempel 1: återställa en fil från alternativet Använd-Force för data Lake Store</span><span class="sxs-lookup"><span data-stu-id="462a8-111">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="462a8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="462a8-112">PARAMETERS</span></span>

### <span data-ttu-id="462a8-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="462a8-113">-Account</span></span>
<span data-ttu-id="462a8-114">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="462a8-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="462a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="462a8-115">-DefaultProfile</span></span>
<span data-ttu-id="462a8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="462a8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="462a8-117">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="462a8-117">-DeletedItem</span></span>
<span data-ttu-id="462a8-118">Objektet borttaget.</span><span class="sxs-lookup"><span data-stu-id="462a8-118">The deleted item object.</span></span>

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

### <span data-ttu-id="462a8-119">-Mål</span><span class="sxs-lookup"><span data-stu-id="462a8-119">-Destination</span></span>
<span data-ttu-id="462a8-120">Mål Sök vägen dit den borttagna filen eller mappen ska återställas.</span><span class="sxs-lookup"><span data-stu-id="462a8-120">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="462a8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="462a8-121">-Force</span></span>
<span data-ttu-id="462a8-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="462a8-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="462a8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="462a8-123">-PassThru</span></span>
<span data-ttu-id="462a8-124">Returnerar boolesk sant vid framgång.</span><span class="sxs-lookup"><span data-stu-id="462a8-124">Return boolean true on success.</span></span>

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

### <span data-ttu-id="462a8-125">-Path</span><span class="sxs-lookup"><span data-stu-id="462a8-125">-Path</span></span>
<span data-ttu-id="462a8-126">Sökvägen till den borttagna filen eller mappen i pappers korgen.</span><span class="sxs-lookup"><span data-stu-id="462a8-126">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="462a8-127">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="462a8-127">-RestoreAction</span></span>
<span data-ttu-id="462a8-128">Åtgärd att vidta för mål namn konflikter – "Kopiera" eller "överskrivning"</span><span class="sxs-lookup"><span data-stu-id="462a8-128">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="462a8-129">– Skriv</span><span class="sxs-lookup"><span data-stu-id="462a8-129">-Type</span></span>
<span data-ttu-id="462a8-130">Den typ av post som återställs – "fil" eller "mapp"</span><span class="sxs-lookup"><span data-stu-id="462a8-130">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="462a8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="462a8-131">CommonParameters</span></span>
<span data-ttu-id="462a8-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="462a8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="462a8-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="462a8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="462a8-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="462a8-134">INPUTS</span></span>

### <span data-ttu-id="462a8-135">System. String</span><span class="sxs-lookup"><span data-stu-id="462a8-135">System.String</span></span>

## <span data-ttu-id="462a8-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="462a8-136">OUTPUTS</span></span>

### <span data-ttu-id="462a8-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="462a8-137">None</span></span>

## <span data-ttu-id="462a8-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="462a8-138">NOTES</span></span>

## <span data-ttu-id="462a8-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="462a8-139">RELATED LINKS</span></span>

[<span data-ttu-id="462a8-140">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="462a8-140">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)