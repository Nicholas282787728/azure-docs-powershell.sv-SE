---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090027"
---
# <span data-ttu-id="b9bc2-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b9bc2-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="b9bc2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="b9bc2-103">Hämtar ImmutabilityPolicy för en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="b9bc2-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="b9bc2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9bc2-104">SYNTAX</span></span>

### <span data-ttu-id="b9bc2-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="b9bc2-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9bc2-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b9bc2-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9bc2-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="b9bc2-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9bc2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9bc2-108">DESCRIPTION</span></span>
<span data-ttu-id="b9bc2-109">Cmdleten **Get-AzRmStorageContainerImmutabilityPolicy** får ImmutabilityPolicy för lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="b9bc2-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="b9bc2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9bc2-110">EXAMPLES</span></span>

### <span data-ttu-id="b9bc2-111">Exempel 1: Hämta ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="b9bc2-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="b9bc2-112">Det här kommandot hämtar ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="b9bc2-113">Exempel 2: Hämta ImmutabilityPolicy för en lagrings-behållare med lagrings konto objekt och container namn</span><span class="sxs-lookup"><span data-stu-id="b9bc2-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="b9bc2-114">Det här kommandot får ImmutabilityPolicy på en lagrings-BLOB med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="b9bc2-115">Exempel 3: Hämta ImmutabilityPolicy för en lagrings-behållare med lagrings behållar objekt</span><span class="sxs-lookup"><span data-stu-id="b9bc2-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="b9bc2-116">Det här kommandot hämtar ImmutabilityPolicy för en lagrings-behållare med lagrings behållar objekt.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="b9bc2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9bc2-117">PARAMETERS</span></span>

### <span data-ttu-id="b9bc2-118">-Container</span><span class="sxs-lookup"><span data-stu-id="b9bc2-118">-Container</span></span>
<span data-ttu-id="b9bc2-119">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="b9bc2-119">Storage container object</span></span>

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

### <span data-ttu-id="b9bc2-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="b9bc2-120">-ContainerName</span></span>
<span data-ttu-id="b9bc2-121">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="b9bc2-121">Container Name</span></span>

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

### <span data-ttu-id="b9bc2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9bc2-122">-DefaultProfile</span></span>
<span data-ttu-id="b9bc2-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9bc2-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="b9bc2-124">-Etag</span></span>
<span data-ttu-id="b9bc2-125">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-125">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9bc2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9bc2-126">-ResourceGroupName</span></span>
<span data-ttu-id="b9bc2-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b9bc2-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b9bc2-128">-StorageAccount</span></span>
<span data-ttu-id="b9bc2-129">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="b9bc2-129">Storage account object</span></span>

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

### <span data-ttu-id="b9bc2-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b9bc2-130">-StorageAccountName</span></span>
<span data-ttu-id="b9bc2-131">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="b9bc2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9bc2-132">CommonParameters</span></span>
<span data-ttu-id="b9bc2-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9bc2-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9bc2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9bc2-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9bc2-135">INPUTS</span></span>

### <span data-ttu-id="b9bc2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b9bc2-136">System.String</span></span>

### <span data-ttu-id="b9bc2-137">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b9bc2-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b9bc2-138">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="b9bc2-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="b9bc2-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9bc2-139">OUTPUTS</span></span>

### <span data-ttu-id="b9bc2-140">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b9bc2-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="b9bc2-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9bc2-141">NOTES</span></span>

## <span data-ttu-id="b9bc2-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9bc2-142">RELATED LINKS</span></span>
