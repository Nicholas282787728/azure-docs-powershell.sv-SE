---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322276"
---
# <span data-ttu-id="73a13-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="73a13-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="73a13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73a13-102">SYNOPSIS</span></span>
<span data-ttu-id="73a13-103">Inaktivera borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="73a13-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="73a13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73a13-104">SYNTAX</span></span>

### <span data-ttu-id="73a13-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="73a13-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73a13-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="73a13-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73a13-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="73a13-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73a13-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73a13-108">DESCRIPTION</span></span>
<span data-ttu-id="73a13-109">Cmdleten **disable-AzStorageBlobDeleteRetentionPolicy** inaktiverar borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="73a13-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="73a13-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73a13-110">EXAMPLES</span></span>

### <span data-ttu-id="73a13-111">Exempel 1: inaktivera borttagnings principer för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="73a13-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="73a13-112">Det här kommandot inaktiverar borttagning av princip för bevarande av Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="73a13-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="73a13-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73a13-113">PARAMETERS</span></span>

### <span data-ttu-id="73a13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73a13-114">-DefaultProfile</span></span>
<span data-ttu-id="73a13-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73a13-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73a13-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73a13-116">-PassThru</span></span>
<span data-ttu-id="73a13-117">Visa ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="73a13-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="73a13-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73a13-118">-ResourceGroupName</span></span>
<span data-ttu-id="73a13-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="73a13-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="73a13-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73a13-120">-ResourceId</span></span>
<span data-ttu-id="73a13-121">Ange ett resurs-ID för lagrings-ID eller egenskaper för Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="73a13-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="73a13-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="73a13-122">-StorageAccount</span></span>
<span data-ttu-id="73a13-123">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="73a13-123">Storage account object</span></span>

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

### <span data-ttu-id="73a13-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="73a13-124">-StorageAccountName</span></span>
<span data-ttu-id="73a13-125">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="73a13-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="73a13-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="73a13-126">-Confirm</span></span>
<span data-ttu-id="73a13-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73a13-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73a13-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73a13-128">-WhatIf</span></span>
<span data-ttu-id="73a13-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="73a13-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73a13-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="73a13-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73a13-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a13-131">CommonParameters</span></span>
<span data-ttu-id="73a13-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a13-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a13-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73a13-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a13-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73a13-134">INPUTS</span></span>

### <span data-ttu-id="73a13-135">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73a13-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="73a13-136">System. String</span><span class="sxs-lookup"><span data-stu-id="73a13-136">System.String</span></span>

## <span data-ttu-id="73a13-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73a13-137">OUTPUTS</span></span>

### <span data-ttu-id="73a13-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="73a13-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="73a13-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73a13-139">NOTES</span></span>

## <span data-ttu-id="73a13-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73a13-140">RELATED LINKS</span></span>
