---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 9c37421ff33bfb7f2a2308512e28fa8373ee308c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928946"
---
# <span data-ttu-id="ee925-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee925-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="ee925-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee925-102">SYNOPSIS</span></span>
<span data-ttu-id="ee925-103">Tar bort en lagrad åtkomst princip från en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="ee925-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee925-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee925-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee925-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee925-105">DESCRIPTION</span></span>
<span data-ttu-id="ee925-106">Cmdleten **Remove-AzureStorageQueueStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="ee925-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="ee925-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee925-107">EXAMPLES</span></span>

### <span data-ttu-id="ee925-108">Exempel 1: ta bort en lagrad åtkomst princip från en lagrings kö</span><span class="sxs-lookup"><span data-stu-id="ee925-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="ee925-109">Det här kommandot tar bort en åtkomst princip med namnet Policy04 från lagringsmappen som heter kön.</span><span class="sxs-lookup"><span data-stu-id="ee925-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="ee925-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee925-110">PARAMETERS</span></span>

### <span data-ttu-id="ee925-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ee925-111">-Context</span></span>
<span data-ttu-id="ee925-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="ee925-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ee925-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="ee925-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ee925-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee925-114">-DefaultProfile</span></span>
<span data-ttu-id="ee925-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee925-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee925-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee925-116">-PassThru</span></span>
<span data-ttu-id="ee925-117">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="ee925-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ee925-118">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="ee925-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ee925-119">-Princip</span><span class="sxs-lookup"><span data-stu-id="ee925-119">-Policy</span></span>
<span data-ttu-id="ee925-120">Anger namnet på den lagrade åtkomst principen som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee925-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ee925-121">-Kö</span><span class="sxs-lookup"><span data-stu-id="ee925-121">-Queue</span></span>
<span data-ttu-id="ee925-122">Anger namnet på Azure Storage-kön.</span><span class="sxs-lookup"><span data-stu-id="ee925-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="ee925-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee925-123">-Confirm</span></span>
<span data-ttu-id="ee925-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee925-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee925-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee925-125">-WhatIf</span></span>
<span data-ttu-id="ee925-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ee925-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee925-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ee925-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee925-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee925-128">CommonParameters</span></span>
<span data-ttu-id="ee925-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee925-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee925-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee925-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee925-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee925-131">INPUTS</span></span>

### <span data-ttu-id="ee925-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ee925-132">System.String</span></span>

### <span data-ttu-id="ee925-133">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ee925-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ee925-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee925-134">OUTPUTS</span></span>

### <span data-ttu-id="ee925-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee925-135">System.Boolean</span></span>

## <span data-ttu-id="ee925-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee925-136">NOTES</span></span>

## <span data-ttu-id="ee925-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee925-137">RELATED LINKS</span></span>

[<span data-ttu-id="ee925-138">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee925-138">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ee925-139">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ee925-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ee925-140">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee925-140">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ee925-141">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee925-141">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
