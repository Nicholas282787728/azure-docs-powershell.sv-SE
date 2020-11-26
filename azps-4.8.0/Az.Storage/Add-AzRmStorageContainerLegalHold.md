---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 438aa207d28ca2a432d413f847d674d25bf55a42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103446"
---
# <span data-ttu-id="d4847-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="d4847-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="d4847-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4847-102">SYNOPSIS</span></span>
<span data-ttu-id="d4847-103">Lägger till juridiska undantags flaggor i en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="d4847-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="d4847-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4847-104">SYNTAX</span></span>

### <span data-ttu-id="d4847-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="d4847-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4847-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d4847-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4847-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="d4847-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4847-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4847-108">DESCRIPTION</span></span>
<span data-ttu-id="d4847-109">Cmdleten **Add-AzRmStorageContainerLegalHold** lägger till juridiska undantags flaggor i en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="d4847-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="d4847-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4847-110">EXAMPLES</span></span>

### <span data-ttu-id="d4847-111">Exempel 1: lägga till flaggor för juridiska undantag i en lagrings-BLOB med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="d4847-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="d4847-112">Det här kommandot lägger till giltiga undantags flaggor i en lagrings-BLOB med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="d4847-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d4847-113">Exempel 2: lägga till taggar för juridiska undantag i en lagrings-BLOB med lagrings konto objekt och container namn</span><span class="sxs-lookup"><span data-stu-id="d4847-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="d4847-114">Det här kommandot lägger till giltiga undantags flaggor i en lagrings-BLOB med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="d4847-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="d4847-115">Exempel 3: lägga till taggar för juridiska undantag i alla lagrings-BLOB-behållare i ett lagrings konto med pipeline</span><span class="sxs-lookup"><span data-stu-id="d4847-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="d4847-116">Det här kommandot lägger till juridiska undantags flaggor i alla lagrings-BLOB-behållare i ett lagrings konto med pipeline.</span><span class="sxs-lookup"><span data-stu-id="d4847-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="d4847-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4847-117">PARAMETERS</span></span>

### <span data-ttu-id="d4847-118">-Container</span><span class="sxs-lookup"><span data-stu-id="d4847-118">-Container</span></span>
<span data-ttu-id="d4847-119">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="d4847-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4847-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4847-120">-DefaultProfile</span></span>
<span data-ttu-id="d4847-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4847-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4847-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d4847-122">-Name</span></span>
<span data-ttu-id="d4847-123">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="d4847-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4847-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4847-124">-ResourceGroupName</span></span>
<span data-ttu-id="d4847-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d4847-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4847-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4847-126">-StorageAccount</span></span>
<span data-ttu-id="d4847-127">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="d4847-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4847-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d4847-128">-StorageAccountName</span></span>
<span data-ttu-id="d4847-129">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="d4847-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4847-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d4847-130">-Tag</span></span>
<span data-ttu-id="d4847-131">LegalHold-taggar för container</span><span class="sxs-lookup"><span data-stu-id="d4847-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4847-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d4847-132">-Confirm</span></span>
<span data-ttu-id="d4847-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d4847-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4847-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4847-134">-WhatIf</span></span>
<span data-ttu-id="d4847-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d4847-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4847-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d4847-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4847-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4847-137">CommonParameters</span></span>
<span data-ttu-id="d4847-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4847-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4847-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4847-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4847-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4847-140">INPUTS</span></span>

### <span data-ttu-id="d4847-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d4847-141">System.String</span></span>

### <span data-ttu-id="d4847-142">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4847-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d4847-143">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="d4847-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="d4847-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4847-144">OUTPUTS</span></span>

### <span data-ttu-id="d4847-145">Microsoft. Azure. commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="d4847-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="d4847-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4847-146">NOTES</span></span>

## <span data-ttu-id="d4847-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4847-147">RELATED LINKS</span></span>