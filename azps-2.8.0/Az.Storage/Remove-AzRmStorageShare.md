---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: 3c4071d11e521476f02cadb7323267f84183510b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920944"
---
# <span data-ttu-id="84023-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="84023-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="84023-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84023-102">SYNOPSIS</span></span>
<span data-ttu-id="84023-103">Tar bort en lagrings fil resurs.</span><span class="sxs-lookup"><span data-stu-id="84023-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="84023-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84023-104">SYNTAX</span></span>

### <span data-ttu-id="84023-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="84023-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84023-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="84023-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84023-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="84023-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84023-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="84023-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84023-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84023-109">DESCRIPTION</span></span>
<span data-ttu-id="84023-110">**New-AzRmStorageShare** cmdlet tar bort en lagrings fil resurs.</span><span class="sxs-lookup"><span data-stu-id="84023-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="84023-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84023-111">EXAMPLES</span></span>

### <span data-ttu-id="84023-112">Exempel 1: ta bort en lagrings fil med lagrings konto namn och resurs namn</span><span class="sxs-lookup"><span data-stu-id="84023-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="84023-113">Det här kommandot tar bort en lagrings fil resurs med namn på lagrings konto och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="84023-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="84023-114">Exempel 2: ta bort en lagrings fil med lagrings konto objekt och resurs namn</span><span class="sxs-lookup"><span data-stu-id="84023-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="84023-115">Det här kommandot tar bort en lagrings fil med lagrings konto objekt och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="84023-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="84023-116">Exempel 3: ta bort alla lagrings fil resurser i ett lagrings konto med pipeline</span><span class="sxs-lookup"><span data-stu-id="84023-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="84023-117">Detta kommando tar bort alla lagrings fil resurser i ett lagrings konto med pipelinan.</span><span class="sxs-lookup"><span data-stu-id="84023-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="84023-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84023-118">PARAMETERS</span></span>

### <span data-ttu-id="84023-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84023-119">-DefaultProfile</span></span>
<span data-ttu-id="84023-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="84023-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84023-121">-Force</span><span class="sxs-lookup"><span data-stu-id="84023-121">-Force</span></span>
<span data-ttu-id="84023-122">Tvinga att ta bort delningen och allt innehåll i den</span><span class="sxs-lookup"><span data-stu-id="84023-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="84023-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84023-123">-InputObject</span></span>
<span data-ttu-id="84023-124">Lagrings objekt</span><span class="sxs-lookup"><span data-stu-id="84023-124">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84023-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="84023-125">-Name</span></span>
<span data-ttu-id="84023-126">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="84023-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84023-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84023-127">-PassThru</span></span>
<span data-ttu-id="84023-128">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="84023-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="84023-129">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="84023-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="84023-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84023-130">-ResourceGroupName</span></span>
<span data-ttu-id="84023-131">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="84023-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="84023-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84023-132">-ResourceId</span></span>
<span data-ttu-id="84023-133">Ange ett resurs-ID för fildelning.</span><span class="sxs-lookup"><span data-stu-id="84023-133">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="84023-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="84023-134">-StorageAccount</span></span>
<span data-ttu-id="84023-135">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="84023-135">Storage account object</span></span>

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

### <span data-ttu-id="84023-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="84023-136">-StorageAccountName</span></span>
<span data-ttu-id="84023-137">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="84023-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="84023-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="84023-138">-Confirm</span></span>
<span data-ttu-id="84023-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="84023-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84023-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84023-140">-WhatIf</span></span>
<span data-ttu-id="84023-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="84023-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84023-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="84023-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84023-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84023-143">CommonParameters</span></span>
<span data-ttu-id="84023-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84023-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84023-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84023-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84023-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84023-146">INPUTS</span></span>

### <span data-ttu-id="84023-147">System. String</span><span class="sxs-lookup"><span data-stu-id="84023-147">System.String</span></span>

### <span data-ttu-id="84023-148">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="84023-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="84023-149">Microsoft. Azure. commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="84023-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="84023-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84023-150">OUTPUTS</span></span>

### <span data-ttu-id="84023-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84023-151">System.Boolean</span></span>

## <span data-ttu-id="84023-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84023-152">NOTES</span></span>

## <span data-ttu-id="84023-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84023-153">RELATED LINKS</span></span>
