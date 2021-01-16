---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 4dc3914e4a8bc9113dd16ab431db53ddcf00ab5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404128"
---
# <span data-ttu-id="b0ba4-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b0ba4-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="b0ba4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="b0ba4-103">Skapar en lagrings fil resurs.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="b0ba4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0ba4-104">SYNTAX</span></span>

### <span data-ttu-id="b0ba4-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="b0ba4-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0ba4-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b0ba4-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0ba4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0ba4-107">DESCRIPTION</span></span>
<span data-ttu-id="b0ba4-108">Cmdleten **New-AzRmStorageShare** skapar en lagrings fil resurs.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="b0ba4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0ba4-109">EXAMPLES</span></span>

### <span data-ttu-id="b0ba4-110">Exempel 1: skapa en lagrings fil med lagrings konto namn och dela namn, med metadata och dela kvot som 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="b0ba4-111">Det här kommandot skapar en lagrings fil med metadata och delar kvot som 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="b0ba4-112">Exempel 2: skapa en lagrings fil med lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="b0ba4-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="b0ba4-113">Det här kommandot skapar en lagrings fil resurs med lagrings konto objekt och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="b0ba4-114">Exempel 3: skapa en lagrings fil med accesstier som het</span><span class="sxs-lookup"><span data-stu-id="b0ba4-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="b0ba4-115">Det här kommandot skapar en lagrings fil med accesstier som het.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="b0ba4-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0ba4-116">PARAMETERS</span></span>

### <span data-ttu-id="b0ba4-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="b0ba4-117">-AccessTier</span></span>
<span data-ttu-id="b0ba4-118">Åtkomst nivå för specifik resurs.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-118">Access tier for specific share.</span></span> <span data-ttu-id="b0ba4-119">StorageV2-konto kan välja mellan TransactionOptimized (standard), varmt och coolt.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="b0ba4-120">FileStorage-konto kan välja Premium.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="b0ba4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0ba4-121">-DefaultProfile</span></span>
<span data-ttu-id="b0ba4-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0ba4-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b0ba4-123">-Metadata</span></span>
<span data-ttu-id="b0ba4-124">Dela metadata</span><span class="sxs-lookup"><span data-stu-id="b0ba4-124">Share Metadata</span></span>

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

### <span data-ttu-id="b0ba4-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0ba4-125">-Name</span></span>
<span data-ttu-id="b0ba4-126">Azure fil resurs namn</span><span class="sxs-lookup"><span data-stu-id="b0ba4-126">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ba4-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="b0ba4-127">-QuotaGiB</span></span>
<span data-ttu-id="b0ba4-128">Dela kvot i gibibyte.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="b0ba4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0ba4-129">-ResourceGroupName</span></span>
<span data-ttu-id="b0ba4-130">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="b0ba4-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b0ba4-131">-StorageAccount</span></span>
<span data-ttu-id="b0ba4-132">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="b0ba4-132">Storage account object</span></span>

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

### <span data-ttu-id="b0ba4-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b0ba4-133">-StorageAccountName</span></span>
<span data-ttu-id="b0ba4-134">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="b0ba4-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b0ba4-135">-Confirm</span></span>
<span data-ttu-id="b0ba4-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0ba4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0ba4-137">-WhatIf</span></span>
<span data-ttu-id="b0ba4-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0ba4-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0ba4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0ba4-140">CommonParameters</span></span>
<span data-ttu-id="b0ba4-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0ba4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0ba4-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0ba4-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0ba4-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0ba4-143">INPUTS</span></span>

### <span data-ttu-id="b0ba4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b0ba4-144">System.String</span></span>

### <span data-ttu-id="b0ba4-145">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b0ba4-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="b0ba4-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0ba4-146">OUTPUTS</span></span>

### <span data-ttu-id="b0ba4-147">Microsoft. Azure. commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="b0ba4-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="b0ba4-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0ba4-148">NOTES</span></span>

## <span data-ttu-id="b0ba4-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0ba4-149">RELATED LINKS</span></span>
