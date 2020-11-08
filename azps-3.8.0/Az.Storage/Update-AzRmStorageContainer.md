---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 3ece496830cf3d6b1618bd410e2352d65f6e2fad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089220"
---
# <span data-ttu-id="4d728-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4d728-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="4d728-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d728-102">SYNOPSIS</span></span>
<span data-ttu-id="4d728-103">Ändrar en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="4d728-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="4d728-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d728-104">SYNTAX</span></span>

### <span data-ttu-id="4d728-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="4d728-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d728-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4d728-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d728-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="4d728-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d728-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d728-108">DESCRIPTION</span></span>
<span data-ttu-id="4d728-109">Cmdleten **Update-AzRmStorageContainer** ändrar en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="4d728-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="4d728-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d728-110">EXAMPLES</span></span>

### <span data-ttu-id="4d728-111">Exempel 1: ändrar en lagrings BLOB-behållares metadata och offentlig åtkomst med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="4d728-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="4d728-112">Det här kommandot ändrar metadata för en lagrings-BLOB-behållare och offentlig åtkomst med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="4d728-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="4d728-113">Exempel 2: inaktivera offentlig åtkomst på en lagrings-BLOB med lagrings konto objekt och behållare namn</span><span class="sxs-lookup"><span data-stu-id="4d728-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="4d728-114">Det här kommandot inaktiverar offentlig åtkomst i en lagrings-BLOB med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="4d728-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="4d728-115">Exempel 3: Ange offentlig åtkomst som BLOB för alla lagrings-BLOB-behållare i ett lagrings konto med pipeline</span><span class="sxs-lookup"><span data-stu-id="4d728-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="4d728-116">Det här kommandot anger offentlig åtkomst som BLOB för alla lagrings-BLOB-behållare i ett lagrings konto med pipeline.</span><span class="sxs-lookup"><span data-stu-id="4d728-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="4d728-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d728-117">PARAMETERS</span></span>

### <span data-ttu-id="4d728-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d728-118">-DefaultProfile</span></span>
<span data-ttu-id="4d728-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d728-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d728-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d728-120">-InputObject</span></span>
<span data-ttu-id="4d728-121">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="4d728-121">Storage container object</span></span>

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

### <span data-ttu-id="4d728-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4d728-122">-Metadata</span></span>
<span data-ttu-id="4d728-123">Metadata för behållare</span><span class="sxs-lookup"><span data-stu-id="4d728-123">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d728-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d728-124">-Name</span></span>
<span data-ttu-id="4d728-125">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="4d728-125">Container Name</span></span>

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

### <span data-ttu-id="4d728-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="4d728-126">-PublicAccess</span></span>
<span data-ttu-id="4d728-127">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="4d728-127">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d728-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d728-128">-ResourceGroupName</span></span>
<span data-ttu-id="4d728-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4d728-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="4d728-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4d728-130">-StorageAccount</span></span>
<span data-ttu-id="4d728-131">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="4d728-131">Storage account object</span></span>

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

### <span data-ttu-id="4d728-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4d728-132">-StorageAccountName</span></span>
<span data-ttu-id="4d728-133">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="4d728-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="4d728-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d728-134">-Confirm</span></span>
<span data-ttu-id="4d728-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d728-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d728-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d728-136">-WhatIf</span></span>
<span data-ttu-id="4d728-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d728-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d728-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d728-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d728-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d728-139">CommonParameters</span></span>
<span data-ttu-id="4d728-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d728-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d728-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d728-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d728-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d728-142">INPUTS</span></span>

### <span data-ttu-id="4d728-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4d728-143">System.String</span></span>

### <span data-ttu-id="4d728-144">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4d728-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="4d728-145">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="4d728-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="4d728-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d728-146">OUTPUTS</span></span>

### <span data-ttu-id="4d728-147">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="4d728-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="4d728-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d728-148">NOTES</span></span>

## <span data-ttu-id="4d728-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d728-149">RELATED LINKS</span></span>
