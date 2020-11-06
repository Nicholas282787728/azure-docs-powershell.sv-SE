---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 48edcb93cb8fce66c9175bdcf498bd6545949090
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580648"
---
# <span data-ttu-id="d7222-101">Remove-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="d7222-101">Remove-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="d7222-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7222-102">SYNOPSIS</span></span>
<span data-ttu-id="d7222-103">Rensar en ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7222-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7222-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7222-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7222-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7222-105">DESCRIPTION</span></span>
<span data-ttu-id="d7222-106">Cmdleten **Remove-AzureRmDataLakeStoreItemAcl** rensar åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7222-106">The **Remove-AzureRmDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d7222-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7222-107">EXAMPLES</span></span>

### <span data-ttu-id="d7222-108">Exempel 1: ta bort en ACL från en mapp</span><span class="sxs-lookup"><span data-stu-id="d7222-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="d7222-109">Det här kommandot tar bort ACL för rot katalogen för ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="d7222-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="d7222-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7222-110">PARAMETERS</span></span>

### <span data-ttu-id="d7222-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="d7222-111">-Account</span></span>
<span data-ttu-id="d7222-112">Anger namnet på data Lake Store-butiken.</span><span class="sxs-lookup"><span data-stu-id="d7222-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="d7222-113">-Standard</span><span class="sxs-lookup"><span data-stu-id="d7222-113">-Default</span></span>
<span data-ttu-id="d7222-114">Anger att cmdleten tar bort standard åtkomst för en fil eller mapp.</span><span class="sxs-lookup"><span data-stu-id="d7222-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="d7222-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d7222-115">-Force</span></span>
<span data-ttu-id="d7222-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d7222-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d7222-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7222-117">-PassThru</span></span>
<span data-ttu-id="d7222-118">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="d7222-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="d7222-119">-Path</span><span class="sxs-lookup"><span data-stu-id="d7222-119">-Path</span></span>
<span data-ttu-id="d7222-120">Anger data Lake Store-sökvägen för objektet, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="d7222-120">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d7222-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d7222-121">-Confirm</span></span>
<span data-ttu-id="d7222-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d7222-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7222-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7222-123">-WhatIf</span></span>
<span data-ttu-id="d7222-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d7222-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7222-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d7222-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7222-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7222-126">-DefaultProfile</span></span>
<span data-ttu-id="d7222-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7222-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7222-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7222-128">CommonParameters</span></span>
<span data-ttu-id="d7222-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7222-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7222-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7222-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7222-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7222-131">INPUTS</span></span>

## <span data-ttu-id="d7222-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7222-132">OUTPUTS</span></span>

### <span data-ttu-id="d7222-133">bool</span><span class="sxs-lookup"><span data-stu-id="d7222-133">bool</span></span>
<span data-ttu-id="d7222-134">Om PassThru är angivet returneras sant när du är klar.</span><span class="sxs-lookup"><span data-stu-id="d7222-134">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="d7222-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7222-135">NOTES</span></span>
* <span data-ttu-id="d7222-136">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="d7222-136">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="d7222-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7222-137">RELATED LINKS</span></span>

[<span data-ttu-id="d7222-138">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d7222-138">Get-AzureRmDataLakeStoreItemAclEntry</span></span>](./Get-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="d7222-139">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="d7222-139">Set-AzureRmDataLakeStoreItemAcl</span></span>](./Set-AzureRmDataLakeStoreItemAcl.md)

[<span data-ttu-id="d7222-140">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d7222-140">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


