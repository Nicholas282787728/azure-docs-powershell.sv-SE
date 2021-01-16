---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 0cb3a4e65d8e464dda85e18e12dc106620e3eee8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404139"
---
# <span data-ttu-id="8f79d-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8f79d-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="8f79d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f79d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f79d-103">Lås ImmutabilityPolicy för en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="8f79d-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="8f79d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f79d-104">SYNTAX</span></span>

### <span data-ttu-id="8f79d-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="8f79d-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f79d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8f79d-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f79d-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="8f79d-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f79d-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="8f79d-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f79d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f79d-109">DESCRIPTION</span></span>
<span data-ttu-id="8f79d-110">**Lås-AzRmStorageContainerImmutabilityPolicy** cmdlet låser ImmutabilityPolicy i en lagrings-BLOB-behållare.</span><span class="sxs-lookup"><span data-stu-id="8f79d-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="8f79d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f79d-111">EXAMPLES</span></span>

### <span data-ttu-id="8f79d-112">Exempel 1: Lås ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="8f79d-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="8f79d-113">Det här kommandot låser ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="8f79d-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="8f79d-114">Exempel 2: Lås ImmutabilityPolicy för en lagrings-behållare med lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="8f79d-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="8f79d-115">Det här kommandot låser ImmutabilityPolicy för en lagrings-behållare med lagrings konto objekt.</span><span class="sxs-lookup"><span data-stu-id="8f79d-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="8f79d-116">Exempel 3: Lås ImmutabilityPolicyof en BLOB-behållare för lagring, med behållar-objekt</span><span class="sxs-lookup"><span data-stu-id="8f79d-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="8f79d-117">Det här kommandot låser ImmutabilityPolicy för en lagrings-behållare med lagrings Container objekt.</span><span class="sxs-lookup"><span data-stu-id="8f79d-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="8f79d-118">Exempel 4: Lås ImmutabilityPolicy för en lagrings-behållare med ImmutabilityPolicy-objekt</span><span class="sxs-lookup"><span data-stu-id="8f79d-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="8f79d-119">Det här kommandot låser ImmutabilityPolicy för en lagrings-behållare med ImmutabilityPolicy-objekt.</span><span class="sxs-lookup"><span data-stu-id="8f79d-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="8f79d-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f79d-120">PARAMETERS</span></span>

### <span data-ttu-id="8f79d-121">-Container</span><span class="sxs-lookup"><span data-stu-id="8f79d-121">-Container</span></span>
<span data-ttu-id="8f79d-122">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="8f79d-122">Storage container object</span></span>

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

### <span data-ttu-id="8f79d-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8f79d-123">-ContainerName</span></span>
<span data-ttu-id="8f79d-124">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="8f79d-124">Container Name</span></span>

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

### <span data-ttu-id="8f79d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f79d-125">-DefaultProfile</span></span>
<span data-ttu-id="8f79d-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8f79d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f79d-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="8f79d-127">-Etag</span></span>
<span data-ttu-id="8f79d-128">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="8f79d-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="8f79d-129">-Force</span><span class="sxs-lookup"><span data-stu-id="8f79d-129">-Force</span></span>
<span data-ttu-id="8f79d-130">Tvinga att ta bort ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="8f79d-130">Force to remove the ImmutabilityPolicy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f79d-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f79d-131">-InputObject</span></span>
<span data-ttu-id="8f79d-132">ImmutabilityPolicy-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="8f79d-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="8f79d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f79d-133">-ResourceGroupName</span></span>
<span data-ttu-id="8f79d-134">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="8f79d-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="8f79d-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8f79d-135">-StorageAccount</span></span>
<span data-ttu-id="8f79d-136">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="8f79d-136">Storage account object</span></span>

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

### <span data-ttu-id="8f79d-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8f79d-137">-StorageAccountName</span></span>
<span data-ttu-id="8f79d-138">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="8f79d-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="8f79d-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f79d-139">-Confirm</span></span>
<span data-ttu-id="8f79d-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f79d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f79d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f79d-141">-WhatIf</span></span>
<span data-ttu-id="8f79d-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f79d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f79d-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f79d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f79d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f79d-144">CommonParameters</span></span>
<span data-ttu-id="8f79d-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f79d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f79d-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f79d-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f79d-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f79d-147">INPUTS</span></span>

### <span data-ttu-id="8f79d-148">System. String</span><span class="sxs-lookup"><span data-stu-id="8f79d-148">System.String</span></span>

### <span data-ttu-id="8f79d-149">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8f79d-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8f79d-150">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="8f79d-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="8f79d-151">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8f79d-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="8f79d-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f79d-152">OUTPUTS</span></span>

### <span data-ttu-id="8f79d-153">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8f79d-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="8f79d-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f79d-154">NOTES</span></span>

## <span data-ttu-id="8f79d-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f79d-155">RELATED LINKS</span></span>
