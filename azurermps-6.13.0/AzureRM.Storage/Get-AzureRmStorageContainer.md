---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
ms.openlocfilehash: 64e3857ddd9a9bb00b94e3e550c6be33722990a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573857"
---
# <span data-ttu-id="0d192-101">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0d192-101">Get-AzureRmStorageContainer</span></span>

## <span data-ttu-id="0d192-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d192-102">SYNOPSIS</span></span>
<span data-ttu-id="0d192-103">Hämtar eller visar en lista över BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="0d192-103">Gets or lists Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d192-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d192-104">SYNTAX</span></span>

### <span data-ttu-id="0d192-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="0d192-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d192-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0d192-106">AccountObject</span></span>
```
Get-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d192-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d192-107">DESCRIPTION</span></span>
<span data-ttu-id="0d192-108">Cmdleten **Get-AzureRmStorageContainer** hämtar eller visar en lista över BLOB-behållare för lagring</span><span class="sxs-lookup"><span data-stu-id="0d192-108">The **Get-AzureRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="0d192-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d192-109">EXAMPLES</span></span>

### <span data-ttu-id="0d192-110">Exempel 1: Hämta en lagrings-BLOB med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="0d192-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" 
```

<span data-ttu-id="0d192-111">Det här kommandot får en lagrings-BLOB-behållare med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="0d192-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="0d192-112">Exempel 2: lista alla lagrings-BLOB-behållare för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="0d192-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" 
```

<span data-ttu-id="0d192-113">Det här kommandot listar alla lagrings-BLOB-behållare för ett lagrings konto med lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="0d192-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="0d192-114">Exempel 3: skaffa en lagrings-BLOB-behållare med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="0d192-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" 
```

<span data-ttu-id="0d192-115">Det här kommandot får en lagrings-BLOB-behållare med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="0d192-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="0d192-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d192-116">PARAMETERS</span></span>

### <span data-ttu-id="0d192-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d192-117">-DefaultProfile</span></span>
<span data-ttu-id="0d192-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d192-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d192-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="0d192-119">-Name</span></span>
<span data-ttu-id="0d192-120">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="0d192-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d192-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d192-121">-ResourceGroupName</span></span>
<span data-ttu-id="0d192-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="0d192-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="0d192-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0d192-123">-StorageAccount</span></span>
<span data-ttu-id="0d192-124">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="0d192-124">Storage account object</span></span>

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

### <span data-ttu-id="0d192-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0d192-125">-StorageAccountName</span></span>
<span data-ttu-id="0d192-126">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="0d192-126">Storage Account Name.</span></span>

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

### <span data-ttu-id="0d192-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d192-127">CommonParameters</span></span>
<span data-ttu-id="0d192-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d192-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d192-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d192-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d192-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d192-130">INPUTS</span></span>

### <span data-ttu-id="0d192-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0d192-131">System.String</span></span>

## <span data-ttu-id="0d192-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d192-132">OUTPUTS</span></span>

### <span data-ttu-id="0d192-133">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="0d192-133">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="0d192-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d192-134">NOTES</span></span>

## <span data-ttu-id="0d192-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d192-135">RELATED LINKS</span></span>

