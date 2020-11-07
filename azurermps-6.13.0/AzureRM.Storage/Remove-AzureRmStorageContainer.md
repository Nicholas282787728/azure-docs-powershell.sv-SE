---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
ms.openlocfilehash: 089451a0a0aae399a18296fbf4982724b35d432e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757817"
---
# <span data-ttu-id="51d2d-101">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="51d2d-101">Remove-AzureRmStorageContainer</span></span>

## <span data-ttu-id="51d2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51d2d-102">SYNOPSIS</span></span>
<span data-ttu-id="51d2d-103">Tar bort en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="51d2d-103">Removes a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51d2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51d2d-104">SYNTAX</span></span>

### <span data-ttu-id="51d2d-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="51d2d-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51d2d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="51d2d-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51d2d-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="51d2d-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51d2d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51d2d-108">DESCRIPTION</span></span>
<span data-ttu-id="51d2d-109">Cmdleten **Remove-AzureRmStorageContainer** tar bort en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="51d2d-109">The **Remove-AzureRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="51d2d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51d2d-110">EXAMPLES</span></span>

### <span data-ttu-id="51d2d-111">Exempel 1: ta bort en lagrings-BLOB-behållare med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="51d2d-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="51d2d-112">Det här kommandot tar bort en lagrings-BLOB med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="51d2d-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="51d2d-113">Exempel 2: ta bort en lagrings-BLOB-behållare med lagrings konto objekt och container namn</span><span class="sxs-lookup"><span data-stu-id="51d2d-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="51d2d-114">Det här kommandot tar bort en lagrings-BLOB-behållare med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="51d2d-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="51d2d-115">Exempel 3: ta bort alla lagrings-BLOB-behållare i ett lagrings konto med pipeline</span><span class="sxs-lookup"><span data-stu-id="51d2d-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainer -Force
```

<span data-ttu-id="51d2d-116">Det här kommandot tar bort alla lagrings-BLOB-behållare i ett lagrings konto med pipeline.</span><span class="sxs-lookup"><span data-stu-id="51d2d-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="51d2d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51d2d-117">PARAMETERS</span></span>

### <span data-ttu-id="51d2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51d2d-118">-DefaultProfile</span></span>
<span data-ttu-id="51d2d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51d2d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51d2d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="51d2d-120">-Force</span></span>
<span data-ttu-id="51d2d-121">Tvinga att ta bort behållaren och allt innehåll i den</span><span class="sxs-lookup"><span data-stu-id="51d2d-121">Force to remove the container and all content in it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d2d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51d2d-122">-InputObject</span></span>
<span data-ttu-id="51d2d-123">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="51d2d-123">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51d2d-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="51d2d-124">-Name</span></span>
<span data-ttu-id="51d2d-125">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="51d2d-125">Container Name</span></span>

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

### <span data-ttu-id="51d2d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51d2d-126">-PassThru</span></span>
<span data-ttu-id="51d2d-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="51d2d-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d2d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51d2d-128">-ResourceGroupName</span></span>
<span data-ttu-id="51d2d-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="51d2d-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="51d2d-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="51d2d-130">-StorageAccount</span></span>
<span data-ttu-id="51d2d-131">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="51d2d-131">Storage account object</span></span>

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

### <span data-ttu-id="51d2d-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="51d2d-132">-StorageAccountName</span></span>
<span data-ttu-id="51d2d-133">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="51d2d-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="51d2d-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51d2d-134">-Confirm</span></span>
<span data-ttu-id="51d2d-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51d2d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51d2d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51d2d-136">-WhatIf</span></span>
<span data-ttu-id="51d2d-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51d2d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51d2d-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51d2d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51d2d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51d2d-139">CommonParameters</span></span>
<span data-ttu-id="51d2d-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51d2d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51d2d-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51d2d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51d2d-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51d2d-142">INPUTS</span></span>

### <span data-ttu-id="51d2d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="51d2d-143">System.String</span></span>

## <span data-ttu-id="51d2d-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51d2d-144">OUTPUTS</span></span>

### <span data-ttu-id="51d2d-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="51d2d-145">System.Object</span></span>

## <span data-ttu-id="51d2d-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51d2d-146">NOTES</span></span>

## <span data-ttu-id="51d2d-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51d2d-147">RELATED LINKS</span></span>
