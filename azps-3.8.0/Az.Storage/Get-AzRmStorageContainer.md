---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: da0ccdc791318f0a315bea8d2464d8d0852aec8b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090030"
---
# <span data-ttu-id="4be86-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4be86-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="4be86-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4be86-102">SYNOPSIS</span></span>
<span data-ttu-id="4be86-103">Hämtar eller visar en lista över BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="4be86-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="4be86-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4be86-104">SYNTAX</span></span>

### <span data-ttu-id="4be86-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="4be86-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4be86-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4be86-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4be86-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4be86-107">DESCRIPTION</span></span>
<span data-ttu-id="4be86-108">Cmdleten **Get-AzRmStorageContainer** hämtar eller visar en lista över BLOB-behållare för lagring</span><span class="sxs-lookup"><span data-stu-id="4be86-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="4be86-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4be86-109">EXAMPLES</span></span>

### <span data-ttu-id="4be86-110">Exempel 1: Hämta en lagrings-BLOB med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="4be86-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="4be86-111">Det här kommandot får en lagrings-BLOB-behållare med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="4be86-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="4be86-112">Exempel 2: lista alla lagrings-BLOB-behållare för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="4be86-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="4be86-113">Det här kommandot listar alla lagrings-BLOB-behållare för ett lagrings konto med lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="4be86-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="4be86-114">Exempel 3: skaffa en lagrings-BLOB-behållare med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="4be86-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="4be86-115">Det här kommandot får en lagrings-BLOB-behållare med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="4be86-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="4be86-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4be86-116">PARAMETERS</span></span>

### <span data-ttu-id="4be86-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4be86-117">-AsJob</span></span>
<span data-ttu-id="4be86-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4be86-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4be86-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be86-119">-DefaultProfile</span></span>
<span data-ttu-id="4be86-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4be86-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4be86-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="4be86-121">-Name</span></span>
<span data-ttu-id="4be86-122">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="4be86-122">Container Name</span></span>

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

### <span data-ttu-id="4be86-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4be86-123">-ResourceGroupName</span></span>
<span data-ttu-id="4be86-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4be86-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="4be86-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4be86-125">-StorageAccount</span></span>
<span data-ttu-id="4be86-126">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="4be86-126">Storage account object</span></span>

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

### <span data-ttu-id="4be86-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4be86-127">-StorageAccountName</span></span>
<span data-ttu-id="4be86-128">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="4be86-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="4be86-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be86-129">CommonParameters</span></span>
<span data-ttu-id="4be86-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4be86-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be86-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4be86-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be86-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4be86-132">INPUTS</span></span>

### <span data-ttu-id="4be86-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4be86-133">System.String</span></span>

### <span data-ttu-id="4be86-134">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4be86-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="4be86-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4be86-135">OUTPUTS</span></span>

### <span data-ttu-id="4be86-136">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="4be86-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="4be86-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4be86-137">NOTES</span></span>

## <span data-ttu-id="4be86-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4be86-138">RELATED LINKS</span></span>
