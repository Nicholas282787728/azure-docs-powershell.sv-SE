---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404352"
---
# <span data-ttu-id="942a5-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="942a5-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="942a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="942a5-102">SYNOPSIS</span></span>
<span data-ttu-id="942a5-103">Inaktiverar BLOB Restore policy för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="942a5-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="942a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="942a5-104">SYNTAX</span></span>

### <span data-ttu-id="942a5-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="942a5-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="942a5-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="942a5-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="942a5-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="942a5-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="942a5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="942a5-108">DESCRIPTION</span></span>
<span data-ttu-id="942a5-109">Cmdleten **disable-AzStorageBlobRestorePolicy** inaktiverar BLOB Restore policy för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="942a5-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="942a5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="942a5-110">EXAMPLES</span></span>

### <span data-ttu-id="942a5-111">Exempel 1: inaktiverar BLOB Restore policy för Azure Storage Blob-tjänsten på ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="942a5-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="942a5-112">Det här kommandot inaktiverar BLOB Restore policy för Azure Storage Blob-tjänsten på ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="942a5-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="942a5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="942a5-113">PARAMETERS</span></span>

### <span data-ttu-id="942a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="942a5-114">-DefaultProfile</span></span>
<span data-ttu-id="942a5-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="942a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="942a5-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="942a5-116">-PassThru</span></span>
<span data-ttu-id="942a5-117">Visa ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="942a5-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="942a5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="942a5-118">-ResourceGroupName</span></span>
<span data-ttu-id="942a5-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="942a5-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="942a5-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="942a5-120">-ResourceId</span></span>
<span data-ttu-id="942a5-121">Ange ett resurs-ID för lagrings-ID eller egenskaper för Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="942a5-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="942a5-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="942a5-122">-StorageAccount</span></span>
<span data-ttu-id="942a5-123">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="942a5-123">Storage account object</span></span>

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

### <span data-ttu-id="942a5-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="942a5-124">-StorageAccountName</span></span>
<span data-ttu-id="942a5-125">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="942a5-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="942a5-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="942a5-126">-Confirm</span></span>
<span data-ttu-id="942a5-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="942a5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="942a5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="942a5-128">-WhatIf</span></span>
<span data-ttu-id="942a5-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="942a5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="942a5-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="942a5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="942a5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="942a5-131">CommonParameters</span></span>
<span data-ttu-id="942a5-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="942a5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="942a5-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="942a5-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="942a5-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="942a5-134">INPUTS</span></span>

### <span data-ttu-id="942a5-135">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="942a5-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="942a5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="942a5-136">System.String</span></span>

## <span data-ttu-id="942a5-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="942a5-137">OUTPUTS</span></span>

### <span data-ttu-id="942a5-138">Microsoft. Azure. commands. Management. Storage. Models. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="942a5-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="942a5-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="942a5-139">NOTES</span></span>

## <span data-ttu-id="942a5-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="942a5-140">RELATED LINKS</span></span>
