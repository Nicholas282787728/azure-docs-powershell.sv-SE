---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: a5b5b1c761bb6e3c23a5dd5f0525d2d6627b3ab2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273005"
---
# <span data-ttu-id="d2e26-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="d2e26-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="d2e26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2e26-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e26-103">Aktiverar BLOB-återställning för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="d2e26-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="d2e26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2e26-104">SYNTAX</span></span>

### <span data-ttu-id="d2e26-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="d2e26-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2e26-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d2e26-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2e26-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="d2e26-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2e26-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2e26-108">DESCRIPTION</span></span>
<span data-ttu-id="d2e26-109">Cmdleten **Enable-AzStorageBlobRestorePolicy** aktiverar BLOB Restore policy för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d2e26-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="d2e26-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2e26-110">EXAMPLES</span></span>

### <span data-ttu-id="d2e26-111">Exempel 1: aktiverar BLOB Restore policy för Azure Storage Blob-tjänsten på ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="d2e26-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" $accountName -RetentionDays 5

PS C:\> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : False
RestorePolicy.Days            : 
RestorePolicy.MinRestoreTime  : 
ChangeFeed                    : True
IsVersioningEnabled           : True

PS C:\> Enable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -RestoreDays 4

PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : True
RestorePolicy.Days            : 4
RestorePolicy.MinRestoreTime  : 8/28/2020 6:00:59 AM
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="d2e26-112">Detta kommando aktiverar först BLOB softdelete och changefeed, sedan aktiverar BLOB Restore policy och slutligen kontrollerar inställningen i egenskaper för Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d2e26-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="d2e26-113">RestorePolicy för Blob-tjänsten måste vara mindre än DeleteRetentionPolicy. dagar.</span><span class="sxs-lookup"><span data-stu-id="d2e26-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="d2e26-114">BLOB softdelete och ChangeFeed måste aktive ras före aktivering av BLOB Restore policy.</span><span class="sxs-lookup"><span data-stu-id="d2e26-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="d2e26-115">Om softdelete och Changefeed just är aktiverade kan det vara nödvändigt att vänta en stund för att servern ska hantera inställningen innan den aktive ras.</span><span class="sxs-lookup"><span data-stu-id="d2e26-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="d2e26-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2e26-116">PARAMETERS</span></span>

### <span data-ttu-id="d2e26-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e26-117">-DefaultProfile</span></span>
<span data-ttu-id="d2e26-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e26-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2e26-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2e26-119">-PassThru</span></span>
<span data-ttu-id="d2e26-120">Visa ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="d2e26-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="d2e26-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e26-121">-ResourceGroupName</span></span>
<span data-ttu-id="d2e26-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d2e26-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="d2e26-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2e26-123">-ResourceId</span></span>
<span data-ttu-id="d2e26-124">Ange ett resurs-ID för lagrings-ID eller egenskaper för Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d2e26-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e26-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="d2e26-125">-RestoreDays</span></span>
<span data-ttu-id="d2e26-126">Anger antalet dagar som blobben kan återställas.</span><span class="sxs-lookup"><span data-stu-id="d2e26-126">Sets the number of days for the blob can be restored..</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e26-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2e26-127">-StorageAccount</span></span>
<span data-ttu-id="d2e26-128">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="d2e26-128">Storage account object</span></span>

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

### <span data-ttu-id="d2e26-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d2e26-129">-StorageAccountName</span></span>
<span data-ttu-id="d2e26-130">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="d2e26-130">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e26-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d2e26-131">-Confirm</span></span>
<span data-ttu-id="d2e26-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d2e26-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2e26-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2e26-133">-WhatIf</span></span>
<span data-ttu-id="d2e26-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d2e26-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2e26-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d2e26-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2e26-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e26-136">CommonParameters</span></span>
<span data-ttu-id="d2e26-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2e26-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e26-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e26-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e26-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2e26-139">INPUTS</span></span>

### <span data-ttu-id="d2e26-140">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2e26-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d2e26-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d2e26-141">System.String</span></span>

## <span data-ttu-id="d2e26-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2e26-142">OUTPUTS</span></span>

### <span data-ttu-id="d2e26-143">Microsoft. Azure. commands. Management. Storage. Models. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="d2e26-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="d2e26-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2e26-144">NOTES</span></span>

## <span data-ttu-id="d2e26-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2e26-145">RELATED LINKS</span></span>
