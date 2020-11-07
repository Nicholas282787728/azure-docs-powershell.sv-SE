---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: f15d9905abbc7a61dc77d4e8b28c5942126d7b14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746418"
---
# <span data-ttu-id="02286-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="02286-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="02286-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02286-102">SYNOPSIS</span></span>
<span data-ttu-id="02286-103">Hämtar eller visar en lista över BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="02286-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="02286-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02286-104">SYNTAX</span></span>

### <span data-ttu-id="02286-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="02286-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02286-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="02286-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02286-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02286-107">DESCRIPTION</span></span>
<span data-ttu-id="02286-108">Cmdleten **Get-AzRmStorageContainer** hämtar eller visar en lista över BLOB-behållare för lagring</span><span class="sxs-lookup"><span data-stu-id="02286-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="02286-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02286-109">EXAMPLES</span></span>

### <span data-ttu-id="02286-110">Exempel 1: Hämta en lagrings-BLOB med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="02286-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="02286-111">Det här kommandot får en lagrings-BLOB-behållare med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="02286-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="02286-112">Exempel 2: lista alla lagrings-BLOB-behållare för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="02286-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="02286-113">Det här kommandot listar alla lagrings-BLOB-behållare för ett lagrings konto med lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="02286-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="02286-114">Exempel 3: skaffa en lagrings-BLOB-behållare med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="02286-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="02286-115">Det här kommandot får en lagrings-BLOB-behållare med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="02286-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="02286-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02286-116">PARAMETERS</span></span>

### <span data-ttu-id="02286-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02286-117">-DefaultProfile</span></span>
<span data-ttu-id="02286-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02286-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02286-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="02286-119">-Name</span></span>
<span data-ttu-id="02286-120">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="02286-120">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02286-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02286-121">-ResourceGroupName</span></span>
<span data-ttu-id="02286-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="02286-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="02286-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="02286-123">-StorageAccount</span></span>
<span data-ttu-id="02286-124">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="02286-124">Storage account object</span></span>

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

### <span data-ttu-id="02286-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="02286-125">-StorageAccountName</span></span>
<span data-ttu-id="02286-126">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="02286-126">Storage Account Name.</span></span>

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

### <span data-ttu-id="02286-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02286-127">CommonParameters</span></span>
<span data-ttu-id="02286-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02286-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02286-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02286-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02286-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02286-130">INPUTS</span></span>

### <span data-ttu-id="02286-131">System. String</span><span class="sxs-lookup"><span data-stu-id="02286-131">System.String</span></span>

### <span data-ttu-id="02286-132">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="02286-132">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="02286-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02286-133">OUTPUTS</span></span>

### <span data-ttu-id="02286-134">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="02286-134">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="02286-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02286-135">NOTES</span></span>

## <span data-ttu-id="02286-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02286-136">RELATED LINKS</span></span>
