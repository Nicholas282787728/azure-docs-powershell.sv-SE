---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: cff5f387b6729f51634ee0466b099e1df8314589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583399"
---
# <span data-ttu-id="ca972-101">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ca972-101">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="ca972-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca972-102">SYNOPSIS</span></span>
<span data-ttu-id="ca972-103">Hämtar ImmutabilityPolicy för en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="ca972-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca972-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca972-104">SYNTAX</span></span>

### <span data-ttu-id="ca972-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="ca972-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca972-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ca972-106">AccountObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca972-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="ca972-107">ContainerObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca972-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca972-108">DESCRIPTION</span></span>
<span data-ttu-id="ca972-109">Cmdleten **Get-AzureRmStorageContainerImmutabilityPolicy** får ImmutabilityPolicy för lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="ca972-109">The **Get-AzureRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="ca972-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca972-110">EXAMPLES</span></span>

### <span data-ttu-id="ca972-111">Exempel 1: Hämta ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="ca972-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="ca972-112">Det här kommandot hämtar ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="ca972-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="ca972-113">Exempel 2: Hämta ImmutabilityPolicy för en lagrings-behållare med lagrings konto objekt och container namn</span><span class="sxs-lookup"><span data-stu-id="ca972-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="ca972-114">Det här kommandot får ImmutabilityPolicy på en lagrings-BLOB med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="ca972-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="ca972-115">Exempel 3: Hämta ImmutabilityPolicy för en lagrings-behållare med lagrings behållar objekt</span><span class="sxs-lookup"><span data-stu-id="ca972-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject 
```

<span data-ttu-id="ca972-116">Det här kommandot hämtar ImmutabilityPolicy för en lagrings-behållare med lagrings behållar objekt.</span><span class="sxs-lookup"><span data-stu-id="ca972-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="ca972-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca972-117">PARAMETERS</span></span>

### <span data-ttu-id="ca972-118">-Container</span><span class="sxs-lookup"><span data-stu-id="ca972-118">-Container</span></span>
<span data-ttu-id="ca972-119">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="ca972-119">Storage container object</span></span>

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

### <span data-ttu-id="ca972-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ca972-120">-ContainerName</span></span>
<span data-ttu-id="ca972-121">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="ca972-121">Container Name</span></span>

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

### <span data-ttu-id="ca972-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca972-122">-DefaultProfile</span></span>
<span data-ttu-id="ca972-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ca972-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca972-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="ca972-124">-Etag</span></span>
<span data-ttu-id="ca972-125">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="ca972-125">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca972-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca972-126">-ResourceGroupName</span></span>
<span data-ttu-id="ca972-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ca972-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="ca972-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca972-128">-StorageAccount</span></span>
<span data-ttu-id="ca972-129">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="ca972-129">Storage account object</span></span>

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

### <span data-ttu-id="ca972-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ca972-130">-StorageAccountName</span></span>
<span data-ttu-id="ca972-131">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ca972-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="ca972-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca972-132">CommonParameters</span></span>
<span data-ttu-id="ca972-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca972-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca972-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca972-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca972-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca972-135">INPUTS</span></span>

### <span data-ttu-id="ca972-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ca972-136">System.String</span></span>

## <span data-ttu-id="ca972-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca972-137">OUTPUTS</span></span>

### <span data-ttu-id="ca972-138">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ca972-138">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="ca972-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca972-139">NOTES</span></span>

## <span data-ttu-id="ca972-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca972-140">RELATED LINKS</span></span>

