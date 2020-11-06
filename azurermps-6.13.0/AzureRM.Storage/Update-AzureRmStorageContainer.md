---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
ms.openlocfilehash: 9e4f62ef28d4cbcb22ddb563e558ad5d48733360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578712"
---
# <span data-ttu-id="fdc9a-101">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fdc9a-101">Update-AzureRmStorageContainer</span></span>

## <span data-ttu-id="fdc9a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fdc9a-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc9a-103">Ändrar en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="fdc9a-103">Modifies a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdc9a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fdc9a-104">SYNTAX</span></span>

### <span data-ttu-id="fdc9a-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="fdc9a-105">AccountName (Default)</span></span>
```
Update-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc9a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fdc9a-106">AccountObject</span></span>
```
Update-AzureRmStorageContainer [-Name] <String> -StorageAccount <PSStorageAccount>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc9a-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="fdc9a-107">ContainerObject</span></span>
```
Update-AzureRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdc9a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fdc9a-108">DESCRIPTION</span></span>
<span data-ttu-id="fdc9a-109">Cmdleten **Update-AzureRmStorageContainer** ändrar en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="fdc9a-109">The **Update-AzureRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="fdc9a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fdc9a-110">EXAMPLES</span></span>

### <span data-ttu-id="fdc9a-111">Exempel 1: ändrar en lagrings BLOB-behållares metadata och offentlig åtkomst med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="fdc9a-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"} 
```

<span data-ttu-id="fdc9a-112">Det här kommandot ändrar metadata för en lagrings-BLOB-behållare och offentlig åtkomst med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="fdc9a-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="fdc9a-113">Exempel 2: inaktivera offentlig åtkomst på en lagrings-BLOB med lagrings konto objekt och behållare namn</span><span class="sxs-lookup"><span data-stu-id="fdc9a-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="fdc9a-114">Det här kommandot inaktiverar offentlig åtkomst i en lagrings-BLOB med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="fdc9a-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="fdc9a-115">Exempel 3: Ange offentlig åtkomst som BLOB för alla lagrings-BLOB-behållare i ett lagrings konto med pipeline</span><span class="sxs-lookup"><span data-stu-id="fdc9a-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzureRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="fdc9a-116">Det här kommandot anger offentlig åtkomst som BLOB för alla lagrings-BLOB-behållare i ett lagrings konto med pipeline.</span><span class="sxs-lookup"><span data-stu-id="fdc9a-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="fdc9a-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fdc9a-117">PARAMETERS</span></span>

### <span data-ttu-id="fdc9a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdc9a-118">-DefaultProfile</span></span>
<span data-ttu-id="fdc9a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fdc9a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdc9a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdc9a-120">-InputObject</span></span>
<span data-ttu-id="fdc9a-121">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="fdc9a-121">Storage container object</span></span>

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

### <span data-ttu-id="fdc9a-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fdc9a-122">-Metadata</span></span>
<span data-ttu-id="fdc9a-123">Metadata för behållare</span><span class="sxs-lookup"><span data-stu-id="fdc9a-123">Container Metadata</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc9a-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="fdc9a-124">-Name</span></span>
<span data-ttu-id="fdc9a-125">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="fdc9a-125">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdc9a-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="fdc9a-126">-PublicAccess</span></span>
<span data-ttu-id="fdc9a-127">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="fdc9a-127">Container PublicAccess</span></span>

```yaml
Type: PSPublicAccess
Parameter Sets: (All)
Aliases: 
Accepted values: Container, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc9a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdc9a-128">-ResourceGroupName</span></span>
<span data-ttu-id="fdc9a-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fdc9a-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="fdc9a-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fdc9a-130">-StorageAccount</span></span>
<span data-ttu-id="fdc9a-131">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="fdc9a-131">Storage account object</span></span>

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

### <span data-ttu-id="fdc9a-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fdc9a-132">-StorageAccountName</span></span>
<span data-ttu-id="fdc9a-133">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="fdc9a-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="fdc9a-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fdc9a-134">-Confirm</span></span>
<span data-ttu-id="fdc9a-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fdc9a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdc9a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdc9a-136">-WhatIf</span></span>
<span data-ttu-id="fdc9a-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fdc9a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdc9a-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fdc9a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdc9a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc9a-139">CommonParameters</span></span>
<span data-ttu-id="fdc9a-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdc9a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc9a-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdc9a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc9a-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fdc9a-142">INPUTS</span></span>

### <span data-ttu-id="fdc9a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fdc9a-143">System.String</span></span>

## <span data-ttu-id="fdc9a-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fdc9a-144">OUTPUTS</span></span>

### <span data-ttu-id="fdc9a-145">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="fdc9a-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="fdc9a-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fdc9a-146">NOTES</span></span>

## <span data-ttu-id="fdc9a-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fdc9a-147">RELATED LINKS</span></span>

