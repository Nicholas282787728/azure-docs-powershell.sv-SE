---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 74963ef36a33bed6145d315f5792aa776a36bc7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578739"
---
# <span data-ttu-id="2481b-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2481b-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="2481b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2481b-102">SYNOPSIS</span></span>
<span data-ttu-id="2481b-103">Tar bort ImmutabilityPolicy för en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="2481b-103">Removes ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2481b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2481b-104">SYNTAX</span></span>

### <span data-ttu-id="2481b-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="2481b-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2481b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2481b-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2481b-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="2481b-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2481b-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="2481b-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2481b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2481b-109">DESCRIPTION</span></span>
<span data-ttu-id="2481b-110">Cmdleten **Remove-AzureRmStorageContainerImmutabilityPolicy** tar bort ImmutabilityPolicy i en BLOB-behållare för lagring.</span><span class="sxs-lookup"><span data-stu-id="2481b-110">The **Remove-AzureRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="2481b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2481b-111">EXAMPLES</span></span>

### <span data-ttu-id="2481b-112">Exempel 1: ta bort ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="2481b-112">Example 1: Remove ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="2481b-113">Det här kommandot tar bort ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="2481b-113">This command removes ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="2481b-114">Exempel 2: ta bort ImmutabilityPolicy för en lagrings-behållare med lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="2481b-114">Example 2: Remove ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="2481b-115">Det här kommandot tar bort ImmutabilityPolicy för en lagrings-behållare med lagrings konto objekt.</span><span class="sxs-lookup"><span data-stu-id="2481b-115">This command removes ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="2481b-116">Exempel 3: ta bort ImmutabilityPolicyof en BLOB-behållare för lagring, med behållar-objekt</span><span class="sxs-lookup"><span data-stu-id="2481b-116">Example 3: Remove ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="2481b-117">Det här kommandot tar bort ImmutabilityPolicy för en lagrings-behållare med lagrings behållar objekt.</span><span class="sxs-lookup"><span data-stu-id="2481b-117">This command removes ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="2481b-118">Exempel 4: ta bort ImmutabilityPolicy för en lagrings-behållare med ImmutabilityPolicy-objekt</span><span class="sxs-lookup"><span data-stu-id="2481b-118">Example 4: Remove ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzureRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="2481b-119">Det här kommandot tar bort ImmutabilityPolicy för en lagrings-behållare med ImmutabilityPolicy-objekt.</span><span class="sxs-lookup"><span data-stu-id="2481b-119">This command removes ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="2481b-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2481b-120">PARAMETERS</span></span>

### <span data-ttu-id="2481b-121">-Container</span><span class="sxs-lookup"><span data-stu-id="2481b-121">-Container</span></span>
<span data-ttu-id="2481b-122">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="2481b-122">Storage container object</span></span>

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

### <span data-ttu-id="2481b-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="2481b-123">-ContainerName</span></span>
<span data-ttu-id="2481b-124">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="2481b-124">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2481b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2481b-125">-DefaultProfile</span></span>
<span data-ttu-id="2481b-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2481b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2481b-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="2481b-127">-Etag</span></span>
<span data-ttu-id="2481b-128">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="2481b-128">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2481b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2481b-129">-InputObject</span></span>
<span data-ttu-id="2481b-130">ImmutabilityPolicy-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="2481b-130">ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2481b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2481b-131">-ResourceGroupName</span></span>
<span data-ttu-id="2481b-132">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2481b-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="2481b-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2481b-133">-StorageAccount</span></span>
<span data-ttu-id="2481b-134">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="2481b-134">Storage account object</span></span>

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

### <span data-ttu-id="2481b-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2481b-135">-StorageAccountName</span></span>
<span data-ttu-id="2481b-136">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="2481b-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="2481b-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2481b-137">-Confirm</span></span>
<span data-ttu-id="2481b-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2481b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2481b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2481b-139">-WhatIf</span></span>
<span data-ttu-id="2481b-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2481b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2481b-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2481b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2481b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2481b-142">CommonParameters</span></span>
<span data-ttu-id="2481b-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2481b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2481b-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2481b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2481b-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2481b-145">INPUTS</span></span>

### <span data-ttu-id="2481b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2481b-146">System.String</span></span>
<span data-ttu-id="2481b-147">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2481b-147">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="2481b-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2481b-148">OUTPUTS</span></span>

### <span data-ttu-id="2481b-149">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2481b-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="2481b-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2481b-150">NOTES</span></span>

## <span data-ttu-id="2481b-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2481b-151">RELATED LINKS</span></span>

