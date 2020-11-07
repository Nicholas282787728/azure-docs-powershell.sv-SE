---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 32bf76e80dbd088b133d4401dc51bb1f49b2593b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746289"
---
# <span data-ttu-id="8192c-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8192c-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="8192c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8192c-102">SYNOPSIS</span></span>
<span data-ttu-id="8192c-103">Tar bort en lagrad åtkomst princip från en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="8192c-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="8192c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8192c-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8192c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8192c-105">DESCRIPTION</span></span>
<span data-ttu-id="8192c-106">Cmdleten **Remove-AzStorageQueueStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="8192c-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="8192c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8192c-107">EXAMPLES</span></span>

### <span data-ttu-id="8192c-108">Exempel 1: ta bort en lagrad åtkomst princip från en lagrings kö</span><span class="sxs-lookup"><span data-stu-id="8192c-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="8192c-109">Det här kommandot tar bort en åtkomst princip med namnet Policy04 från lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="8192c-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="8192c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8192c-110">PARAMETERS</span></span>

### <span data-ttu-id="8192c-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="8192c-111">-Context</span></span>
<span data-ttu-id="8192c-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="8192c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8192c-113">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="8192c-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8192c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8192c-114">-DefaultProfile</span></span>
<span data-ttu-id="8192c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8192c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8192c-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8192c-116">-PassThru</span></span>
<span data-ttu-id="8192c-117">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="8192c-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="8192c-118">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="8192c-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8192c-119">-Princip</span><span class="sxs-lookup"><span data-stu-id="8192c-119">-Policy</span></span>
<span data-ttu-id="8192c-120">Anger namnet på den lagrade åtkomst principen som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8192c-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8192c-121">-Kö</span><span class="sxs-lookup"><span data-stu-id="8192c-121">-Queue</span></span>
<span data-ttu-id="8192c-122">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="8192c-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="8192c-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8192c-123">-Confirm</span></span>
<span data-ttu-id="8192c-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8192c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8192c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8192c-125">-WhatIf</span></span>
<span data-ttu-id="8192c-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8192c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8192c-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8192c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8192c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8192c-128">CommonParameters</span></span>
<span data-ttu-id="8192c-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8192c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8192c-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8192c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8192c-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8192c-131">INPUTS</span></span>

### <span data-ttu-id="8192c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8192c-132">System.String</span></span>

### <span data-ttu-id="8192c-133">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8192c-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8192c-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8192c-134">OUTPUTS</span></span>

### <span data-ttu-id="8192c-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8192c-135">System.Boolean</span></span>

## <span data-ttu-id="8192c-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8192c-136">NOTES</span></span>

## <span data-ttu-id="8192c-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8192c-137">RELATED LINKS</span></span>

[<span data-ttu-id="8192c-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8192c-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8192c-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8192c-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="8192c-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8192c-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8192c-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8192c-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
