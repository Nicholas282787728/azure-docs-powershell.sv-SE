---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: da0793e7eb10f7b83d785aea34866842abe9b887
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578736"
---
# <span data-ttu-id="b93f7-101">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="b93f7-101">Remove-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="b93f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b93f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b93f7-103">Tar bort giltiga undantags koder från en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="b93f7-103">Removes legal hold tags from a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b93f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b93f7-104">SYNTAX</span></span>

### <span data-ttu-id="b93f7-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="b93f7-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b93f7-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b93f7-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b93f7-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="b93f7-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b93f7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b93f7-108">DESCRIPTION</span></span>
<span data-ttu-id="b93f7-109">Cmdleten **Remove-AzureRmStorageContainerLegalHold** tar bort giltiga undantags koder från en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="b93f7-109">The **Remove-AzureRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="b93f7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b93f7-110">EXAMPLES</span></span>

### <span data-ttu-id="b93f7-111">Exempel 1: ta bort giltiga undantag från en lagrings-BLOB med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="b93f7-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="b93f7-112">Det här kommandot tar bort giltiga undantags koder från en lagrings-BLOB med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="b93f7-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="b93f7-113">Exempel 2: ta bort flaggor för juridiska undantag från en lagrings-BLOB med lagrings konto objekt och container namn</span><span class="sxs-lookup"><span data-stu-id="b93f7-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2 
```

<span data-ttu-id="b93f7-114">Det här kommandot tar bort giltiga undantags koder från en lagrings-BLOB med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="b93f7-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="b93f7-115">Exempel 3: ta bort giltiga undantag från alla lagrings-BLOB-behållare i ett lagrings konto med pipeline</span><span class="sxs-lookup"><span data-stu-id="b93f7-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="b93f7-116">Det här kommandot tar bort giltiga undantags koder från alla lagrings-BLOB-behållare i ett lagrings konto med pipeline.</span><span class="sxs-lookup"><span data-stu-id="b93f7-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>


## <span data-ttu-id="b93f7-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b93f7-117">PARAMETERS</span></span>

### <span data-ttu-id="b93f7-118">-Container</span><span class="sxs-lookup"><span data-stu-id="b93f7-118">-Container</span></span>
<span data-ttu-id="b93f7-119">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="b93f7-119">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b93f7-120">-DefaultProfile</span></span>
<span data-ttu-id="b93f7-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b93f7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b93f7-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b93f7-122">-Name</span></span>
<span data-ttu-id="b93f7-123">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="b93f7-123">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b93f7-124">-ResourceGroupName</span></span>
<span data-ttu-id="b93f7-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b93f7-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b93f7-126">-StorageAccount</span></span>
<span data-ttu-id="b93f7-127">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="b93f7-127">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b93f7-128">-StorageAccountName</span></span>
<span data-ttu-id="b93f7-129">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b93f7-129">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b93f7-130">-Tag</span></span>
<span data-ttu-id="b93f7-131">LegalHold-taggar för container</span><span class="sxs-lookup"><span data-stu-id="b93f7-131">Container LegalHold Tags</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b93f7-132">-Confirm</span></span>
<span data-ttu-id="b93f7-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b93f7-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b93f7-134">-WhatIf</span></span>
<span data-ttu-id="b93f7-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b93f7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b93f7-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b93f7-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b93f7-137">CommonParameters</span></span>
<span data-ttu-id="b93f7-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b93f7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b93f7-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b93f7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b93f7-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b93f7-140">INPUTS</span></span>

### <span data-ttu-id="b93f7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b93f7-141">System.String</span></span>

## <span data-ttu-id="b93f7-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b93f7-142">OUTPUTS</span></span>

### <span data-ttu-id="b93f7-143">Microsoft. Azure. commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="b93f7-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="b93f7-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b93f7-144">NOTES</span></span>

## <span data-ttu-id="b93f7-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b93f7-145">RELATED LINKS</span></span>

