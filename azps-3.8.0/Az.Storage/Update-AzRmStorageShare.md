---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 6e3c71900e5fe4a4ac8e4f092691dcde3e759c2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089218"
---
# <span data-ttu-id="223c8-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="223c8-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="223c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="223c8-102">SYNOPSIS</span></span>
<span data-ttu-id="223c8-103">Ändrar en lagrings fil resurs.</span><span class="sxs-lookup"><span data-stu-id="223c8-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="223c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="223c8-104">SYNTAX</span></span>

### <span data-ttu-id="223c8-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="223c8-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="223c8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="223c8-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="223c8-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="223c8-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="223c8-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="223c8-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="223c8-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="223c8-109">DESCRIPTION</span></span>
<span data-ttu-id="223c8-110">Cmdleten **New-AzRmStorageShare** ändrar en lagrings fil resurs.</span><span class="sxs-lookup"><span data-stu-id="223c8-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="223c8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="223c8-111">EXAMPLES</span></span>

### <span data-ttu-id="223c8-112">Exempel 1: ändrar en lagrings fils metadata och delar kvot med lagrings konto namn och resurs namn</span><span class="sxs-lookup"><span data-stu-id="223c8-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup                       200     

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="223c8-113">Det här kommandot ändrar metadata för en lagrings fil resurs och delar kvot med lagrings konto namn och resurs namn och visar sedan ã ndra resultat med det returnerade fildelnings-objektet.</span><span class="sxs-lookup"><span data-stu-id="223c8-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="223c8-114">Exempel 2: ändrar metadata på en lagrings fil resurs med lagrings konto objekt och resurs namn</span><span class="sxs-lookup"><span data-stu-id="223c8-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="223c8-115">Det här kommandot ändrar metadata på en lagrings fil resurs med lagrings konto objekt och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="223c8-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="223c8-116">Exempel 3: ändrar delnings kvoten för alla lagrings fil resurser i ett lagrings konto med pipeline</span><span class="sxs-lookup"><span data-stu-id="223c8-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Update-AzRmStorageShare -QuotaGiB 5000

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup                       5000
share2   myStorageAccount   myResourceGroup                       5000
```

<span data-ttu-id="223c8-117">Det här kommandot ändrar delnings kvoten som 5000 GiB för alla lagrings fil resurser i ett lagrings konto med pipeline.</span><span class="sxs-lookup"><span data-stu-id="223c8-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="223c8-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="223c8-118">PARAMETERS</span></span>

### <span data-ttu-id="223c8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="223c8-119">-DefaultProfile</span></span>
<span data-ttu-id="223c8-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="223c8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="223c8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="223c8-121">-InputObject</span></span>
<span data-ttu-id="223c8-122">Lagrings objekt</span><span class="sxs-lookup"><span data-stu-id="223c8-122">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="223c8-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="223c8-123">-Metadata</span></span>
<span data-ttu-id="223c8-124">Dela metadata</span><span class="sxs-lookup"><span data-stu-id="223c8-124">Share Metadata</span></span>

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

### <span data-ttu-id="223c8-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="223c8-125">-Name</span></span>
<span data-ttu-id="223c8-126">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="223c8-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="223c8-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="223c8-127">-QuotaGiB</span></span>
<span data-ttu-id="223c8-128">Dela kvot i gibibyte.</span><span class="sxs-lookup"><span data-stu-id="223c8-128">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Quota

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="223c8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="223c8-129">-ResourceGroupName</span></span>
<span data-ttu-id="223c8-130">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="223c8-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="223c8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="223c8-131">-ResourceId</span></span>
<span data-ttu-id="223c8-132">Ange ett resurs-ID för fildelning.</span><span class="sxs-lookup"><span data-stu-id="223c8-132">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="223c8-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="223c8-133">-StorageAccount</span></span>
<span data-ttu-id="223c8-134">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="223c8-134">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="223c8-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="223c8-135">-StorageAccountName</span></span>
<span data-ttu-id="223c8-136">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="223c8-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="223c8-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="223c8-137">-Confirm</span></span>
<span data-ttu-id="223c8-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="223c8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="223c8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="223c8-139">-WhatIf</span></span>
<span data-ttu-id="223c8-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="223c8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="223c8-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="223c8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="223c8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="223c8-142">CommonParameters</span></span>
<span data-ttu-id="223c8-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="223c8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="223c8-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="223c8-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="223c8-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="223c8-145">INPUTS</span></span>

### <span data-ttu-id="223c8-146">System. String</span><span class="sxs-lookup"><span data-stu-id="223c8-146">System.String</span></span>

### <span data-ttu-id="223c8-147">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="223c8-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="223c8-148">Microsoft. Azure. commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="223c8-148">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="223c8-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="223c8-149">OUTPUTS</span></span>

### <span data-ttu-id="223c8-150">Microsoft. Azure. commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="223c8-150">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="223c8-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="223c8-151">NOTES</span></span>

## <span data-ttu-id="223c8-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="223c8-152">RELATED LINKS</span></span>
