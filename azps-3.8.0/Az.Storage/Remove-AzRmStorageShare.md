---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: bff7a79513cc8eb0047860f9edd00c6c37c5f1b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090187"
---
# <span data-ttu-id="8b68b-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8b68b-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="8b68b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b68b-102">SYNOPSIS</span></span>
<span data-ttu-id="8b68b-103">Tar bort en lagrings fil resurs.</span><span class="sxs-lookup"><span data-stu-id="8b68b-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="8b68b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b68b-104">SYNTAX</span></span>

### <span data-ttu-id="8b68b-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="8b68b-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b68b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8b68b-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b68b-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="8b68b-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b68b-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="8b68b-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b68b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b68b-109">DESCRIPTION</span></span>
<span data-ttu-id="8b68b-110">**New-AzRmStorageShare** cmdlet tar bort en lagrings fil resurs.</span><span class="sxs-lookup"><span data-stu-id="8b68b-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="8b68b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b68b-111">EXAMPLES</span></span>

### <span data-ttu-id="8b68b-112">Exempel 1: ta bort en lagrings fil med lagrings konto namn och resurs namn</span><span class="sxs-lookup"><span data-stu-id="8b68b-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="8b68b-113">Det här kommandot tar bort en lagrings fil resurs med namn på lagrings konto och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="8b68b-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="8b68b-114">Exempel 2: ta bort en lagrings fil med lagrings konto objekt och resurs namn</span><span class="sxs-lookup"><span data-stu-id="8b68b-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="8b68b-115">Det här kommandot tar bort en lagrings fil med lagrings konto objekt och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="8b68b-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="8b68b-116">Exempel 3: ta bort alla lagrings fil resurser i ett lagrings konto med pipeline</span><span class="sxs-lookup"><span data-stu-id="8b68b-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="8b68b-117">Detta kommando tar bort alla lagrings fil resurser i ett lagrings konto med pipelinan.</span><span class="sxs-lookup"><span data-stu-id="8b68b-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="8b68b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b68b-118">PARAMETERS</span></span>

### <span data-ttu-id="8b68b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b68b-119">-DefaultProfile</span></span>
<span data-ttu-id="8b68b-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b68b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b68b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8b68b-121">-Force</span></span>
<span data-ttu-id="8b68b-122">Tvinga att ta bort delningen och allt innehåll i den</span><span class="sxs-lookup"><span data-stu-id="8b68b-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="8b68b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b68b-123">-InputObject</span></span>
<span data-ttu-id="8b68b-124">Lagrings objekt</span><span class="sxs-lookup"><span data-stu-id="8b68b-124">Storage Share object</span></span>

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

### <span data-ttu-id="8b68b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b68b-125">-Name</span></span>
<span data-ttu-id="8b68b-126">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="8b68b-126">Share Name</span></span>

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

### <span data-ttu-id="8b68b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b68b-127">-PassThru</span></span>
<span data-ttu-id="8b68b-128">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="8b68b-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="8b68b-129">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="8b68b-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8b68b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b68b-130">-ResourceGroupName</span></span>
<span data-ttu-id="8b68b-131">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="8b68b-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="8b68b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b68b-132">-ResourceId</span></span>
<span data-ttu-id="8b68b-133">Ange ett resurs-ID för fildelning.</span><span class="sxs-lookup"><span data-stu-id="8b68b-133">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="8b68b-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b68b-134">-StorageAccount</span></span>
<span data-ttu-id="8b68b-135">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="8b68b-135">Storage account object</span></span>

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

### <span data-ttu-id="8b68b-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8b68b-136">-StorageAccountName</span></span>
<span data-ttu-id="8b68b-137">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="8b68b-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="8b68b-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8b68b-138">-Confirm</span></span>
<span data-ttu-id="8b68b-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8b68b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b68b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b68b-140">-WhatIf</span></span>
<span data-ttu-id="8b68b-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8b68b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b68b-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8b68b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b68b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b68b-143">CommonParameters</span></span>
<span data-ttu-id="8b68b-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b68b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b68b-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b68b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b68b-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b68b-146">INPUTS</span></span>

### <span data-ttu-id="8b68b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="8b68b-147">System.String</span></span>

### <span data-ttu-id="8b68b-148">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b68b-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8b68b-149">Microsoft. Azure. commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="8b68b-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="8b68b-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b68b-150">OUTPUTS</span></span>

### <span data-ttu-id="8b68b-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b68b-151">System.Boolean</span></span>

## <span data-ttu-id="8b68b-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b68b-152">NOTES</span></span>

## <span data-ttu-id="8b68b-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b68b-153">RELATED LINKS</span></span>
