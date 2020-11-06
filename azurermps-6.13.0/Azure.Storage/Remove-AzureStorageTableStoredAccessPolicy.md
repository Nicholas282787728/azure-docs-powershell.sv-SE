---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b1e06a31cfbe16cb04a7158cd62858683db6e131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575400"
---
# <span data-ttu-id="ef6d7-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ef6d7-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="ef6d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6d7-103">Tar bort en lagrad åtkomst princip från en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="ef6d7-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef6d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef6d7-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef6d7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef6d7-105">DESCRIPTION</span></span>
<span data-ttu-id="ef6d7-106">Cmdleten **Remove-AzureStorageTableStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="ef6d7-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="ef6d7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef6d7-107">EXAMPLES</span></span>

### <span data-ttu-id="ef6d7-108">Exempel 1: ta bort en lagrad åtkomst princip från en lagrings tabell</span><span class="sxs-lookup"><span data-stu-id="ef6d7-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="ef6d7-109">Det här kommandot tar bort principen med namnet Policy05 från lagrings tabellen tabell.</span><span class="sxs-lookup"><span data-stu-id="ef6d7-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="ef6d7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef6d7-110">PARAMETERS</span></span>

### <span data-ttu-id="ef6d7-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ef6d7-111">-Context</span></span>
<span data-ttu-id="ef6d7-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="ef6d7-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ef6d7-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="ef6d7-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ef6d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6d7-114">-DefaultProfile</span></span>
<span data-ttu-id="ef6d7-115">kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef6d7-115">communication with Azure.</span></span>

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

### <span data-ttu-id="ef6d7-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef6d7-116">-PassThru</span></span>
<span data-ttu-id="ef6d7-117">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="ef6d7-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ef6d7-118">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="ef6d7-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ef6d7-119">-Princip</span><span class="sxs-lookup"><span data-stu-id="ef6d7-119">-Policy</span></span>
<span data-ttu-id="ef6d7-120">Anger namnet på den lagrade åtkomst principen som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef6d7-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ef6d7-121">-Tabell</span><span class="sxs-lookup"><span data-stu-id="ef6d7-121">-Table</span></span>
<span data-ttu-id="ef6d7-122">Anger namnet på Azure-tabellen.</span><span class="sxs-lookup"><span data-stu-id="ef6d7-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="ef6d7-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef6d7-123">-Confirm</span></span>
<span data-ttu-id="ef6d7-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef6d7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef6d7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef6d7-125">-WhatIf</span></span>
<span data-ttu-id="ef6d7-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef6d7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef6d7-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef6d7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef6d7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6d7-128">CommonParameters</span></span>
<span data-ttu-id="ef6d7-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef6d7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6d7-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef6d7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6d7-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef6d7-131">INPUTS</span></span>

### <span data-ttu-id="ef6d7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ef6d7-132">System.String</span></span>

### <span data-ttu-id="ef6d7-133">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ef6d7-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ef6d7-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef6d7-134">OUTPUTS</span></span>

### <span data-ttu-id="ef6d7-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef6d7-135">System.Boolean</span></span>

## <span data-ttu-id="ef6d7-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef6d7-136">NOTES</span></span>

## <span data-ttu-id="ef6d7-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef6d7-137">RELATED LINKS</span></span>

[<span data-ttu-id="ef6d7-138">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ef6d7-138">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ef6d7-139">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ef6d7-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ef6d7-140">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ef6d7-140">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ef6d7-141">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ef6d7-141">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
