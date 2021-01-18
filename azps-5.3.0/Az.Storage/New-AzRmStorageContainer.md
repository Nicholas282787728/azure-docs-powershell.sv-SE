---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 901061390c68853832bad14965620abad21817e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522734"
---
# <span data-ttu-id="6b007-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6b007-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="6b007-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b007-102">SYNOPSIS</span></span>
<span data-ttu-id="6b007-103">Skapar en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="6b007-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="6b007-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b007-104">SYNTAX</span></span>

### <span data-ttu-id="6b007-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="6b007-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b007-106">AccountNameEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="6b007-106">AccountNameEncryptionScope</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b007-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6b007-107">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b007-108">AccountObjectEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="6b007-108">AccountObjectEncryptionScope</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> -DefaultEncryptionScope <String>
 -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b007-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b007-109">DESCRIPTION</span></span>
<span data-ttu-id="6b007-110">Cmdleten **New-AzRmStorageContainer** skapar en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="6b007-110">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="6b007-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b007-111">EXAMPLES</span></span>

### <span data-ttu-id="6b007-112">Exempel 1: skapa en lagrings-BLOB-behållare med lagrings konto namn och container namn, med metadata</span><span class="sxs-lookup"><span data-stu-id="6b007-112">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="6b007-113">Det här kommandot skapar en lagrings-BLOB-behållare med lagrings konto namn och container namn, med metadata.</span><span class="sxs-lookup"><span data-stu-id="6b007-113">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="6b007-114">Exempel 2: skapa en lagrings-BLOB-behållare med lagrings konto objekt och container namn, med offentlig åtkomst som BLOB</span><span class="sxs-lookup"><span data-stu-id="6b007-114">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="6b007-115">Det här kommandot skapar en lagrings-BLOB-behållare med lagrings konto objekt och container namn, med offentlig åtkomst som blob.</span><span class="sxs-lookup"><span data-stu-id="6b007-115">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

### <span data-ttu-id="6b007-116">Exempel 3: skapa en lagrings behållare med EncryptionScope inställning</span><span class="sxs-lookup"><span data-stu-id="6b007-116">Example 3: Create a storage container with EncryptionScope setting</span></span>
```
PS C:\> $c = New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name testcontainer -DefaultEncryptionScope "testscope" -PreventEncryptionScopeOverride $true

PS C:\> $c

   ResourceGroupName: myResourceGroup, StorageAccountName: myStorageAccount

Name          PublicAccess LastModified HasLegalHold HasImmutabilityPolicy
----          ------------ ------------ ------------ ---------------------
testcontainer                           False        False                

PS C:\> $c.DefaultEncryptionScope
testscope

PS C:\> $c.DenyEncryptionScopeOverride
True
```

<span data-ttu-id="6b007-117">Det här kommandot skapar en lagrings behållare med en defalt-encryptionScope och blockerar blockering av krypterings omfång från standard behållaren.</span><span class="sxs-lookup"><span data-stu-id="6b007-117">This command creates a storage container with a defalt encryptionScope, and blocks override of encryption scope from the container default.</span></span>
<span data-ttu-id="6b007-118">Visa sedan de relaterade egenskaperna för behållaren.</span><span class="sxs-lookup"><span data-stu-id="6b007-118">Then show the related container properties.</span></span>

## <span data-ttu-id="6b007-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b007-119">PARAMETERS</span></span>

### <span data-ttu-id="6b007-120">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="6b007-120">-DefaultEncryptionScope</span></span>
<span data-ttu-id="6b007-121">Använd den angivna krypterings omfattningen för alla skrivningar.</span><span class="sxs-lookup"><span data-stu-id="6b007-121">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b007-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b007-122">-DefaultProfile</span></span>
<span data-ttu-id="6b007-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b007-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b007-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6b007-124">-Metadata</span></span>
<span data-ttu-id="6b007-125">Metadata för behållare</span><span class="sxs-lookup"><span data-stu-id="6b007-125">Container Metadata</span></span>

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

### <span data-ttu-id="6b007-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="6b007-126">-Name</span></span>
<span data-ttu-id="6b007-127">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="6b007-127">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b007-128">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="6b007-128">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="6b007-129">Blockera åsidosättning av krypterings omfång från standard behållare.</span><span class="sxs-lookup"><span data-stu-id="6b007-129">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b007-130">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="6b007-130">-PublicAccess</span></span>
<span data-ttu-id="6b007-131">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="6b007-131">Container PublicAccess</span></span>

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

### <span data-ttu-id="6b007-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b007-132">-ResourceGroupName</span></span>
<span data-ttu-id="6b007-133">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6b007-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b007-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b007-134">-StorageAccount</span></span>
<span data-ttu-id="6b007-135">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="6b007-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b007-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6b007-136">-StorageAccountName</span></span>
<span data-ttu-id="6b007-137">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6b007-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b007-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6b007-138">-Confirm</span></span>
<span data-ttu-id="6b007-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b007-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b007-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b007-140">-WhatIf</span></span>
<span data-ttu-id="6b007-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6b007-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b007-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6b007-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b007-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b007-143">CommonParameters</span></span>
<span data-ttu-id="6b007-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b007-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b007-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b007-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b007-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b007-146">INPUTS</span></span>

### <span data-ttu-id="6b007-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6b007-147">System.String</span></span>

### <span data-ttu-id="6b007-148">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b007-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="6b007-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b007-149">OUTPUTS</span></span>

### <span data-ttu-id="6b007-150">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="6b007-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="6b007-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b007-151">NOTES</span></span>

## <span data-ttu-id="6b007-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b007-152">RELATED LINKS</span></span>
