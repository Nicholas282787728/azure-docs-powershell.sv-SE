---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 81e380f6b6d4b1c35a6cff98093dfedf94119a9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101819"
---
# <span data-ttu-id="8b0a4-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8b0a4-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="8b0a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b0a4-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0a4-103">Skapar en lagrings fil resurs.</span><span class="sxs-lookup"><span data-stu-id="8b0a4-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="8b0a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b0a4-104">SYNTAX</span></span>

### <span data-ttu-id="8b0a4-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="8b0a4-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b0a4-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8b0a4-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b0a4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b0a4-107">DESCRIPTION</span></span>
<span data-ttu-id="8b0a4-108">Cmdleten **New-AzRmStorageShare** skapar en lagrings fil resurs.</span><span class="sxs-lookup"><span data-stu-id="8b0a4-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="8b0a4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b0a4-109">EXAMPLES</span></span>

### <span data-ttu-id="8b0a4-110">Exempel 1: skapa en lagrings fil med lagrings konto namn och dela namn, med metadata och dela kvot som 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="8b0a4-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="8b0a4-111">Det här kommandot skapar en lagrings fil med metadata och delar kvot som 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="8b0a4-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="8b0a4-112">Exempel 2: skapa en lagrings fil med lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="8b0a4-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="8b0a4-113">Det här kommandot skapar en lagrings fil resurs med lagrings konto objekt och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="8b0a4-113">This command creates a Storage file share with Storage account object and share name.</span></span>

## <span data-ttu-id="8b0a4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b0a4-114">PARAMETERS</span></span>

### <span data-ttu-id="8b0a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b0a4-115">-DefaultProfile</span></span>
<span data-ttu-id="8b0a4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b0a4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b0a4-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8b0a4-117">-Metadata</span></span>
<span data-ttu-id="8b0a4-118">Dela metadata</span><span class="sxs-lookup"><span data-stu-id="8b0a4-118">Share Metadata</span></span>

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

### <span data-ttu-id="8b0a4-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b0a4-119">-Name</span></span>
<span data-ttu-id="8b0a4-120">Azure fil resurs namn</span><span class="sxs-lookup"><span data-stu-id="8b0a4-120">Azure File share name</span></span>

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

### <span data-ttu-id="8b0a4-121">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="8b0a4-121">-QuotaGiB</span></span>
<span data-ttu-id="8b0a4-122">Dela kvot i gibibyte.</span><span class="sxs-lookup"><span data-stu-id="8b0a4-122">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="8b0a4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b0a4-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b0a4-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="8b0a4-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="8b0a4-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b0a4-125">-StorageAccount</span></span>
<span data-ttu-id="8b0a4-126">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="8b0a4-126">Storage account object</span></span>

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

### <span data-ttu-id="8b0a4-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8b0a4-127">-StorageAccountName</span></span>
<span data-ttu-id="8b0a4-128">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="8b0a4-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="8b0a4-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8b0a4-129">-Confirm</span></span>
<span data-ttu-id="8b0a4-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8b0a4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b0a4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b0a4-131">-WhatIf</span></span>
<span data-ttu-id="8b0a4-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8b0a4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b0a4-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8b0a4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b0a4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0a4-134">CommonParameters</span></span>
<span data-ttu-id="8b0a4-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b0a4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0a4-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b0a4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0a4-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b0a4-137">INPUTS</span></span>

### <span data-ttu-id="8b0a4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8b0a4-138">System.String</span></span>

### <span data-ttu-id="8b0a4-139">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b0a4-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="8b0a4-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b0a4-140">OUTPUTS</span></span>

### <span data-ttu-id="8b0a4-141">Microsoft. Azure. commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="8b0a4-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="8b0a4-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b0a4-142">NOTES</span></span>

## <span data-ttu-id="8b0a4-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b0a4-143">RELATED LINKS</span></span>
