---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 879645975636a981ded22a0fe63d398fc4659d85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746239"
---
# <span data-ttu-id="88302-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="88302-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="88302-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88302-102">SYNOPSIS</span></span>
<span data-ttu-id="88302-103">Ändrar en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="88302-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="88302-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88302-104">SYNTAX</span></span>

### <span data-ttu-id="88302-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="88302-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88302-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="88302-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88302-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="88302-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88302-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88302-108">DESCRIPTION</span></span>
<span data-ttu-id="88302-109">Cmdleten **Update-AzRmStorageContainer** ändrar en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="88302-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="88302-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88302-110">EXAMPLES</span></span>

### <span data-ttu-id="88302-111">Exempel 1: ändrar en lagrings BLOB-behållares metadata och offentlig åtkomst med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="88302-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="88302-112">Det här kommandot ändrar metadata för en lagrings-BLOB-behållare och offentlig åtkomst med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="88302-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="88302-113">Exempel 2: inaktivera offentlig åtkomst på en lagrings-BLOB med lagrings konto objekt och behållare namn</span><span class="sxs-lookup"><span data-stu-id="88302-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="88302-114">Det här kommandot inaktiverar offentlig åtkomst i en lagrings-BLOB med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="88302-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="88302-115">Exempel 3: Ange offentlig åtkomst som BLOB för alla lagrings-BLOB-behållare i ett lagrings konto med pipeline</span><span class="sxs-lookup"><span data-stu-id="88302-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="88302-116">Det här kommandot anger offentlig åtkomst som BLOB för alla lagrings-BLOB-behållare i ett lagrings konto med pipeline.</span><span class="sxs-lookup"><span data-stu-id="88302-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="88302-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88302-117">PARAMETERS</span></span>

### <span data-ttu-id="88302-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88302-118">-DefaultProfile</span></span>
<span data-ttu-id="88302-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="88302-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88302-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88302-120">-InputObject</span></span>
<span data-ttu-id="88302-121">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="88302-121">Storage container object</span></span>

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

### <span data-ttu-id="88302-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="88302-122">-Metadata</span></span>
<span data-ttu-id="88302-123">Metadata för behållare</span><span class="sxs-lookup"><span data-stu-id="88302-123">Container Metadata</span></span>

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

### <span data-ttu-id="88302-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="88302-124">-Name</span></span>
<span data-ttu-id="88302-125">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="88302-125">Container Name</span></span>

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

### <span data-ttu-id="88302-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="88302-126">-PublicAccess</span></span>
<span data-ttu-id="88302-127">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="88302-127">Container PublicAccess</span></span>

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

### <span data-ttu-id="88302-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88302-128">-ResourceGroupName</span></span>
<span data-ttu-id="88302-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="88302-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="88302-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="88302-130">-StorageAccount</span></span>
<span data-ttu-id="88302-131">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="88302-131">Storage account object</span></span>

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

### <span data-ttu-id="88302-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="88302-132">-StorageAccountName</span></span>
<span data-ttu-id="88302-133">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="88302-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="88302-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="88302-134">-Confirm</span></span>
<span data-ttu-id="88302-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="88302-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88302-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88302-136">-WhatIf</span></span>
<span data-ttu-id="88302-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="88302-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88302-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="88302-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88302-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88302-139">CommonParameters</span></span>
<span data-ttu-id="88302-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88302-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88302-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88302-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88302-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88302-142">INPUTS</span></span>

### <span data-ttu-id="88302-143">System. String</span><span class="sxs-lookup"><span data-stu-id="88302-143">System.String</span></span>

### <span data-ttu-id="88302-144">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="88302-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="88302-145">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="88302-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="88302-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88302-146">OUTPUTS</span></span>

### <span data-ttu-id="88302-147">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="88302-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="88302-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88302-148">NOTES</span></span>

## <span data-ttu-id="88302-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88302-149">RELATED LINKS</span></span>
