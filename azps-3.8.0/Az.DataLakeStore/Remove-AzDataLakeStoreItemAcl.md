---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: ed7b1a0c0c969f2593d045549f897a172a88f6aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088781"
---
# <span data-ttu-id="59fb7-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="59fb7-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="59fb7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="59fb7-103">Rensar en ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="59fb7-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="59fb7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59fb7-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59fb7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59fb7-105">DESCRIPTION</span></span>
<span data-ttu-id="59fb7-106">Cmdleten **Remove-AzDataLakeStoreItemAcl** rensar åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="59fb7-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="59fb7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59fb7-107">EXAMPLES</span></span>

### <span data-ttu-id="59fb7-108">Exempel 1: ta bort en ACL från en mapp</span><span class="sxs-lookup"><span data-stu-id="59fb7-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="59fb7-109">Det här kommandot tar bort ACL för rot katalogen för ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="59fb7-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="59fb7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59fb7-110">PARAMETERS</span></span>

### <span data-ttu-id="59fb7-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="59fb7-111">-Account</span></span>
<span data-ttu-id="59fb7-112">Anger namnet på data Lake Store-butiken.</span><span class="sxs-lookup"><span data-stu-id="59fb7-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="59fb7-113">-Standard</span><span class="sxs-lookup"><span data-stu-id="59fb7-113">-Default</span></span>
<span data-ttu-id="59fb7-114">Anger att cmdleten tar bort standard åtkomst för en fil eller mapp.</span><span class="sxs-lookup"><span data-stu-id="59fb7-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="59fb7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fb7-115">-DefaultProfile</span></span>
<span data-ttu-id="59fb7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59fb7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59fb7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="59fb7-117">-Force</span></span>
<span data-ttu-id="59fb7-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="59fb7-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="59fb7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59fb7-119">-PassThru</span></span>
<span data-ttu-id="59fb7-120">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="59fb7-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59fb7-121">-Path</span><span class="sxs-lookup"><span data-stu-id="59fb7-121">-Path</span></span>
<span data-ttu-id="59fb7-122">Anger data Lake Store-sökvägen för objektet, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="59fb7-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="59fb7-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59fb7-123">-Confirm</span></span>
<span data-ttu-id="59fb7-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59fb7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59fb7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59fb7-125">-WhatIf</span></span>
<span data-ttu-id="59fb7-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59fb7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59fb7-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59fb7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59fb7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fb7-128">CommonParameters</span></span>
<span data-ttu-id="59fb7-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59fb7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fb7-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59fb7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fb7-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59fb7-131">INPUTS</span></span>

### <span data-ttu-id="59fb7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="59fb7-132">System.String</span></span>

### <span data-ttu-id="59fb7-133">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="59fb7-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="59fb7-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="59fb7-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="59fb7-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59fb7-135">OUTPUTS</span></span>

### <span data-ttu-id="59fb7-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59fb7-136">System.Boolean</span></span>

## <span data-ttu-id="59fb7-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59fb7-137">NOTES</span></span>
* <span data-ttu-id="59fb7-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="59fb7-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="59fb7-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59fb7-139">RELATED LINKS</span></span>

[<span data-ttu-id="59fb7-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="59fb7-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="59fb7-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="59fb7-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="59fb7-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="59fb7-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


