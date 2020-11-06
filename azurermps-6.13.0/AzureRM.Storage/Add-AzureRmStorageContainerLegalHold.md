---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: 465a40e384e5ea7240e0ced2a010c88529feb2f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573860"
---
# <span data-ttu-id="c43db-101">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="c43db-101">Add-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="c43db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c43db-102">SYNOPSIS</span></span>
<span data-ttu-id="c43db-103">Lägger till juridiska undantags flaggor i en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="c43db-103">Adds legal hold tags to a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c43db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c43db-104">SYNTAX</span></span>

### <span data-ttu-id="c43db-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="c43db-105">AccountName (Default)</span></span>
```
Add-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c43db-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c43db-106">AccountObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c43db-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="c43db-107">ContainerObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c43db-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c43db-108">DESCRIPTION</span></span>
<span data-ttu-id="c43db-109">Cmdleten **Add-AzureRmStorageContainerLegalHold** lägger till juridiska undantags flaggor i en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="c43db-109">The **Add-AzureRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="c43db-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c43db-110">EXAMPLES</span></span>

### <span data-ttu-id="c43db-111">Exempel 1: lägga till flaggor för juridiska undantag i en lagrings-BLOB med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="c43db-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2 
```

<span data-ttu-id="c43db-112">Det här kommandot lägger till giltiga undantags flaggor i en lagrings-BLOB med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="c43db-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="c43db-113">Exempel 2: lägga till taggar för juridiska undantag i en lagrings-BLOB med lagrings konto objekt och container namn</span><span class="sxs-lookup"><span data-stu-id="c43db-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="c43db-114">Det här kommandot lägger till giltiga undantags flaggor i en lagrings-BLOB med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="c43db-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="c43db-115">Exempel 3: lägga till taggar för juridiska undantag i alla lagrings-BLOB-behållare i ett lagrings konto med pipeline</span><span class="sxs-lookup"><span data-stu-id="c43db-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzureRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="c43db-116">Det här kommandot lägger till juridiska undantags flaggor i alla lagrings-BLOB-behållare i ett lagrings konto med pipeline.</span><span class="sxs-lookup"><span data-stu-id="c43db-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="c43db-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c43db-117">PARAMETERS</span></span>

### <span data-ttu-id="c43db-118">-Container</span><span class="sxs-lookup"><span data-stu-id="c43db-118">-Container</span></span>
<span data-ttu-id="c43db-119">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="c43db-119">Storage container object</span></span>

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

### <span data-ttu-id="c43db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c43db-120">-DefaultProfile</span></span>
<span data-ttu-id="c43db-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c43db-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c43db-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c43db-122">-Name</span></span>
<span data-ttu-id="c43db-123">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="c43db-123">Container Name</span></span>

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

### <span data-ttu-id="c43db-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c43db-124">-ResourceGroupName</span></span>
<span data-ttu-id="c43db-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c43db-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c43db-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c43db-126">-StorageAccount</span></span>
<span data-ttu-id="c43db-127">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="c43db-127">Storage account object</span></span>

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

### <span data-ttu-id="c43db-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c43db-128">-StorageAccountName</span></span>
<span data-ttu-id="c43db-129">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="c43db-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="c43db-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c43db-130">-Tag</span></span>
<span data-ttu-id="c43db-131">LegalHold-taggar för container</span><span class="sxs-lookup"><span data-stu-id="c43db-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="c43db-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c43db-132">-Confirm</span></span>
<span data-ttu-id="c43db-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c43db-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c43db-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c43db-134">-WhatIf</span></span>
<span data-ttu-id="c43db-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c43db-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c43db-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c43db-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c43db-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c43db-137">CommonParameters</span></span>
<span data-ttu-id="c43db-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c43db-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c43db-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c43db-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c43db-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c43db-140">INPUTS</span></span>

### <span data-ttu-id="c43db-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c43db-141">System.String</span></span>

## <span data-ttu-id="c43db-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c43db-142">OUTPUTS</span></span>

### <span data-ttu-id="c43db-143">Microsoft. Azure. commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="c43db-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="c43db-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c43db-144">NOTES</span></span>

## <span data-ttu-id="c43db-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c43db-145">RELATED LINKS</span></span>

