---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 1f5c97824a9296954f2c7bad742b5f8176359563
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581856"
---
# <span data-ttu-id="03062-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="03062-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="03062-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03062-102">SYNOPSIS</span></span>
<span data-ttu-id="03062-103">Tar bort en lagrad åtkomst princip från en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="03062-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03062-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03062-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03062-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03062-105">DESCRIPTION</span></span>
<span data-ttu-id="03062-106">Cmdleten **Remove-AzureStorageQueueStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="03062-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="03062-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03062-107">EXAMPLES</span></span>

### <span data-ttu-id="03062-108">Exempel 1: ta bort en lagrad åtkomst princip från en lagrings kö</span><span class="sxs-lookup"><span data-stu-id="03062-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="03062-109">Det här kommandot tar bort en åtkomst princip med namnet Policy04 från lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="03062-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="03062-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03062-110">PARAMETERS</span></span>

### <span data-ttu-id="03062-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="03062-111">-Context</span></span>
<span data-ttu-id="03062-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="03062-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="03062-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="03062-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03062-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03062-114">-DefaultProfile</span></span>
<span data-ttu-id="03062-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03062-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03062-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03062-116">-PassThru</span></span>
<span data-ttu-id="03062-117">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="03062-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="03062-118">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="03062-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="03062-119">-Princip</span><span class="sxs-lookup"><span data-stu-id="03062-119">-Policy</span></span>
<span data-ttu-id="03062-120">Anger namnet på den lagrade åtkomst principen som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="03062-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03062-121">-Kö</span><span class="sxs-lookup"><span data-stu-id="03062-121">-Queue</span></span>
<span data-ttu-id="03062-122">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="03062-122">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03062-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="03062-123">-Confirm</span></span>
<span data-ttu-id="03062-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="03062-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03062-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03062-125">-WhatIf</span></span>
<span data-ttu-id="03062-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="03062-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03062-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="03062-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03062-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03062-128">CommonParameters</span></span>
<span data-ttu-id="03062-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03062-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03062-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03062-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03062-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03062-131">INPUTS</span></span>

### <span data-ttu-id="03062-132">System. String</span><span class="sxs-lookup"><span data-stu-id="03062-132">System.String</span></span>

### <span data-ttu-id="03062-133">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="03062-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="03062-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03062-134">OUTPUTS</span></span>

### <span data-ttu-id="03062-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03062-135">System.Boolean</span></span>

## <span data-ttu-id="03062-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03062-136">NOTES</span></span>

## <span data-ttu-id="03062-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03062-137">RELATED LINKS</span></span>

[<span data-ttu-id="03062-138">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="03062-138">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="03062-139">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="03062-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="03062-140">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="03062-140">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="03062-141">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="03062-141">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
