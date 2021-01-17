---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 0f2d86fca85364fa71d50c05d83f278bd997252e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394555"
---
# <span data-ttu-id="301f7-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="301f7-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="301f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="301f7-102">SYNOPSIS</span></span>
<span data-ttu-id="301f7-103">Ändrar en lagrings fil resurs.</span><span class="sxs-lookup"><span data-stu-id="301f7-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="301f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="301f7-104">SYNTAX</span></span>

### <span data-ttu-id="301f7-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="301f7-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="301f7-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="301f7-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="301f7-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="301f7-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="301f7-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="301f7-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="301f7-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="301f7-109">DESCRIPTION</span></span>
<span data-ttu-id="301f7-110">Cmdleten **New-AzRmStorageShare** ändrar en lagrings fil resurs.</span><span class="sxs-lookup"><span data-stu-id="301f7-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="301f7-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="301f7-111">EXAMPLES</span></span>

### <span data-ttu-id="301f7-112">Exempel 1: ändrar en lagrings fils metadata och delar kvot med lagrings konto namn och resurs namn</span><span class="sxs-lookup"><span data-stu-id="301f7-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  200

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="301f7-113">Det här kommandot ändrar metadata för en lagrings fil resurs och delar kvot med lagrings konto namn och resurs namn och visar sedan ã ndra resultat med det returnerade fildelnings-objektet.</span><span class="sxs-lookup"><span data-stu-id="301f7-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="301f7-114">Exempel 2: ändrar metadata på en lagrings fil resurs med lagrings konto objekt och resurs namn</span><span class="sxs-lookup"><span data-stu-id="301f7-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="301f7-115">Det här kommandot ändrar metadata på en lagrings fil resurs med lagrings konto objekt och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="301f7-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="301f7-116">Exempel 3: ändrar delnings kvoten för alla lagrings fil resurser i ett lagrings konto med pipeline</span><span class="sxs-lookup"><span data-stu-id="301f7-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="301f7-117">Det här kommandot ändrar delnings kvoten som 5000 GiB för alla lagrings fil resurser i ett lagrings konto med pipeline.</span><span class="sxs-lookup"><span data-stu-id="301f7-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="301f7-118">Exempel 4: ändra en lagrings fil med accesstier som coolt</span><span class="sxs-lookup"><span data-stu-id="301f7-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="301f7-119">Det här kommandot ändrar en lagrings fil med accesstier som coolt.</span><span class="sxs-lookup"><span data-stu-id="301f7-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="301f7-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="301f7-120">PARAMETERS</span></span>

### <span data-ttu-id="301f7-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="301f7-121">-AccessTier</span></span>
<span data-ttu-id="301f7-122">Åtkomst nivå för specifik resurs.</span><span class="sxs-lookup"><span data-stu-id="301f7-122">Access tier for specific share.</span></span> <span data-ttu-id="301f7-123">StorageV2-konto kan välja mellan TransactionOptimized (standard), varmt och coolt.</span><span class="sxs-lookup"><span data-stu-id="301f7-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="301f7-124">FileStorage-konto kan välja Premium.</span><span class="sxs-lookup"><span data-stu-id="301f7-124">FileStorage account can choose Premium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TransactionOptimized, Premium, Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301f7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301f7-125">-DefaultProfile</span></span>
<span data-ttu-id="301f7-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="301f7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="301f7-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="301f7-127">-InputObject</span></span>
<span data-ttu-id="301f7-128">Lagrings objekt</span><span class="sxs-lookup"><span data-stu-id="301f7-128">Storage Share object</span></span>

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

### <span data-ttu-id="301f7-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="301f7-129">-Metadata</span></span>
<span data-ttu-id="301f7-130">Dela metadata</span><span class="sxs-lookup"><span data-stu-id="301f7-130">Share Metadata</span></span>

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

### <span data-ttu-id="301f7-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="301f7-131">-Name</span></span>
<span data-ttu-id="301f7-132">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="301f7-132">Share Name</span></span>

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

### <span data-ttu-id="301f7-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="301f7-133">-QuotaGiB</span></span>
<span data-ttu-id="301f7-134">Dela kvot i gibibyte.</span><span class="sxs-lookup"><span data-stu-id="301f7-134">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="301f7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301f7-135">-ResourceGroupName</span></span>
<span data-ttu-id="301f7-136">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="301f7-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="301f7-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="301f7-137">-ResourceId</span></span>
<span data-ttu-id="301f7-138">Ange ett resurs-ID för fildelning.</span><span class="sxs-lookup"><span data-stu-id="301f7-138">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="301f7-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="301f7-139">-StorageAccount</span></span>
<span data-ttu-id="301f7-140">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="301f7-140">Storage account object</span></span>

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

### <span data-ttu-id="301f7-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="301f7-141">-StorageAccountName</span></span>
<span data-ttu-id="301f7-142">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="301f7-142">Storage Account Name.</span></span>

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

### <span data-ttu-id="301f7-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="301f7-143">-Confirm</span></span>
<span data-ttu-id="301f7-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="301f7-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="301f7-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="301f7-145">-WhatIf</span></span>
<span data-ttu-id="301f7-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="301f7-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="301f7-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="301f7-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="301f7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301f7-148">CommonParameters</span></span>
<span data-ttu-id="301f7-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="301f7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301f7-150">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="301f7-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301f7-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="301f7-151">INPUTS</span></span>

### <span data-ttu-id="301f7-152">System. String</span><span class="sxs-lookup"><span data-stu-id="301f7-152">System.String</span></span>

### <span data-ttu-id="301f7-153">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="301f7-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="301f7-154">Microsoft. Azure. commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="301f7-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="301f7-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="301f7-155">OUTPUTS</span></span>

### <span data-ttu-id="301f7-156">Microsoft. Azure. commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="301f7-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="301f7-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="301f7-157">NOTES</span></span>

## <span data-ttu-id="301f7-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="301f7-158">RELATED LINKS</span></span>
