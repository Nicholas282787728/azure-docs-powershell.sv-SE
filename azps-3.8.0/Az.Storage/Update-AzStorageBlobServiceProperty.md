---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: b7d6299af3f56dd8f09c73171ab6630cbbb9bc96
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090250"
---
# <span data-ttu-id="c2651-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c2651-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="c2651-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2651-102">SYNOPSIS</span></span>
<span data-ttu-id="c2651-103">Ändrar tjänste egenskaperna för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c2651-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c2651-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2651-104">SYNTAX</span></span>

### <span data-ttu-id="c2651-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="c2651-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2651-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c2651-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2651-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="c2651-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2651-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2651-108">DESCRIPTION</span></span>
<span data-ttu-id="c2651-109">Cmdleten **Update-AzStorageBlobServiceProperty** ändrar tjänst egenskaperna för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c2651-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c2651-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2651-110">EXAMPLES</span></span>

### <span data-ttu-id="c2651-111">Exempel 1: Ange BLOB service-DefaultServiceVersion till 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="c2651-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False                                                   
```

<span data-ttu-id="c2651-112">Det här kommandot anger DefaultServiceVersion för Blob-tjänsten till 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="c2651-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

## <span data-ttu-id="c2651-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2651-113">PARAMETERS</span></span>

### <span data-ttu-id="c2651-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2651-114">-DefaultProfile</span></span>
<span data-ttu-id="c2651-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2651-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2651-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="c2651-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="c2651-117">Standard tjänst version att ange</span><span class="sxs-lookup"><span data-stu-id="c2651-117">Default Service Version to Set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2651-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2651-118">-ResourceGroupName</span></span>
<span data-ttu-id="c2651-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c2651-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="c2651-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2651-120">-ResourceId</span></span>
<span data-ttu-id="c2651-121">Ange ett resurs-ID för lagrings-ID eller egenskaper för Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c2651-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="c2651-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2651-122">-StorageAccount</span></span>
<span data-ttu-id="c2651-123">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="c2651-123">Storage account object</span></span>

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

### <span data-ttu-id="c2651-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c2651-124">-StorageAccountName</span></span>
<span data-ttu-id="c2651-125">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="c2651-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="c2651-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2651-126">-Confirm</span></span>
<span data-ttu-id="c2651-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2651-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2651-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2651-128">-WhatIf</span></span>
<span data-ttu-id="c2651-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2651-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2651-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2651-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2651-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2651-131">CommonParameters</span></span>
<span data-ttu-id="c2651-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2651-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2651-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2651-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2651-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2651-134">INPUTS</span></span>

### <span data-ttu-id="c2651-135">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2651-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c2651-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c2651-136">System.String</span></span>

## <span data-ttu-id="c2651-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2651-137">OUTPUTS</span></span>

### <span data-ttu-id="c2651-138">Microsoft. Azure. commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="c2651-138">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="c2651-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2651-139">NOTES</span></span>

## <span data-ttu-id="c2651-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2651-140">RELATED LINKS</span></span>
