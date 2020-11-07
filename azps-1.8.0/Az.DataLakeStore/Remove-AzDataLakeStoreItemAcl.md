---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 9339857a125ca0646869a81749f9cf55ff2531ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754289"
---
# <span data-ttu-id="4c217-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="4c217-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="4c217-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c217-102">SYNOPSIS</span></span>
<span data-ttu-id="4c217-103">Rensar en ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4c217-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4c217-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c217-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c217-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c217-105">DESCRIPTION</span></span>
<span data-ttu-id="4c217-106">Cmdleten **Remove-AzDataLakeStoreItemAcl** rensar åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4c217-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4c217-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c217-107">EXAMPLES</span></span>

### <span data-ttu-id="4c217-108">Exempel 1: ta bort en ACL från en mapp</span><span class="sxs-lookup"><span data-stu-id="4c217-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="4c217-109">Det här kommandot tar bort ACL för rot katalogen för ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="4c217-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="4c217-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c217-110">PARAMETERS</span></span>

### <span data-ttu-id="4c217-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="4c217-111">-Account</span></span>
<span data-ttu-id="4c217-112">Anger namnet på data Lake Store-butiken.</span><span class="sxs-lookup"><span data-stu-id="4c217-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="4c217-113">-Standard</span><span class="sxs-lookup"><span data-stu-id="4c217-113">-Default</span></span>
<span data-ttu-id="4c217-114">Anger att cmdleten tar bort standard åtkomst för en fil eller mapp.</span><span class="sxs-lookup"><span data-stu-id="4c217-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="4c217-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c217-115">-DefaultProfile</span></span>
<span data-ttu-id="4c217-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c217-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c217-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4c217-117">-Force</span></span>
<span data-ttu-id="4c217-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4c217-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4c217-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c217-119">-PassThru</span></span>
<span data-ttu-id="4c217-120">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="4c217-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="4c217-121">-Path</span><span class="sxs-lookup"><span data-stu-id="4c217-121">-Path</span></span>
<span data-ttu-id="4c217-122">Anger data Lake Store-sökvägen för objektet, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="4c217-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4c217-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4c217-123">-Confirm</span></span>
<span data-ttu-id="4c217-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4c217-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c217-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c217-125">-WhatIf</span></span>
<span data-ttu-id="4c217-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4c217-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c217-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4c217-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c217-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c217-128">CommonParameters</span></span>
<span data-ttu-id="4c217-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c217-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c217-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c217-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c217-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c217-131">INPUTS</span></span>

### <span data-ttu-id="4c217-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4c217-132">System.String</span></span>

### <span data-ttu-id="4c217-133">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4c217-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4c217-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4c217-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4c217-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c217-135">OUTPUTS</span></span>

### <span data-ttu-id="4c217-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c217-136">System.Boolean</span></span>

## <span data-ttu-id="4c217-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c217-137">NOTES</span></span>
* <span data-ttu-id="4c217-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="4c217-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="4c217-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c217-139">RELATED LINKS</span></span>

[<span data-ttu-id="4c217-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="4c217-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="4c217-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="4c217-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="4c217-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="4c217-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)

