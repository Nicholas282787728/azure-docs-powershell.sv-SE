---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 333df1432ed892e75e0b798f1412cb7b0327a334
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272565"
---
# <span data-ttu-id="a80fb-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a80fb-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="a80fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a80fb-102">SYNOPSIS</span></span>
<span data-ttu-id="a80fb-103">Tar bort en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="a80fb-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="a80fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a80fb-104">SYNTAX</span></span>

### <span data-ttu-id="a80fb-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="a80fb-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a80fb-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a80fb-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a80fb-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="a80fb-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a80fb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a80fb-108">DESCRIPTION</span></span>
<span data-ttu-id="a80fb-109">Cmdleten **Remove-AzRmStorageContainer** tar bort en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="a80fb-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="a80fb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a80fb-110">EXAMPLES</span></span>

### <span data-ttu-id="a80fb-111">Exempel 1: ta bort en lagrings-BLOB-behållare med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="a80fb-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="a80fb-112">Det här kommandot tar bort en lagrings-BLOB med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="a80fb-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="a80fb-113">Exempel 2: ta bort en lagrings-BLOB-behållare med lagrings konto objekt och container namn</span><span class="sxs-lookup"><span data-stu-id="a80fb-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="a80fb-114">Det här kommandot tar bort en lagrings-BLOB-behållare med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="a80fb-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="a80fb-115">Exempel 3: ta bort alla lagrings-BLOB-behållare i ett lagrings konto med pipeline</span><span class="sxs-lookup"><span data-stu-id="a80fb-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="a80fb-116">Det här kommandot tar bort alla lagrings-BLOB-behållare i ett lagrings konto med pipeline.</span><span class="sxs-lookup"><span data-stu-id="a80fb-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="a80fb-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a80fb-117">PARAMETERS</span></span>

### <span data-ttu-id="a80fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a80fb-118">-DefaultProfile</span></span>
<span data-ttu-id="a80fb-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a80fb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a80fb-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a80fb-120">-Force</span></span>
<span data-ttu-id="a80fb-121">Tvinga att ta bort behållaren och allt innehåll i den</span><span class="sxs-lookup"><span data-stu-id="a80fb-121">Force to remove the container and all content in it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a80fb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a80fb-122">-InputObject</span></span>
<span data-ttu-id="a80fb-123">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="a80fb-123">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a80fb-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a80fb-124">-Name</span></span>
<span data-ttu-id="a80fb-125">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="a80fb-125">Container Name</span></span>

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

### <span data-ttu-id="a80fb-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a80fb-126">-PassThru</span></span>
<span data-ttu-id="a80fb-127">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="a80fb-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a80fb-128">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="a80fb-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a80fb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a80fb-129">-ResourceGroupName</span></span>
<span data-ttu-id="a80fb-130">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a80fb-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="a80fb-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a80fb-131">-StorageAccount</span></span>
<span data-ttu-id="a80fb-132">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="a80fb-132">Storage account object</span></span>

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

### <span data-ttu-id="a80fb-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a80fb-133">-StorageAccountName</span></span>
<span data-ttu-id="a80fb-134">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a80fb-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="a80fb-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a80fb-135">-Confirm</span></span>
<span data-ttu-id="a80fb-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a80fb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a80fb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a80fb-137">-WhatIf</span></span>
<span data-ttu-id="a80fb-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a80fb-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a80fb-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a80fb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a80fb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a80fb-140">CommonParameters</span></span>
<span data-ttu-id="a80fb-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a80fb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a80fb-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a80fb-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a80fb-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a80fb-143">INPUTS</span></span>

### <span data-ttu-id="a80fb-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a80fb-144">System.String</span></span>

### <span data-ttu-id="a80fb-145">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a80fb-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a80fb-146">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="a80fb-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="a80fb-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a80fb-147">OUTPUTS</span></span>

### <span data-ttu-id="a80fb-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a80fb-148">System.Boolean</span></span>

## <span data-ttu-id="a80fb-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a80fb-149">NOTES</span></span>

## <span data-ttu-id="a80fb-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a80fb-150">RELATED LINKS</span></span>