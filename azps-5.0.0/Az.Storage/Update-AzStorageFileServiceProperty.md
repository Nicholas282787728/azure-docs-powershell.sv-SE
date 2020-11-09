---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324977"
---
# <span data-ttu-id="70754-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="70754-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="70754-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70754-102">SYNOPSIS</span></span>
<span data-ttu-id="70754-103">Ändrar tjänste egenskaperna för Azure Storage File-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="70754-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="70754-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70754-104">SYNTAX</span></span>

### <span data-ttu-id="70754-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="70754-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70754-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="70754-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70754-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="70754-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70754-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70754-108">DESCRIPTION</span></span>
<span data-ttu-id="70754-109">Cmdleten **Update-AzStorageFileServiceProperty** ändrar tjänst egenskaperna för Azure Storage File-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="70754-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="70754-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70754-110">EXAMPLES</span></span>

### <span data-ttu-id="70754-111">Exempel 1: aktivera fil resursen softdelete</span><span class="sxs-lookup"><span data-stu-id="70754-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="70754-112">Med det här kommandot kan fil resursen softdelete ta bort med bevarande dagar som 5</span><span class="sxs-lookup"><span data-stu-id="70754-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="70754-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70754-113">PARAMETERS</span></span>

### <span data-ttu-id="70754-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70754-114">-DefaultProfile</span></span>
<span data-ttu-id="70754-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70754-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70754-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="70754-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="70754-117">Aktivera dela borttagnings princip för lagrings kontot genom att ange $true och inaktivera dela ta bort bevarande princip genom att ange $false.</span><span class="sxs-lookup"><span data-stu-id="70754-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70754-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70754-118">-ResourceGroupName</span></span>
<span data-ttu-id="70754-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="70754-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="70754-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70754-120">-ResourceId</span></span>
<span data-ttu-id="70754-121">Ange ett resurs-ID för ett lagrings konto eller ett resurs namn för fil tjänst egenskaper.</span><span class="sxs-lookup"><span data-stu-id="70754-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70754-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="70754-122">-ShareRetentionDays</span></span>
<span data-ttu-id="70754-123">Anger antalet bevarande dagar för Share DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="70754-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="70754-124">Värdet bör bara anges när du aktiverar ta bort lagrings princip för delning.</span><span class="sxs-lookup"><span data-stu-id="70754-124">The value should only be set when enable share Delete Retention Policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days, RetentionDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70754-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="70754-125">-StorageAccount</span></span>
<span data-ttu-id="70754-126">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="70754-126">Storage account object</span></span>

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

### <span data-ttu-id="70754-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="70754-127">-StorageAccountName</span></span>
<span data-ttu-id="70754-128">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="70754-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="70754-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="70754-129">-Confirm</span></span>
<span data-ttu-id="70754-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="70754-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70754-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70754-131">-WhatIf</span></span>
<span data-ttu-id="70754-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="70754-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70754-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="70754-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70754-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70754-134">CommonParameters</span></span>
<span data-ttu-id="70754-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70754-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70754-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70754-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70754-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70754-137">INPUTS</span></span>

### <span data-ttu-id="70754-138">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="70754-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="70754-139">System. String</span><span class="sxs-lookup"><span data-stu-id="70754-139">System.String</span></span>

## <span data-ttu-id="70754-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70754-140">OUTPUTS</span></span>

### <span data-ttu-id="70754-141">Microsoft. Azure. commands. Management. Storage. Models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="70754-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="70754-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70754-142">NOTES</span></span>

## <span data-ttu-id="70754-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70754-143">RELATED LINKS</span></span>
