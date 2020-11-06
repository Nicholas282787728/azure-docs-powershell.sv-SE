---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/lock-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 726dc9043c1082f97e32da46305cf81192e1806c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572620"
---
# <span data-ttu-id="0246c-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0246c-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="0246c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0246c-102">SYNOPSIS</span></span>
<span data-ttu-id="0246c-103">Lås ImmutabilityPolicy för en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="0246c-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0246c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0246c-104">SYNTAX</span></span>

### <span data-ttu-id="0246c-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="0246c-105">AccountName (Default)</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0246c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0246c-106">AccountObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0246c-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="0246c-107">ContainerObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0246c-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="0246c-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0246c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0246c-109">DESCRIPTION</span></span>
<span data-ttu-id="0246c-110">**Lås-AzureRmStorageContainerImmutabilityPolicy** cmdlet låser ImmutabilityPolicy i en lagrings-BLOB-behållare.</span><span class="sxs-lookup"><span data-stu-id="0246c-110">The **Lock-AzureRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="0246c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0246c-111">EXAMPLES</span></span>

### <span data-ttu-id="0246c-112">Exempel 1: Lås ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="0246c-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="0246c-113">Det här kommandot låser ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="0246c-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="0246c-114">Exempel 2: Lås ImmutabilityPolicy för en lagrings-behållare med lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="0246c-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="0246c-115">Det här kommandot låser ImmutabilityPolicy för en lagrings-behållare med lagrings konto objekt.</span><span class="sxs-lookup"><span data-stu-id="0246c-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="0246c-116">Exempel 3: Lås ImmutabilityPolicyof en BLOB-behållare för lagring, med behållar-objekt</span><span class="sxs-lookup"><span data-stu-id="0246c-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="0246c-117">Det här kommandot låser ImmutabilityPolicy för en lagrings-behållare med lagrings Container objekt.</span><span class="sxs-lookup"><span data-stu-id="0246c-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="0246c-118">Exempel 4: Lås ImmutabilityPolicy för en lagrings-behållare med ImmutabilityPolicy-objekt</span><span class="sxs-lookup"><span data-stu-id="0246c-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzureRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="0246c-119">Det här kommandot låser ImmutabilityPolicy för en lagrings-behållare med ImmutabilityPolicy-objekt.</span><span class="sxs-lookup"><span data-stu-id="0246c-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="0246c-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0246c-120">PARAMETERS</span></span>

### <span data-ttu-id="0246c-121">-Container</span><span class="sxs-lookup"><span data-stu-id="0246c-121">-Container</span></span>
<span data-ttu-id="0246c-122">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="0246c-122">Storage container object</span></span>

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

### <span data-ttu-id="0246c-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="0246c-123">-ContainerName</span></span>
<span data-ttu-id="0246c-124">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="0246c-124">Container Name</span></span>

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

### <span data-ttu-id="0246c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0246c-125">-DefaultProfile</span></span>
<span data-ttu-id="0246c-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0246c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0246c-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="0246c-127">-Etag</span></span>
<span data-ttu-id="0246c-128">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="0246c-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="0246c-129">-Force</span><span class="sxs-lookup"><span data-stu-id="0246c-129">-Force</span></span>
<span data-ttu-id="0246c-130">Tvinga att ta bort ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="0246c-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="0246c-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0246c-131">-InputObject</span></span>
<span data-ttu-id="0246c-132">ImmutabilityPolicy-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="0246c-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="0246c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0246c-133">-ResourceGroupName</span></span>
<span data-ttu-id="0246c-134">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="0246c-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="0246c-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0246c-135">-StorageAccount</span></span>
<span data-ttu-id="0246c-136">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="0246c-136">Storage account object</span></span>

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

### <span data-ttu-id="0246c-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0246c-137">-StorageAccountName</span></span>
<span data-ttu-id="0246c-138">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="0246c-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="0246c-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0246c-139">-Confirm</span></span>
<span data-ttu-id="0246c-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0246c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0246c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0246c-141">-WhatIf</span></span>
<span data-ttu-id="0246c-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0246c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0246c-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0246c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0246c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0246c-144">CommonParameters</span></span>
<span data-ttu-id="0246c-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0246c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0246c-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0246c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0246c-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0246c-147">INPUTS</span></span>

### <span data-ttu-id="0246c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0246c-148">System.String</span></span>
<span data-ttu-id="0246c-149">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0246c-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="0246c-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0246c-150">OUTPUTS</span></span>

### <span data-ttu-id="0246c-151">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0246c-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="0246c-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0246c-152">NOTES</span></span>

## <span data-ttu-id="0246c-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0246c-153">RELATED LINKS</span></span>

