---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 494995a97ccb74df9ad9a9fc1f88272505598bb9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092396"
---
# <span data-ttu-id="bf0a9-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="bf0a9-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="bf0a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf0a9-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0a9-103">Tar bort giltiga undantags koder från en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="bf0a9-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="bf0a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf0a9-104">SYNTAX</span></span>

### <span data-ttu-id="bf0a9-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="bf0a9-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf0a9-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="bf0a9-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf0a9-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="bf0a9-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf0a9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf0a9-108">DESCRIPTION</span></span>
<span data-ttu-id="bf0a9-109">Cmdleten **Remove-AzRmStorageContainerLegalHold** tar bort giltiga undantags koder från en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="bf0a9-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="bf0a9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf0a9-110">EXAMPLES</span></span>

### <span data-ttu-id="bf0a9-111">Exempel 1: ta bort giltiga undantag från en lagrings-BLOB med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="bf0a9-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="bf0a9-112">Det här kommandot tar bort giltiga undantags koder från en lagrings-BLOB med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="bf0a9-113">Exempel 2: ta bort flaggor för juridiska undantag från en lagrings-BLOB med lagrings konto objekt och container namn</span><span class="sxs-lookup"><span data-stu-id="bf0a9-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="bf0a9-114">Det här kommandot tar bort giltiga undantags koder från en lagrings-BLOB med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="bf0a9-115">Exempel 3: ta bort giltiga undantag från alla lagrings-BLOB-behållare i ett lagrings konto med pipeline</span><span class="sxs-lookup"><span data-stu-id="bf0a9-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="bf0a9-116">Det här kommandot tar bort giltiga undantags koder från alla lagrings-BLOB-behållare i ett lagrings konto med pipeline.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="bf0a9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf0a9-117">PARAMETERS</span></span>

### <span data-ttu-id="bf0a9-118">-Container</span><span class="sxs-lookup"><span data-stu-id="bf0a9-118">-Container</span></span>
<span data-ttu-id="bf0a9-119">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="bf0a9-119">Storage container object</span></span>

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

### <span data-ttu-id="bf0a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0a9-120">-DefaultProfile</span></span>
<span data-ttu-id="bf0a9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf0a9-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="bf0a9-122">-Name</span></span>
<span data-ttu-id="bf0a9-123">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="bf0a9-123">Container Name</span></span>

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

### <span data-ttu-id="bf0a9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf0a9-124">-ResourceGroupName</span></span>
<span data-ttu-id="bf0a9-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="bf0a9-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf0a9-126">-StorageAccount</span></span>
<span data-ttu-id="bf0a9-127">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="bf0a9-127">Storage account object</span></span>

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

### <span data-ttu-id="bf0a9-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bf0a9-128">-StorageAccountName</span></span>
<span data-ttu-id="bf0a9-129">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="bf0a9-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="bf0a9-130">-Tag</span></span>
<span data-ttu-id="bf0a9-131">LegalHold-taggar för container</span><span class="sxs-lookup"><span data-stu-id="bf0a9-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="bf0a9-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf0a9-132">-Confirm</span></span>
<span data-ttu-id="bf0a9-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf0a9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf0a9-134">-WhatIf</span></span>
<span data-ttu-id="bf0a9-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf0a9-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf0a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0a9-137">CommonParameters</span></span>
<span data-ttu-id="bf0a9-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0a9-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf0a9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0a9-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf0a9-140">INPUTS</span></span>

### <span data-ttu-id="bf0a9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bf0a9-141">System.String</span></span>

### <span data-ttu-id="bf0a9-142">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf0a9-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="bf0a9-143">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="bf0a9-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="bf0a9-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf0a9-144">OUTPUTS</span></span>

### <span data-ttu-id="bf0a9-145">Microsoft. Azure. commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="bf0a9-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="bf0a9-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf0a9-146">NOTES</span></span>

## <span data-ttu-id="bf0a9-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf0a9-147">RELATED LINKS</span></span>
