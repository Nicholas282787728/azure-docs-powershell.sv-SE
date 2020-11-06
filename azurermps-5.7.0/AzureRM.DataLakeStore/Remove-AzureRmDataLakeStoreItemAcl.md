---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 23eb57a6c12c3ce5ba8334b7309b5c282624620a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573447"
---
# <span data-ttu-id="830f3-101">Remove-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="830f3-101">Remove-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="830f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="830f3-102">SYNOPSIS</span></span>
<span data-ttu-id="830f3-103">Rensar en ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="830f3-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="830f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="830f3-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="830f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="830f3-105">DESCRIPTION</span></span>
<span data-ttu-id="830f3-106">Cmdleten **Remove-AzureRmDataLakeStoreItemAcl** rensar åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="830f3-106">The **Remove-AzureRmDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="830f3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="830f3-107">EXAMPLES</span></span>

### <span data-ttu-id="830f3-108">Exempel 1: ta bort en ACL från en mapp</span><span class="sxs-lookup"><span data-stu-id="830f3-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="830f3-109">Det här kommandot tar bort ACL för rot katalogen för ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="830f3-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="830f3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="830f3-110">PARAMETERS</span></span>

### <span data-ttu-id="830f3-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="830f3-111">-Account</span></span>
<span data-ttu-id="830f3-112">Anger namnet på data Lake Store-butiken.</span><span class="sxs-lookup"><span data-stu-id="830f3-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="830f3-113">-Standard</span><span class="sxs-lookup"><span data-stu-id="830f3-113">-Default</span></span>
<span data-ttu-id="830f3-114">Anger att cmdleten tar bort standard åtkomst för en fil eller mapp.</span><span class="sxs-lookup"><span data-stu-id="830f3-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="830f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="830f3-115">-DefaultProfile</span></span>
<span data-ttu-id="830f3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="830f3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830f3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="830f3-117">-Force</span></span>
<span data-ttu-id="830f3-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="830f3-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="830f3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="830f3-119">-PassThru</span></span>
<span data-ttu-id="830f3-120">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="830f3-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="830f3-121">-Path</span><span class="sxs-lookup"><span data-stu-id="830f3-121">-Path</span></span>
<span data-ttu-id="830f3-122">Anger data Lake Store-sökvägen för objektet, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="830f3-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="830f3-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="830f3-123">-Confirm</span></span>
<span data-ttu-id="830f3-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="830f3-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830f3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="830f3-125">-WhatIf</span></span>
<span data-ttu-id="830f3-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="830f3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="830f3-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="830f3-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830f3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="830f3-128">CommonParameters</span></span>
<span data-ttu-id="830f3-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="830f3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="830f3-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="830f3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="830f3-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="830f3-131">INPUTS</span></span>

### <span data-ttu-id="830f3-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="830f3-132">None</span></span>
<span data-ttu-id="830f3-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="830f3-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="830f3-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="830f3-134">OUTPUTS</span></span>

### <span data-ttu-id="830f3-135">bool</span><span class="sxs-lookup"><span data-stu-id="830f3-135">bool</span></span>
<span data-ttu-id="830f3-136">Om PassThru är angivet returneras sant när du är klar.</span><span class="sxs-lookup"><span data-stu-id="830f3-136">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="830f3-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="830f3-137">NOTES</span></span>
* <span data-ttu-id="830f3-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="830f3-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="830f3-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="830f3-139">RELATED LINKS</span></span>

[<span data-ttu-id="830f3-140">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="830f3-140">Get-AzureRmDataLakeStoreItemAclEntry</span></span>](./Get-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="830f3-141">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="830f3-141">Set-AzureRmDataLakeStoreItemAcl</span></span>](./Set-AzureRmDataLakeStoreItemAcl.md)

[<span data-ttu-id="830f3-142">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="830f3-142">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


