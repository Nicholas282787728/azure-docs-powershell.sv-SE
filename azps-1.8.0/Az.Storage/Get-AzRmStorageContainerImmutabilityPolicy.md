---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2b324d1b038a6ab97e4e68303bd98570fe0704ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746413"
---
# <span data-ttu-id="460fd-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="460fd-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="460fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="460fd-102">SYNOPSIS</span></span>
<span data-ttu-id="460fd-103">Hämtar ImmutabilityPolicy för en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="460fd-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="460fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="460fd-104">SYNTAX</span></span>

### <span data-ttu-id="460fd-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="460fd-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="460fd-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="460fd-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="460fd-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="460fd-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="460fd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="460fd-108">DESCRIPTION</span></span>
<span data-ttu-id="460fd-109">Cmdleten **Get-AzRmStorageContainerImmutabilityPolicy** får ImmutabilityPolicy för lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="460fd-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="460fd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="460fd-110">EXAMPLES</span></span>

### <span data-ttu-id="460fd-111">Exempel 1: Hämta ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="460fd-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="460fd-112">Det här kommandot hämtar ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="460fd-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="460fd-113">Exempel 2: Hämta ImmutabilityPolicy för en lagrings-behållare med lagrings konto objekt och container namn</span><span class="sxs-lookup"><span data-stu-id="460fd-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="460fd-114">Det här kommandot får ImmutabilityPolicy på en lagrings-BLOB med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="460fd-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="460fd-115">Exempel 3: Hämta ImmutabilityPolicy för en lagrings-behållare med lagrings behållar objekt</span><span class="sxs-lookup"><span data-stu-id="460fd-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="460fd-116">Det här kommandot hämtar ImmutabilityPolicy för en lagrings-behållare med lagrings behållar objekt.</span><span class="sxs-lookup"><span data-stu-id="460fd-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="460fd-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="460fd-117">PARAMETERS</span></span>

### <span data-ttu-id="460fd-118">-Container</span><span class="sxs-lookup"><span data-stu-id="460fd-118">-Container</span></span>
<span data-ttu-id="460fd-119">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="460fd-119">Storage container object</span></span>

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

### <span data-ttu-id="460fd-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="460fd-120">-ContainerName</span></span>
<span data-ttu-id="460fd-121">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="460fd-121">Container Name</span></span>

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

### <span data-ttu-id="460fd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="460fd-122">-DefaultProfile</span></span>
<span data-ttu-id="460fd-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="460fd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="460fd-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="460fd-124">-Etag</span></span>
<span data-ttu-id="460fd-125">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="460fd-125">Immutability policy etag.</span></span>

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

### <span data-ttu-id="460fd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="460fd-126">-ResourceGroupName</span></span>
<span data-ttu-id="460fd-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="460fd-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="460fd-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="460fd-128">-StorageAccount</span></span>
<span data-ttu-id="460fd-129">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="460fd-129">Storage account object</span></span>

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

### <span data-ttu-id="460fd-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="460fd-130">-StorageAccountName</span></span>
<span data-ttu-id="460fd-131">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="460fd-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="460fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="460fd-132">CommonParameters</span></span>
<span data-ttu-id="460fd-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="460fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="460fd-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="460fd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="460fd-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="460fd-135">INPUTS</span></span>

### <span data-ttu-id="460fd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="460fd-136">System.String</span></span>

### <span data-ttu-id="460fd-137">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="460fd-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="460fd-138">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="460fd-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="460fd-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="460fd-139">OUTPUTS</span></span>

### <span data-ttu-id="460fd-140">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="460fd-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="460fd-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="460fd-141">NOTES</span></span>

## <span data-ttu-id="460fd-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="460fd-142">RELATED LINKS</span></span>
