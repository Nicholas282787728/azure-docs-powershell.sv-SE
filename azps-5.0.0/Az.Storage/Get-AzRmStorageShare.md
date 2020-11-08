---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 90edd254eb77b03f4f4d26761020d71025960426
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272991"
---
# <span data-ttu-id="f165f-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f165f-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="f165f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f165f-102">SYNOPSIS</span></span>
<span data-ttu-id="f165f-103">Hämtar eller visar lagrings fil resurser.</span><span class="sxs-lookup"><span data-stu-id="f165f-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="f165f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f165f-104">SYNTAX</span></span>

### <span data-ttu-id="f165f-105">AccountNameSingle (standard)</span><span class="sxs-lookup"><span data-stu-id="f165f-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f165f-106">Konto</span><span class="sxs-lookup"><span data-stu-id="f165f-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f165f-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="f165f-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f165f-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f165f-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f165f-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="f165f-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f165f-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f165f-110">DESCRIPTION</span></span>
<span data-ttu-id="f165f-111">Cmdleten **Get-AzRmStorageShare** hämtar eller visar en lista över lagrings fil resurser.</span><span class="sxs-lookup"><span data-stu-id="f165f-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="f165f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f165f-112">EXAMPLES</span></span>

### <span data-ttu-id="f165f-113">Exempel 1: Hämta en lagrings fil med lagrings konto namn och resurs namn</span><span class="sxs-lookup"><span data-stu-id="f165f-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="f165f-114">Det här kommandot får en lagrings fil resurs med namn på lagrings konto och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="f165f-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="f165f-115">Exempel 2: lista alla lagrings fil resurser för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="f165f-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="f165f-116">Det här kommandot visar alla lagrings fil resurser för ett lagrings konto med lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="f165f-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="f165f-117">Exempel 3: skaffa en lagrings-BLOB-behållare med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="f165f-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="f165f-118">Det här kommandot får en lagrings-BLOB-behållare med lagrings konto objekt och container namn.</span><span class="sxs-lookup"><span data-stu-id="f165f-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="f165f-119">Exempel 4: Hämta en lagrings fil med delnings funktionen i byte</span><span class="sxs-lookup"><span data-stu-id="f165f-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="f165f-120">Det här kommandot får en lagrings fil resurs med namn på lagrings konto och resurs namn och inkluderar delnings användning i byte.</span><span class="sxs-lookup"><span data-stu-id="f165f-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="f165f-121">Exempel 5: lista alla lagrings fil resurser för ett lagrings konto, inklusive borttagna resurser</span><span class="sxs-lookup"><span data-stu-id="f165f-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="f165f-122">Det här kommandot listar alla lagrings fil resurser inkluderar borttagna delar av ett lagrings konto med lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="f165f-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="f165f-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f165f-123">PARAMETERS</span></span>

### <span data-ttu-id="f165f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f165f-124">-DefaultProfile</span></span>
<span data-ttu-id="f165f-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f165f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f165f-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="f165f-126">-GetShareUsage</span></span>
<span data-ttu-id="f165f-127">Ange den här parametern för att få delnings användning i byte.</span><span class="sxs-lookup"><span data-stu-id="f165f-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameSingle, AccountObjectSingle, ShareResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f165f-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="f165f-128">-IncludeDeleted</span></span>
<span data-ttu-id="f165f-129">Ta med borttagna resurser, som standard innehåller inte borttagna resurser</span><span class="sxs-lookup"><span data-stu-id="f165f-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f165f-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="f165f-130">-Name</span></span>
<span data-ttu-id="f165f-131">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="f165f-131">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, ShareResourceId
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountObjectSingle
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f165f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f165f-132">-ResourceGroupName</span></span>
<span data-ttu-id="f165f-133">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f165f-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f165f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f165f-134">-ResourceId</span></span>
<span data-ttu-id="f165f-135">Ange ett resurs-ID för fildelning.</span><span class="sxs-lookup"><span data-stu-id="f165f-135">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="f165f-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f165f-136">-StorageAccount</span></span>
<span data-ttu-id="f165f-137">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="f165f-137">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectSingle, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f165f-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f165f-138">-StorageAccountName</span></span>
<span data-ttu-id="f165f-139">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="f165f-139">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f165f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f165f-140">CommonParameters</span></span>
<span data-ttu-id="f165f-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f165f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f165f-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f165f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f165f-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f165f-143">INPUTS</span></span>

### <span data-ttu-id="f165f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f165f-144">System.String</span></span>

### <span data-ttu-id="f165f-145">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f165f-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="f165f-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f165f-146">OUTPUTS</span></span>

### <span data-ttu-id="f165f-147">Microsoft. Azure. commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="f165f-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="f165f-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f165f-148">NOTES</span></span>

## <span data-ttu-id="f165f-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f165f-149">RELATED LINKS</span></span>
