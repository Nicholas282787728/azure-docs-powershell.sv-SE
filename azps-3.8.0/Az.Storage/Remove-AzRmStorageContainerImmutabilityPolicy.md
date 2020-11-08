---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: eedeeb3311373c240cd564534d3438b948c7a0f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092398"
---
# <span data-ttu-id="554c5-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="554c5-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="554c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="554c5-102">SYNOPSIS</span></span>
<span data-ttu-id="554c5-103">Tar bort ImmutabilityPolicy för en lagrings-behållare med en olåst princip</span><span class="sxs-lookup"><span data-stu-id="554c5-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="554c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="554c5-104">SYNTAX</span></span>

### <span data-ttu-id="554c5-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="554c5-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="554c5-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="554c5-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="554c5-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="554c5-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="554c5-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="554c5-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="554c5-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="554c5-109">DESCRIPTION</span></span>
<span data-ttu-id="554c5-110">Cmdleten **Remove-AzRmStorageContainerImmutabilityPolicy** tar bort ImmutabilityPolicy för en lagrings-BLOB med en olåst princip.</span><span class="sxs-lookup"><span data-stu-id="554c5-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="554c5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="554c5-111">EXAMPLES</span></span>

### <span data-ttu-id="554c5-112">Exempel 1: ta bort olåst ImmutabilityPolicy för en lagrings-BLOB med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="554c5-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="554c5-113">Det här kommandot tar bort olåsta ImmutabilityPolicy för en lagrings-BLOB med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="554c5-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="554c5-114">Exempel 2: ta bort olåsta ImmutabilityPolicy för en lagrings-behållare med lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="554c5-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="554c5-115">Det här kommandot tar bort olåsta ImmutabilityPolicy för en lagrings-BLOB-behållare med lagrings konto objekt.</span><span class="sxs-lookup"><span data-stu-id="554c5-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="554c5-116">Exempel 3: ta bort olåsta ImmutabilityPolicy för en lagrings-behållare, med behållar-objekt</span><span class="sxs-lookup"><span data-stu-id="554c5-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="554c5-117">Det här kommandot tar bort olåsta ImmutabilityPolicy för en lagrings-BLOB med lagrings behållar objekt.</span><span class="sxs-lookup"><span data-stu-id="554c5-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="554c5-118">Exempel 4: ta bort olåsta ImmutabilityPolicy för en lagrings-behållare med ImmutabilityPolicy-objekt</span><span class="sxs-lookup"><span data-stu-id="554c5-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="554c5-119">Det här kommandot tar bort olåsta ImmutabilityPolicy för en lagrings-behållare, med ImmutabilityPolicy-objekt.</span><span class="sxs-lookup"><span data-stu-id="554c5-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="554c5-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="554c5-120">PARAMETERS</span></span>

### <span data-ttu-id="554c5-121">-Container</span><span class="sxs-lookup"><span data-stu-id="554c5-121">-Container</span></span>
<span data-ttu-id="554c5-122">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="554c5-122">Storage container object</span></span>

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

### <span data-ttu-id="554c5-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="554c5-123">-ContainerName</span></span>
<span data-ttu-id="554c5-124">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="554c5-124">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="554c5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="554c5-125">-DefaultProfile</span></span>
<span data-ttu-id="554c5-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="554c5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="554c5-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="554c5-127">-Etag</span></span>
<span data-ttu-id="554c5-128">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="554c5-128">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="554c5-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="554c5-129">-InputObject</span></span>
<span data-ttu-id="554c5-130">Olåst ImmutabilityPolicy-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="554c5-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="554c5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="554c5-131">-ResourceGroupName</span></span>
<span data-ttu-id="554c5-132">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="554c5-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="554c5-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="554c5-133">-StorageAccount</span></span>
<span data-ttu-id="554c5-134">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="554c5-134">Storage account object</span></span>

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

### <span data-ttu-id="554c5-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="554c5-135">-StorageAccountName</span></span>
<span data-ttu-id="554c5-136">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="554c5-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="554c5-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="554c5-137">-Confirm</span></span>
<span data-ttu-id="554c5-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="554c5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="554c5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="554c5-139">-WhatIf</span></span>
<span data-ttu-id="554c5-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="554c5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="554c5-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="554c5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="554c5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="554c5-142">CommonParameters</span></span>
<span data-ttu-id="554c5-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="554c5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="554c5-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="554c5-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="554c5-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="554c5-145">INPUTS</span></span>

### <span data-ttu-id="554c5-146">System. String</span><span class="sxs-lookup"><span data-stu-id="554c5-146">System.String</span></span>

### <span data-ttu-id="554c5-147">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="554c5-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="554c5-148">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="554c5-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="554c5-149">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="554c5-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="554c5-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="554c5-150">OUTPUTS</span></span>

### <span data-ttu-id="554c5-151">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="554c5-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="554c5-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="554c5-152">NOTES</span></span>

## <span data-ttu-id="554c5-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="554c5-153">RELATED LINKS</span></span>
