---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: f54196ef5b055a5e1968c682d21f861ee41c77ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920807"
---
# <span data-ttu-id="7d109-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7d109-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="7d109-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d109-102">SYNOPSIS</span></span>
<span data-ttu-id="7d109-103">Hämtar eller visar lagrings fil resurser.</span><span class="sxs-lookup"><span data-stu-id="7d109-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="7d109-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d109-104">SYNTAX</span></span>

### <span data-ttu-id="7d109-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="7d109-105">AccountName (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d109-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="7d109-106">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d109-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="7d109-107">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d109-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d109-108">DESCRIPTION</span></span>
<span data-ttu-id="7d109-109">Cmdleten **Get-AzRmStorageShare** hämtar eller visar en lista över lagrings fil resurser.</span><span class="sxs-lookup"><span data-stu-id="7d109-109">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="7d109-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d109-110">EXAMPLES</span></span>

### <span data-ttu-id="7d109-111">Exempel 1: Hämta en lagrings fil med lagrings konto namn och resurs namn</span><span class="sxs-lookup"><span data-stu-id="7d109-111">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="7d109-112">Det här kommandot får en lagrings fil resurs med namn på lagrings konto och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="7d109-112">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="7d109-113">Exempel 2: lista alla lagrings fil resurser för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="7d109-113">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
share2   myStorageAccount   myResourceGroup   "0x8D6FF862774FE57" 5120     2019-07-03 07:14:57Z
```

<span data-ttu-id="7d109-114">Det här kommandot visar alla lagrings fil resurser för ett lagrings konto med lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="7d109-114">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="7d109-115">Exempel 3: skaffa en lagrings-BLOB-behållare med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="7d109-115">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Get-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="7d109-116">Det här kommandot får en lagrings-BLOB-behållare med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="7d109-116">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="7d109-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d109-117">PARAMETERS</span></span>

### <span data-ttu-id="7d109-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d109-118">-DefaultProfile</span></span>
<span data-ttu-id="7d109-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d109-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d109-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d109-120">-Name</span></span>
<span data-ttu-id="7d109-121">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="7d109-121">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d109-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d109-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d109-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7d109-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="7d109-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d109-124">-ResourceId</span></span>
<span data-ttu-id="7d109-125">Ange ett resurs-ID för fildelning.</span><span class="sxs-lookup"><span data-stu-id="7d109-125">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d109-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d109-126">-StorageAccount</span></span>
<span data-ttu-id="7d109-127">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="7d109-127">Storage account object</span></span>

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

### <span data-ttu-id="7d109-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7d109-128">-StorageAccountName</span></span>
<span data-ttu-id="7d109-129">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="7d109-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="7d109-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d109-130">CommonParameters</span></span>
<span data-ttu-id="7d109-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d109-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d109-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d109-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d109-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d109-133">INPUTS</span></span>

### <span data-ttu-id="7d109-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7d109-134">System.String</span></span>

### <span data-ttu-id="7d109-135">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d109-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="7d109-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d109-136">OUTPUTS</span></span>

### <span data-ttu-id="7d109-137">Microsoft. Azure. commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="7d109-137">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="7d109-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d109-138">NOTES</span></span>

## <span data-ttu-id="7d109-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d109-139">RELATED LINKS</span></span>
