---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100737"
---
# <span data-ttu-id="772f7-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="772f7-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="772f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="772f7-102">SYNOPSIS</span></span>
<span data-ttu-id="772f7-103">Återställer en borttagen fil resurs.</span><span class="sxs-lookup"><span data-stu-id="772f7-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="772f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="772f7-104">SYNTAX</span></span>

### <span data-ttu-id="772f7-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="772f7-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="772f7-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="772f7-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="772f7-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="772f7-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="772f7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="772f7-108">DESCRIPTION</span></span>
<span data-ttu-id="772f7-109">Cmdleten **restore-AzRmStorageShare** återställer en borttagen fil resurs inom en giltig lagrings dag om dela mjuk borttagning är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="772f7-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="772f7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="772f7-110">EXAMPLES</span></span>

### <span data-ttu-id="772f7-111">Exempel 1: ta bort och återställa en resurs</span><span class="sxs-lookup"><span data-stu-id="772f7-111">Example 1: Remove and restore a share</span></span>
```powershell
PS C:\> Remove-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -Force

PS C:\> Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6                

PS C:\> Restore-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -DeletedShareVersion 01D61FD1FC5498B6

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   100
```

<span data-ttu-id="772f7-112">Det här kommandot tar först bort en fil resurs och sedan list-och avmarkerar du den borttagna delnings versionen och återställer den till en normal delning.</span><span class="sxs-lookup"><span data-stu-id="772f7-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="772f7-113">Behöver aktive rad dela mjuk borttagning med Update-AzStorageFileServiceProperty, innan du tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="772f7-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="772f7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="772f7-114">PARAMETERS</span></span>

### <span data-ttu-id="772f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="772f7-115">-DefaultProfile</span></span>
<span data-ttu-id="772f7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="772f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="772f7-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="772f7-117">-DeletedShareVersion</span></span>
<span data-ttu-id="772f7-118">Borttagen delnings version, som kommer att återställas från.</span><span class="sxs-lookup"><span data-stu-id="772f7-118">Deleted Share Version, which will be restored from.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="772f7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="772f7-119">-InputObject</span></span>
<span data-ttu-id="772f7-120">Borttaget dela-objekt</span><span class="sxs-lookup"><span data-stu-id="772f7-120">Deleted Share object</span></span>

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

### <span data-ttu-id="772f7-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="772f7-121">-Name</span></span>
<span data-ttu-id="772f7-122">Borttaget resurs namn som återställs.</span><span class="sxs-lookup"><span data-stu-id="772f7-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="772f7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="772f7-123">-ResourceGroupName</span></span>
<span data-ttu-id="772f7-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="772f7-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="772f7-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="772f7-125">-StorageAccount</span></span>
<span data-ttu-id="772f7-126">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="772f7-126">Storage account object</span></span>

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

### <span data-ttu-id="772f7-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="772f7-127">-StorageAccountName</span></span>
<span data-ttu-id="772f7-128">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="772f7-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="772f7-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="772f7-129">-Confirm</span></span>
<span data-ttu-id="772f7-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="772f7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="772f7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="772f7-131">-WhatIf</span></span>
<span data-ttu-id="772f7-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="772f7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="772f7-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="772f7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="772f7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="772f7-134">CommonParameters</span></span>
<span data-ttu-id="772f7-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="772f7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="772f7-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="772f7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="772f7-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="772f7-137">INPUTS</span></span>

### <span data-ttu-id="772f7-138">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="772f7-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="772f7-139">Microsoft. Azure. commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="772f7-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="772f7-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="772f7-140">OUTPUTS</span></span>

### <span data-ttu-id="772f7-141">Microsoft. Azure. commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="772f7-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="772f7-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="772f7-142">NOTES</span></span>

## <span data-ttu-id="772f7-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="772f7-143">RELATED LINKS</span></span>