---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: f5620baf0cbd2f5c195b981787ac9def98851fe2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258993"
---
# <span data-ttu-id="2f33a-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2f33a-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="2f33a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f33a-102">SYNOPSIS</span></span>
<span data-ttu-id="2f33a-103">Tar bort en lagrad åtkomst princip från en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="2f33a-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="2f33a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f33a-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f33a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f33a-105">DESCRIPTION</span></span>
<span data-ttu-id="2f33a-106">Cmdleten **Remove-AzStorageQueueStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="2f33a-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="2f33a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f33a-107">EXAMPLES</span></span>

### <span data-ttu-id="2f33a-108">Exempel 1: ta bort en lagrad åtkomst princip från en lagrings kö</span><span class="sxs-lookup"><span data-stu-id="2f33a-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="2f33a-109">Det här kommandot tar bort en åtkomst princip med namnet Policy04 från lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="2f33a-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="2f33a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f33a-110">PARAMETERS</span></span>

### <span data-ttu-id="2f33a-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2f33a-111">-Context</span></span>
<span data-ttu-id="2f33a-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="2f33a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2f33a-113">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="2f33a-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2f33a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f33a-114">-DefaultProfile</span></span>
<span data-ttu-id="2f33a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f33a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f33a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f33a-116">-PassThru</span></span>
<span data-ttu-id="2f33a-117">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="2f33a-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="2f33a-118">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="2f33a-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2f33a-119">-Princip</span><span class="sxs-lookup"><span data-stu-id="2f33a-119">-Policy</span></span>
<span data-ttu-id="2f33a-120">Anger namnet på den lagrade åtkomst principen som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f33a-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2f33a-121">-Kö</span><span class="sxs-lookup"><span data-stu-id="2f33a-121">-Queue</span></span>
<span data-ttu-id="2f33a-122">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="2f33a-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="2f33a-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2f33a-123">-Confirm</span></span>
<span data-ttu-id="2f33a-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f33a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f33a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f33a-125">-WhatIf</span></span>
<span data-ttu-id="2f33a-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2f33a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f33a-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2f33a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f33a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f33a-128">CommonParameters</span></span>
<span data-ttu-id="2f33a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f33a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f33a-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f33a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f33a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f33a-131">INPUTS</span></span>

### <span data-ttu-id="2f33a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2f33a-132">System.String</span></span>

### <span data-ttu-id="2f33a-133">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2f33a-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2f33a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f33a-134">OUTPUTS</span></span>

### <span data-ttu-id="2f33a-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f33a-135">System.Boolean</span></span>

## <span data-ttu-id="2f33a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f33a-136">NOTES</span></span>

## <span data-ttu-id="2f33a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f33a-137">RELATED LINKS</span></span>

[<span data-ttu-id="2f33a-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2f33a-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2f33a-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2f33a-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="2f33a-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2f33a-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2f33a-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2f33a-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)